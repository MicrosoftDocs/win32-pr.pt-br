---
description: Usado com as funções CryptAcquireContext e CryptSetProvider.
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: Nomes de provedor criptográfico (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a5cbe497e56144a9948dab96be0c03dd5a99f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920823"
---
# <a name="cryptographic-provider-names"></a>Nomes de provedor criptográfico

Os seguintes nomes de CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) são definidos em Wincrypt. h. Essas constantes são usadas com as funções [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) e [**CryptSetProvider**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera) .



| Constante/valor                                                                                                                                                                                                                                                                                          | Descrição                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ DH \_ Schannel \_ prov**</dt> <dt>"provedor criptográfico do Microsoft DH Schannel"</dt> </dl>      | O [provedor criptográfico Microsoft DSS e Diffie-Hellman/Schannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md).<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ DH \_ prov**</dt> <dt>"Microsoft Base DSS e Diffie-Hellman provedor criptográfico"</dt> </dl>     | O [Microsoft Base DSS e o provedor de criptografia Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**MS \_ Definição \_ de \_ DSS do def**</dt> <dt>"provedor CRIPTOGRÁFICO do Microsoft Base DSS"</dt> </dl>                                  | O [provedor criptográfico do Microsoft DSS](microsoft-dss-cryptographic-provider.md).<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**MS \_ DEF \_ Prov**</dt> <dt>"Microsoft Base Cryptographic Provider v 1.0"</dt> </dl>                                              | O [provedor Microsoft Base Cryptographic](microsoft-base-cryptographic-provider.md).<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ Schannel \_ prov**</dt> <dt>"provedor criptográfico Microsoft RSA Schannel"</dt> </dl>  | O [provedor criptográfico Microsoft RSA/Schannel](microsoft-rsa-schannel-cryptographic-provider.md).<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ SIG \_ Prov**</dt> <dt>"provedor CRIPTOGRÁFICO de assinatura do Microsoft RSA"</dt> </dl>                | Não há suporte para o [provedor criptográfico da assinatura RSA da Microsoft](microsoft-rsa-signature-cryptographic-provider.md) .<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**MS \_ ENH \_ DSS \_ DH \_ Prov**</dt> <dt>"Microsoft Enhanced DSS e Diffie-Hellman provedor criptográfico"</dt> </dl> | O [provedor criptográfico do Microsoft Enhanced DSS e Diffie-Hellman](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**MS \_ ENH \_ RSA \_ AES \_ Prov**</dt> <dt>"Microsoft Enhanced RSA and AES Cryptographic Provider"</dt> </dl>         | O [provedor criptográfico do Microsoft AES](microsoft-aes-cryptographic-provider.md).<br/> * * Windows XP: * * "Microsoft Enhanced RSA and AES Cryptographic Provider (prototype)"<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**MS \_ \_Prov aprimorado**</dt> <dt>"provedor de criptografia aprimorado da Microsoft v 1.0"</dt> </dl>                           | O [provedor criptográfico aprimorado da Microsoft](microsoft-enhanced-cryptographic-provider.md).<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**MS \_ SCARTAR \_ Prov**</dt> <dt>"provedor de criptografia de cartão inteligente de base Microsoft"</dt> </dl>                                         | O [provedor de serviços de criptografia de cartão inteligente Microsoft base](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider).<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**MS \_ FORTE \_ Prov**</dt> <dt>"provedor de criptografia forte da Microsoft"</dt> </dl>                                        | O [provedor de criptografia forte da Microsoft](microsoft-strong-cryptographic-provider.md).<br/>                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
