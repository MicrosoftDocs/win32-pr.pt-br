---
description: Representa informações sobre uma solicitação de depurador de sombreador.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura DebugShaderRequestInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9691b13936ca8ec8e75aa02d9525a9d57143b19e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628455"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span id="vspixengine.debugshaderrequestinfo"></span>Estrutura DebugShaderRequestInfo

Representa informações sobre uma solicitação de depurador de sombreador.

## <a name="syntax"></a>Sintaxe


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a>Membros

**Test**  
O estágio do pipeline a ser depurado.

**1008**  
A ID do evento de gráficos a ser depurado.

**frameNumber**  
O quadro a ser depurado.

**deles**  
O vértice a ser depurado.

**pixel**  
O pixel a ser depurado.

**groupCoordinates**  
As coordenadas do grupo a ser depurado.

**threadCoordinates**  
As coordenadas do thread a ser depurado

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



