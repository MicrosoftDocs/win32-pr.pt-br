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
ms.openlocfilehash: 10f1d1780404303109a72fe1a12023bc35b2c0ca
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625162"
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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



