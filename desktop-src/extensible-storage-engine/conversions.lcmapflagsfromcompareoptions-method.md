---
description: 'Saiba mais sobre: método conversões. LCMapFlagsFromCompareOptions'
title: Método conversões. LCMapFlagsFromCompareOptions
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808322"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a>Método conversões. LCMapFlagsFromCompareOptions

Forneça CompareOptions, transforme-os em sinalizadores de LCMapString. Opções desconhecidas são ignoradas.

Esta API não está em conformidade com CLS. 

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a>Parâmetros

  - compareOptions  
    Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
    
    As opções a serem convertidas.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. UInt32](/dotnet/api/system.uint32)  
Os sinalizadores LCMapString que correspondem às opções de comparação. As opções sem suporte são ignoradas.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe conversões](./conversions-class.md)

[Membros de conversões](./conversions-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
