---
description: Recupera o objeto de signatário que representa o assinante indexado.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Propriedade signers. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33630586282b745da94a442c13a0e85574c5f2e06fc04ab909e4ebf59fc2707b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898403"
---
# <a name="signersitem-property"></a>Propriedade signers. Item

\[A propriedade **Item** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use uma coleção de objetos CmsSigner. Para obter mais informações, consulte a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **Item** recupera o objeto de [**signatário**](signer.md) que representa o assinante indexado. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor da propriedade

O objeto de [**signatário**](signer.md) que representa o assinante indexado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Signatários**](signers.md)
</dt> </dl>

 

 
