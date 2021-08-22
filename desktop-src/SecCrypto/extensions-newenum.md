---
description: A propriedade NewEnum de Extensions recupera uma interface IEnumVARIANT em um objeto que pode ser usado \_ para enumerar a coleção. Essa propriedade está oculta no Visual Basic Scripting Edition (VBScript).
ms.assetid: 0e461683-bb48-4961-91ef-36af1c3f863e
title: Extensions._NewEnum propriedade
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86d5c42d7eff36d526b10244e968aabe63871b26bde181e7976731921ac7cc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006814"
---
# <a name="extensions_newenum-property"></a>Extensões. \_ Propriedade NewEnum

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **\_ propriedade NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade está oculta no Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Syntax


```VB
Extensions._NewEnum As IUnknown
```



## <a name="property-value"></a>Valor da propriedade

Uma [**interface IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.

## <a name="remarks"></a>Comentários

Essa propriedade é usada automaticamente internamente quando você usa o `For Each In` constructo no Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Extensões**](extensions.md)
</dt> </dl>

 

 
