# DEB/RPM distribution
<a href="repo_nzlosh_public.gpg">Repository signing public key</a>

# Debian

The following steps will install err-stackstorm package on your distribution if it is available.

```
source <(sed -r 's/^/OS_/g' /etc/os-release)
echo Installation of err-stackstorm on $OS_ID $OS_VERSION_CODENAME
curl https://raw.githubusercontent.com/nzlosh/repo/refs/heads/main/repo_nzlosh_public.gpg | gpg --dearmor > /etc/apt/trusted.gpg.d/err-stackstorm.gpg
echo "deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/err-stackstorm.gpg] https://nzlosh.github.io/repo/$OS_ID $OS_VERSION_CODENAME main" > /etc/apt/sources.list.d/err-stackstorm.list
apt update
apt install err-stackstorm
```
