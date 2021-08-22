---
description: Representa informações sobre o histórico de pixels.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixelHistoryOperation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 15cae4986b7dc109c08011d2cc23e1b6133de9e5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625182"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>Estrutura PixelHistoryOperation

Representa informações sobre o histórico de pixels.

## <a name="syntax"></a>Sintaxe


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Membros

**Eid**  
A ID do evento gráfico associado a essa operação.

**PCP**  
Chamadas empacotadas associadas a esta operação.

**renderTargetPtr**  
O destino de renderização originalmente associado (dentro do aplicativo capturado) a essa operação.

**iPrim**  
O índice do primitivo real associado à sua operação.

**numPrims**  
O número total de primitivos associados a essa operação.

**numVertsPerPrim**  
O número de vértices por primitivo.

**Iinstance**  
Ao renderizar instâncias, o número de instância da instância real associada a essa operação.

**iInstanceCount**  
Ao renderizar instâncias, o número total de instâncias associadas a essa operação.

**bAssemblerStageGeneratesInstanceID**  
true se o assembler de entrada gerar IDs de instância; caso contrário, false.

**sinalizadores**  
Uma combinação de valores PIXELHISTORYFLAGS. Para obter mais informações, consulte a enumeração PIXELHISTORYFLAGS.

**pVSFile**  
Um FILEPTR para o fluxo de byte do sombreador de pixel. Isso é passado de volta para depurar.

**pGSFile**  
Um FILEPTR para o fluxo de byte do sombreador de geometria. Isso é passado de volta para depurar.

**pPSFile**  
Um FILEPTR para o fluxo de byte do sombreador de pixel. Isso é passado de volta para depurar.

**pHSFile**  
Um FILEPTR para o fluxo de byte do sombreador de chassi. Isso é passado de volta para depurar.

**pDSFile**  
Um FILEPTR para o fluxo de byte do sombreador de domínio. Isso é passado de volta para depurar.

**pCSFile**  
Um FILEPTR para o fluxo de byte do sombreador de computação. Isso é passado de volta para depurar.

**VertexShaderFile**  
Uma cadeia de caracteres COM que contém o caminho do arquivo de origem do sombreador de vértice.

**PixelShaderFile**  
Uma cadeia de caracteres COM que contém o caminho do arquivo de origem do sombreador de pixel.

**GeometryShaderFile**  
Uma cadeia de caracteres COM que contém o caminho do arquivo de origem do sombreador de geometria.

**HullShaderFile**  
Uma cadeia de caracteres COM que contém o caminho do arquivo de origem do sombreador de chassi.

**DomainShaderFile**  
Uma cadeia de caracteres COM que contém o caminho do arquivo de origem do sombreador de domínio.

**psRed**  
Saída do sombreador de pixel: valor do componente de cor vermelha.

**psGreen**  
Saída do sombreador de pixel: valor do componente de cor verde.

**psBlue**  
Saída do sombreador de pixel: valor do componente de cor azul

**psAlpha**  
Saída do sombreador de pixel: valor do componente de cor alfa

**LabelPSRed**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor vermelha da saída do sombreador de pixel.

**LabelPSGreen**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde da saída do sombreador de pixel.

**LabelPSBlue**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul da saída do sombreador de pixel.

**LabelPSAlpha**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa da saída do sombreador de pixel.

**pixelKillReason**  
Saída do sombreador de pixel: motivo pelo qual a saída de pixel foi morta.

**pixelOccluded**  
true se o pixel estiver ocluído; caso contrário, false.

**fbRed**  
Framebuffer: valor do componente de cor vermelha do framebuffer antes que a saída do sombreador de pixel seja mesclada.

**fbGreen**  
Framebuffer: valor do componente de cor verde do framebuffer antes que a saída do sombreador de pixel seja mesclada.

**fbBlue**  
Framebuffer: valor do componente de cor azul do framebuffer antes que a saída do sombreador de pixel seja mesclada.

**fbAlpha**  
Framebuffer: valor do componente de cor alfa do framebuffer antes que a saída do sombreador de pixel seja mesclada.

**LabelFBRed**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor vermelha do framebuffer.

**LabelFBGreen**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde do framebuffer.

**LabelFBBlue**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul do framebuffer.

**LabelFBAlpha**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa do framebuffer.

**Topologia**  
A topologia de vértice das chamadas de desenho (lista de triângulos, faixa de triângulo etc.).

**Vértices**  
Uma cadeia de caracteres COM que contém o buffer de vértice começando neste primitivo. O buffer de vértice segue o formato de layout de entrada especificado no estágio do pipeline.

**vtexSize**  
O tamanho de um único vértice em bytes.

**InputLayout**  
Uma cadeia de caracteres COM que contém uma sequência de estruturas InputLayoutStruct associadas à chamada de desenho.

**HResult**  
O DirectX HRESULT. No caso de um problema, isso pode ser usado para exibir o erro.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



