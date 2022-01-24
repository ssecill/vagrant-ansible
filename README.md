# vagrant-ansible

```
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh
```
```
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
```
```
helm create mychart
helm upgrade --install secil ./mychart -f ./mychart/values.yaml --set "services.secil\.services\.sns.cap_add={SYS_ADMIN,TEST}"
helm get values secil
```
