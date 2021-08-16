---
description: Define ou recupera um valor de enumeração que especifica o nome CAPICOM do EKU. Essa é a propriedade padrão.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: Propriedade IEKU::Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ca1564b943874ec086dd5e4459e69543cbdc90ebde2a11a2084c3054e3727dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767224"
---
# <a name="iekuname-property"></a>Propriedade IEKU::Name

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade Name** define ou recupera um valor de enumeração que especifica o nome CAPICOM do EKU. Essa é a propriedade padrão.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Valor da propriedade

Um valor da [**enumeração \_ CAPICOM EKU**](capicom-eku.md) que especifica o nome CAPICOM da EKU. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**CAPICOM \_ EKU \_ OTHER**</dt> </dl>                                                      | O certificado tem usos definidos na política local. Isso será usado se o EKU necessário não for predefinido e o valor OID precisar ser definido pelo aplicativo.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**CAPICOM \_ EKU \_ SERVER \_ AUTH**</dt> </dl>                                   | O certificado pode ser usado para autenticar um servidor.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**CAPICOM \_ EKU \_ CLIENT \_ AUTH**</dt> </dl>                                   | O certificado pode ser usado para autenticar um cliente.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**ASSINATURA DE CÓDIGO \_ CAPICOM EKU \_ \_**</dt> </dl>                                | O certificado pode ser usado para criar uma assinatura digital.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**CAPICOM \_ EKU \_ EMAIL \_ PROTECTION**</dt> </dl>                    | O certificado pode ser usado para proteção por email.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**LOGON DE CARTÃO INTELIGENTE \_ CAPICOM \_ EKU \_**</dt> </dl>                       | O certificado pode ser usado para logon de cartão inteligente. Introduzido no CAPICOM 2.0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**CAPICOM \_ EKU \_ ENCRYPTING \_ FILE \_ SYSTEM**</dt> </dl> | O certificado pode ser usado para o EFS. Introduzido no CAPICOM 2.0.<br/>                                                                                      |



 

## <a name="remarks"></a>Comentários

Quando o valor dessa propriedade é redefinido, direta ou indiretamente, todo [*o*](../secgloss/s-gly.md) estado do objeto é redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
