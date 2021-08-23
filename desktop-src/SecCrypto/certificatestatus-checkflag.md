---
description: Define ou recupera os sinalizadores de verificação de validade de um certificado.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: Propriedade CertificateStatus. CheckFlag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CheckFlag
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1c47d7f1c59ecd629db1d6fc735f61b8d1fe59c864ffa8a5a9f013c86bd30faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877446"
---
# <a name="certificatestatuscheckflag-property"></a>Propriedade CertificateStatus. CheckFlag

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **CheckFlag** define ou recupera os sinalizadores de verificação de validade de um certificado.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Valor da propriedade

Um valor da enumeração [**do \_ \_ sinalizador de verificação CAPICOM**](capicom-check-flag.md) que descreve as verificações de validade do certificado. O valor padrão é **Capicot \_ verificar \_ \_ tudo online**.

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1:** O valor padrão é [**Capicore \_ \_ \_ validade da assinatura**](capicom-check-flag.md), [**CAPICOM a \_ validade do \_ tempo \_ de verificação**](capicom-check-flag.md), [**CAPICOM a \_ \_ \_ raiz confiável**](capicom-check-flag.md)e a [**\_ \_ \_ cadeia de verificação de capicor**](capicom-check-flag.md).

**Capicom 2,0 e anteriores:** O valor padrão é [**Capicot \_ verificar \_ \_ validade da assinatura**](capicom-check-flag.md), [**CAPICOM a \_ validade do \_ tempo \_ de verificação**](capicom-check-flag.md)e o [**CAPICOM \_ verificar \_ \_ raiz confiável**](capicom-check-flag.md).

A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**\_ \_ restrições básicas de verificação de CAPICOM \_**</dt> </dl>                          | Verifica as restrições básicas. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**\_ \_ cadeia completa de verificação de CAPICOM \_**</dt> </dl>                                   | Verifica a cadeia completa. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**\_restrições de \_ nome de verificação de CAPICOM \_**</dt> </dl>                             | Verifica as restrições de nome. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**verificação de capicor \_ \_ período de validade aninhado \_ \_**</dt> </dl>          | Verifica a validade aninhada. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**verificação de CAPICOM \_ \_ None**</dt> </dl>                                                                  | Nenhuma verificação de validade é feita.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**capicore \_ verificar \_ offline \_ tudo**</dt> </dl>                                            | Verifica todos offline. Verificações de revogação são executadas em todos os certificados na cadeia, exceto para o certificado raiz. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**capicot \_ verificar \_ \_ tudo online**</dt> </dl>                                               | Verifica tudo online. Verificações de revogação são executadas em todos os certificados na cadeia, exceto para o certificado raiz. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**CAPICOM \_ verificar \_ \_ status de revogação offline \_**</dt> </dl> | Verifica o status de revogação de todos os certificados na cadeia usando somente CRLs offline.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**CAPICOM \_ verificar \_ \_ status de revogação online \_**</dt> </dl>    | Verifica o status de revogação de todos os certificados na cadeia usando as CRLs disponíveis online. As CRLs são baixadas usando a extensão CDP no certificado.<br/> Se a CRL tiver sido baixada e não tiver expirado, capicor o usará e não ficará online.<br/> Se uma CRL não tiver sido baixada ou estiver desatualizada, capicor ficará online para tentar baixar a CRL.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**\_validade da \_ assinatura \_ verificar CAPICOM**</dt> </dl>                       | Verifica se há assinaturas válidas em todos os certificados na cadeia.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**\_validade do \_ tempo de verificação de CAPICOM \_**</dt> </dl>                                      | Verifica a validade do tempo de todos os certificados na cadeia.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**CAPICOM \_ verificar \_ \_ raiz confiável**</dt> </dl>                                         | Verifica se há uma raiz confiável da cadeia de certificados.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
