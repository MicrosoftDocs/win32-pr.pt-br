---
description: Recupera o objeto EKU que representa a propriedade de EKU (uso estendido de chave) indexada.
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'Propriedade IEKUs:: item'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b81e00de0ca8346d56ceafeb8b0d11353219c5fc6ab3eb0b29a9f7c868f79505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875146"
---
# <a name="iekusitem-property"></a>Propriedade IEKUs:: item

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Item** recupera o objeto [**EKU**](eku.md) que representa a propriedade de EKU (uso estendido de chave) indexada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**EKU**](eku.md) que representa a propriedade de EKU (uso estendido de chave) indexado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EKUs**](ekus.md)
</dt> </dl>

 

 
