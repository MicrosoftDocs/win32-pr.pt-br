---
description: Define ou recupera um valor de enumeração que especifica o nome do CAPICOM do EKU. Essa é a propriedade padrão.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'Propriedade IEKU:: Name'
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
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750093"
---
# <a name="iekuname-property"></a>Propriedade IEKU:: Name

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Name** define ou recupera um valor de enumeração que especifica o nome do CAPICOM do EKU. Essa é a propriedade padrão.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Valor da propriedade

Um valor da enumeração [**\_ EKU de CAPICOM**](capicom-eku.md) que especifica o nome do CAPICOM do EKU. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**\_outro EKU de CApicom \_**</dt> </dl>                                                      | O certificado tem usos definidos na política local. Isso será usado se o EKU necessário não for predefinido e o valor de OID precisar ser definido pelo aplicativo.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**\_autenticação de \_ servidor de EKU capicor \_**</dt> </dl>                                   | O certificado pode ser usado para autenticar um servidor.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**\_autenticação de \_ cliente de EKU capicor \_**</dt> </dl>                                   | O certificado pode ser usado para autenticar um cliente.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**\_assinatura de \_ código de EKU CAPICOM \_**</dt> </dl>                                | O certificado pode ser usado para criar uma assinatura digital.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**\_proteção de \_ email de EKU CAPICOM \_**</dt> </dl>                    | O certificado pode ser usado para proteção de email.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**\_logon de \_ cartão inteligente \_ capicor EKU**</dt> </dl>                       | O certificado pode ser usado para logon de cartão inteligente. Introduzido no CAPICOM 2,0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**\_sistema de \_ arquivos com criptografia EKU \_ de CAPICOM \_**</dt> </dl> | O certificado pode ser usado para o EFS. Introduzido no CAPICOM 2,0.<br/>                                                                                      |



 

## <a name="remarks"></a>Comentários

Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
