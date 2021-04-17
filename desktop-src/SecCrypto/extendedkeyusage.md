---
description: Fornece acesso somente leitura às propriedades EKU (uso estendido de chave) de um certificado.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Objeto ExtendedKeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748047"
---
# <a name="extendedkeyusage-object"></a>Objeto ExtendedKeyUsage

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **ExtendedKeyUsage** fornece acesso somente leitura às propriedades EKU (uso estendido de chave) de um certificado.

## <a name="members"></a>Membros

O objeto **ExtendedKeyUsage** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **ExtendedKeyUsage** tem essas propriedades.



| Propriedade                                                     | Tipo de acesso          | Descrição                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EKUs**](extendedkeyusage-ekus.md)<br/>             | Somente leitura<br/> | Coleção [**EKUs**](ekus.md) que contém os objetos [**EKU**](eku.md) para o certificado.<br/>                            |
| [**IsCritical**](extendedkeyusage-iscritical.md)<br/> | Somente leitura<br/> | Recupera um valor **booliano** que indica se a extensão EKU está marcada como crítica.<br/>                                   |
| [**IsPresent**](extendedkeyusage-ispresent.md)<br/>   | Somente leitura<br/> | Recupera um valor **booliano** que indica se a extensão EKU está presente.<br/> Essa é a propriedade padrão. <br/> |



 

## <a name="remarks"></a>Comentários

O objeto **ExtendedKeyUsage** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
