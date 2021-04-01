---
description: Representa informações sobre uma única entrada no layout de buffer de uma malha.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura MeshDataBufferLayoutEntry
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646168"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>Estrutura MeshDataBufferLayoutEntry

Representa informações sobre uma única entrada no layout de buffer de uma malha.

## <a name="syntax"></a>Sintaxe


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Membros

**pName**  
Uma cadeia de caracteres COM que contém o nome da entrada.

**numComponents**  
O número de componentes homogêneos (valores) que compõem essa entrada.

**isposition**  
true se a entrada for uma posição; caso contrário, false.

**format**  
O formato de dados da entrada (registro). Para obter mais informações, consulte a \_ enumeração de formato de registro.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



