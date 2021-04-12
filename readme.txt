helm install my-kf bitnami/kafka

helm install my-pg-db -f postgres-db.yaml bitnami/postgresql

helm install my-auth -f otus-sample-auth.yaml ./otus-sample-auth
helm install my-profile -f otus-sample-profile.yaml ./otus-sample-profile
helm install my-account -f otus-sample-account.yaml ./otus-sample-account
helm install my-event -f otus-sample-event.yaml ./otus-sample-event
helm install my-order -f otus-sample-order.yaml ./otus-sample-order
helm install my-bill -f otus-sample-bill.yaml ./otus-sample-bill
helm install my-email -f otus-sample-email.yaml ./otus-sample-email

helm install my-ing1 -f otus-sample-ing.yaml ./otus-sample-ing1
helm install my-ing2 -f otus-sample-ing.yaml ./otus-sample-ing2

newman run Otus-8.postman_collection.json -e Otus6.postman_environment.json --delay-request 100

helm uninstall my-ing1
helm uninstall my-ing2

helm uninstall my-email                                            
helm uninstall my-bill
helm uninstall my-order
helm uninstall my-event
helm uninstall my-account
helm uninstall my-profile
helm uninstall my-auth

helm uninstall my-pg-db

helm uninstall my-kf
