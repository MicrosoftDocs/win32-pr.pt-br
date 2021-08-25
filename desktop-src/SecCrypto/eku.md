---
description: Representa uma única propriedade EKU (uso estendido de chave) de um certificado.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Objeto EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bd887204abc31583e596e94c25b64addcfe8109e6432845d25d939fd8e79e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875136"
---
# <a name="eku-object"></a>Objeto EKU

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **EKU** representa uma única propriedade EKU (uso estendido de chave) de um certificado.

## <a name="members"></a>Membros

O objeto **EKU** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **EKU** tem essas propriedades.



| Propriedade                            | Tipo de acesso           | Descrição                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome**](eku-name.md)<br/> | Leitura/gravação<br/> | Define ou recupera um valor de enumeração que especifica o nome do CAPICOM do EKU. Essa é a propriedade padrão.<br/>                                                                                   |
| [**OIDs**](eku-oid.md)<br/>   | Leitura/gravação<br/> | Define ou recupera uma cadeia de caracteres que contém um valor de cadeia de caracteres OID ( [*identificador de objeto*](../secgloss/o-gly.md) EKU), conforme definido em Wincrypt. h.<br/> |



 

## <a name="remarks"></a>Comentários

O objeto **EKU** é usado pela seguinte coleção e Propriedade:

-   Coleção [**EKUs**](ekus.md)
-   Propriedade [**CertificateStatus. EKU**](certificatestatus-eku.md)

Não é possível criar o objeto **EKU** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
