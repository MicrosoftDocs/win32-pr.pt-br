---
description: Representa um estágio de pipeline, incluindo detalhes do sombreador usado.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PipeLineStage
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919856"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>Estrutura PipeLineStage

Representa um estágio de pipeline, incluindo detalhes do sombreador usado.

## <a name="syntax"></a>Sintaxe


```C++
} PipeLineStage;
```

## <a name="members"></a>Membros

**Prepareid**  
A ID do estágio do pipeline.

**Depurável**  
true se o estágio do pipeline oferecer suporte à depuração; caso contrário, false.

**StageName**  
Uma cadeia de caracteres COM que contém o nome do estágio do pipeline.

**GuaranteedOutput**  
true se o estágio do pipeline sempre tiver saída de pipeline; caso contrário, false.

**DebugEntryPoint**  
Uma cadeia de caracteres COM que contém o nome do ponto de entrada do sombreador, se houver um.

**Shaderfile**  
Uma cadeia de caracteres COM que contém o caminho de arquivo de origem do sombreador.

**ShaderByteStreamPtr**  
Um FILEPTR para o fluxo de bytes do sombreador. Isso é passado de volta para depurar.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



