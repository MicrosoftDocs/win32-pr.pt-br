---
description: 'Saiba mais sobre: Método Conversions.CompareOptionsFromLCMapFlags'
title: Método Conversions.CompareOptionsFromLCMapFlags
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfe3a65c52d23ee335a81560775f0063b8ca81a10cc43c1787e353a5b803eed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117901842"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>Método Conversions.CompareOptionsFromLCMapFlags

Determinados sinalizadores para LCMapFlags, transforme-os em opções de comparação. As opções desconhecidas são ignoradas.

Esta API não está em conformidade com CLS. 

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a>Parâmetros

  - lcmapFlags  
    Tipo: [System.UInt32](/dotnet/api/system.uint32)  
    
    Sinalizadores LCMapString.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)  
CompareOptions que descrevem os sinalizadores (conhecidos).  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Conversions](./conversions-class.md)

[Membros de conversões](./conversions-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
