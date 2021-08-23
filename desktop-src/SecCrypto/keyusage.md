---
description: Fornece acesso somente leitura às propriedades de uso de chave de um certificado.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: Objeto KeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 37b1e33ccb92b2d46effa9f0575f0331fa064e79d172715b8746355d5e99d2b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622266"
---
# <a name="keyusage-object"></a>Objeto KeyUsage

\[O **objeto KeyUsage** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **objeto KeyUsage** fornece acesso somente leitura às propriedades de uso de chave de um certificado.

## <a name="members"></a>Membros

O **objeto KeyUsage** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto KeyUsage** tem essas propriedades.



| Propriedade                                                                           | Tipo de acesso          | Descrição                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iscritical**](keyusage-iscritical.md)<br/>                               | Somente leitura<br/> | Recupera um valor booliana que indica se a extensão **KeyUsage** está marcada como crítica.<br/>                                  |
| [**IsCRLSignEnabled**](keyusage-iscrlsignenabled.md)<br/>                   | Somente leitura<br/> | Recupera um valor booliana que indica se o bit CRLSign está definido.<br/>                                                         |
| [**IsDataEnciphermentEnabled**](keyusage-isdataenciphermentenabled.md)<br/> | Somente leitura<br/> | Recupera um valor booliana que indica se o bit dataEncipherment está definido.<br/>                                                |
| [**IsDecipherOnlyEnabled**](keyusage-isdecipheronlyenabled.md)<br/>         | Somente leitura<br/> | Recupera um valor booliana que indica se o bit de desdadosOnly está definido.<br/>                                                    |
| [**IsDigitalSignatureEnabled**](keyusage-isdigitalsignatureenabled.md)<br/> | Somente leitura<br/> | Recupera um valor booliana que indica se o bit digitalSignature está definido.<br/>                                                |
| [**IsEncipherOnlyEnabled**](keyusage-isencipheronlyenabled.md)<br/>         | Somente leitura<br/> | Recupera um valor booliana que indica se o bit encipherOnly está definido.<br/>                                                    |
| [**IsKeyAgreementEnabled**](keyusage-iskeyagreementenabled.md)<br/>         | Somente leitura<br/> | Recupera um valor booliana que indica se o bit keyAgreement está definido.<br/>                                                    |
| [**IsKeyCertSignEnabled**](keyusage-iskeycertsignenabled.md)<br/>           | Somente leitura<br/> | Recupera um valor booliana que indica se o bit keyCertSign está definido.<br/>                                                     |
| [**IsKeyEnciphermentEnabled**](keyusage-iskeyenciphermentenabled.md)<br/>   | Somente leitura<br/> | Recupera um valor booliana que indica se o bit keyEncipherment está definido.<br/>                                                 |
| [**IsNonRepudiationEnabled**](keyusage-isnonrepudiationenabled.md)<br/>     | Somente leitura<br/> | Recupera um valor booliano que indica se o bit nonRepudiationEnabled está definido.<br/>                                           |
| [**IsPresent**](keyusage-ispresent.md)<br/>                                 | Somente leitura<br/> | Recupera um valor booliana que indica se a extensão **KeyUsage** está presente.<br/> Essa é a propriedade padrão.<br/> |



 

## <a name="remarks"></a>Comentários

O **objeto KeyUsage** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
