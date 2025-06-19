# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Generalized Linear Latent Variable Models Use gllvm With (In) R Software
install.packages("gllvm")
install.packages("mvabund")
library("mvabund")
library("gllvm")
gllvm = read.csv("https://raw.githubusercontent.com/timbulwidodostp/gllvm/main/gllvm/gllvm.csv",sep = ";")
# Estimation Generalized Linear Latent Variable Models Use gllvm With (In) R Software
gllvm$y <- cbind(gllvm$Alopacce, gllvm$Alopcune, gllvm$Alopfabr, gllvm$Arctlute, gllvm$Arctperi, gllvm$Auloalbi)
gllvm_negative_binomial <- gllvm(y = gllvm$y, family = "negative.binomial")
gllvm_negative_binomial
summary(gllvm_negative_binomial)
gllvm_poisson <- gllvm(y = gllvm$y, family = "poisson")
gllvm_poisson
summary(gllvm_poisson)
gllvm_ZIP <- gllvm(y = gllvm$y, family = "ZIP")
gllvm_ZIP
summary(gllvm_ZIP)
gllvm_tweedie <- gllvm(y = gllvm$y, family = "tweedie")
gllvm_tweedie
summary(gllvm_tweedie)
# Generalized Linear Latent Variable Models Use gllvm With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished