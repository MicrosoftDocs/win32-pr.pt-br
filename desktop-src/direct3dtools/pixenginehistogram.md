---
description: Representa um histograma de uma textura.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixEngineHistogram
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e6235287d2d87bf6fe1bd79c13813e6bb8500bc3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622162"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>Estrutura PixEngineHistogram

Representa um histograma de uma textura.

## <a name="syntax"></a>Sintaxe


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Membros

**horizontalMin**  
Os valores mínimos para cada um dos componentes X, Y, Z e W no eixo horizontal (domínio) do histograma.

**horizontalMax**  
Os valores máximos para cada um dos componentes X, Y, Z e W no eixo horizontal (domínio) do histograma.

**verticalMin**  
Os valores mínimos para cada um dos componentes X, Y, Z e W no eixo vertical (intervalo) do histograma.

**verticalMax**  
Os valores máximos para cada um dos componentes X, Y, Z e W no eixo vertical (intervalo) do histograma.

**dataLength**  
O número de amostras consideradas no histograma.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



