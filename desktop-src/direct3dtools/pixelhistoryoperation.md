---
description: Representa informações sobre o histórico de pixel.
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
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105771538"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>Estrutura PixelHistoryOperation

Representa informações sobre o histórico de pixel.

## <a name="syntax"></a>Sintaxe


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Membros

**Eid**  
A ID do evento de gráficos associado a esta operação.

**PCP**  
Chamadas empacotadas associadas a esta operação.

**renderTargetPtr**  
O destino de renderização originalmente associado (dentro do aplicativo capturado) com esta operação.

**iPrim**  
O índice da primitiva real associada à sua operação.

**numPrims**  
O número total de primitivos associados a esta operação.

**numVertsPerPrim**  
O número de vértices por primitivo.

**iInstance**  
Ao renderizar instâncias, o número de instância da instância real associada a essa operação.

**iInstanceCount**  
Ao renderizar instâncias, o número total de instâncias associadas a essa operação.

**bAssemblerStageGeneratesInstanceID**  
true se o montador de entrada gerar IDs de instância; caso contrário, false.

**sinalizadores**  
Uma combinação de valores PIXELHISTORYFLAGS. Para obter mais informações, consulte a enumeração PIXELHISTORYFLAGS.

**pVSFile**  
Um FILEPTR para o fluxo de bytes do sombreador de pixel. Isso é passado de volta para depurar.

**pGSFile**  
Um FILEPTR para o fluxo de bytes do sombreador de geometria. Isso é passado de volta para depurar.

**pPSFile**  
Um FILEPTR para o fluxo de bytes do sombreador de pixel. Isso é passado de volta para depurar.

**pHSFile**  
Um FILEPTR para o fluxo de bytes do sombreador envoltória. Isso é passado de volta para depurar.

**pDSFile**  
Um FILEPTR para o fluxo de bytes do sombreador de domínio. Isso é passado de volta para depurar.

**pCSFile**  
Um FILEPTR para o fluxo de bytes do sombreador de computação. Isso é passado de volta para depurar.

**VertexShaderFile**  
Uma cadeia de caracteres COM que contém o FilePath do arquivo de origem do sombreador de vértice.

**PixelShaderFile**  
Uma cadeia de caracteres COM que contém o caminho de arquivo de origem do sombreador de pixel.

**GeometryShaderFile**  
Uma cadeia de caracteres COM que contém o FilePath do arquivo de origem do sombreador de geometria.

**HullShaderFile**  
Uma cadeia de caracteres COM que contém o FilePath do arquivo de origem do sombreador envoltória.

**DomainShaderFile**  
Uma cadeia de caracteres COM que contém o caminho de arquivo de origem do sombreador de domínio.

**psRed**  
Saída do sombreador de pixel: valor do componente de cor vermelha.

**psGreen**  
Saída do sombreador de pixel: valor do componente de cor verde.

**psBlue**  
Saída do sombreador de pixel: valor do componente de cor azul

**psAlpha**  
Saída do sombreador de pixel: valor do componente de cor alfa

**LabelPSRed**  
Uma cadeia COM que contém o nome do rótulo associado ao componente de cor vermelha da saída do sombreador de pixel.

**LabelPSGreen**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde da saída do sombreador de pixel.

**LabelPSBlue**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul da saída do sombreador de pixel.

**LabelPSAlpha**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa da saída do sombreador de pixel.

**pixelKillReason**  
Saída do sombreador de pixel: motivo pelo qual a saída de pixel foi eliminada.

**pixelOccluded**  
true se o pixel for obstruído; caso contrário, false.

**fbRed**  
Framebuffer: valor do componente de cor vermelha de framebuffer antes da saída do sombreador de pixel ser mesclada.

**fbGreen**  
Framebuffer: valor do componente de cor verde de framebuffer antes da saída do sombreador de pixel ser mesclada.

**fbBlue**  
Framebuffer: valor do componente de cor azul de framebuffer antes da saída do sombreador de pixel ser mesclada.

**fbAlpha**  
Framebuffer: valor do componente de cor alfa de framebuffer antes da saída do sombreador de pixel ser mesclada.

**LabelFBRed**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor vermelha do framebuffer.

**LabelFBGreen**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde do framebuffer.

**LabelFBBlue**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul do framebuffer.

**LabelFBAlpha**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa do framebuffer.

**visualização**  
A topologia de vértice das chamadas de desenho (lista de triângulo, faixa de triângulo, etc.).

**vértices**  
Uma cadeia de caracteres COM que contém o buffer de vértice começando nesse primitivo. O buffer de vértice segue o formato de layout de entrada especificado no estágio do pipeline.

**vertexSize**  
O tamanho de um único vértice em bytes.

**InputLayout**  
Uma cadeia de caracteres COM que contém uma sequência de estruturas InputLayoutStruct associadas à chamada de desenho.

**Resultado**  
O DirectX HRESULT. No caso de um problema, isso pode ser usado para exibir o erro.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



