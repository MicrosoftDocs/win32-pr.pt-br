---
description: A \_ Propriedade NewEnum de assinantes recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. essa propriedade é oculta no Visual Basic scripting Edition (VBScript).
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Propriedade Signers._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 866b85d8bfd5eee89a8c8766acb10baa024aa35e4f81b7d7289a6430d345fa6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898393"
---
# <a name="signers_newenum-property"></a>Assinantes. \_ Propriedade NewEnum

\[A propriedade **\_ NewEnum** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use uma coleção de objetos CmsSigner. Para obter mais informações, consulte a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. essa propriedade é oculta no Visual Basic scripting Edition (VBScript).

## <a name="syntax"></a>Syntax


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a>Valor da propriedade

Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.

## <a name="remarks"></a>Comentários

essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção no Visual Basic scripting Edition (VBScript).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Signatários**](signers.md)
</dt> </dl>

 

 
