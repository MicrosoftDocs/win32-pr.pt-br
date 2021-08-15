---
description: A propriedade NewEnum de Destinatários recupera uma interface IEnumVARIANT em um objeto que pode ser usado \_ para enumerar a coleção. Essa propriedade está oculta no Visual Basic Scripting Edition (VBScript).
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Recipients._NewEnum propriedade
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b71b015ccec741070d6c0261b0da094be98a716f1596ffab2d66575249ba9baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900746"
---
# <a name="recipients_newenum-property"></a>Destinatários. \_ Propriedade NewEnum

\[A **\_ propriedade NewEnum** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a Classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

A **\_ propriedade NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade está oculta no Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Syntax


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a>Valor da propriedade

Uma [**interface IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.

## <a name="remarks"></a>Comentários

Essa propriedade é usada automaticamente internamente quando você usa o `For Each In` constructo no Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Destinatários**](recipients.md)
</dt> </dl>

 

 
