---
description: O conteúdo de textura geralmente é armazenado no formato sRGB.
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: Gama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ede077347d67c1657b86ad09b778625e22fd19a39c8333d7f11fec51be53b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523019"
---
# <a name="gamma-direct3d-9"></a>Gama (Direct3D 9)

O conteúdo de textura geralmente é armazenado no formato sRGB. Tradicionalmente, os pipelines de pixel assumiram as cores como lineares para que as operações de mesclagem fossem executadas em espaço linear. No entanto, como o conteúdo sRGB é corrigido em gama, as operações de mesclagem em espaço linear produzirão resultados incorretos. As placas de vídeo agora podem corrigir esse problema desfazendo a correção gama ao ler qualquer conteúdo sRGB e converter dados de pixel de volta para o formato sRGB ao gravar pixels. Nesse caso, todas as operações dentro do pipeline de pixel são executadas no espaço linear.

## <a name="gamma-correction"></a>Correção gama

O Direct3D 9 pode:

-   Indique se uma textura é gama 2,2 corrigida ou não (sRGB ou não). O driver converterá em um gama linear para operações de mesclagem em tempo detexture ou a amostra irá convertê-la em dados lineares no momento da pesquisa.
-   Indique se o pipeline de pixel deve corrigir o gama de volta para o espaço sRGB ao gravar no destino de renderização.

Todas as outras cores (cor clara, cor do material, cor do vértice, etc.) são consideradas em espaço linear. Os aplicativos podem usar o gama para corrigir as cores gravadas no buffer de quadro usando instruções de sombreador de pixel. A linearidade deve ser aplicada somente aos canais RGB e não ao canal alfa.

Nem todos os formatos de superfície podem ser lineares. Somente os formatos que passam [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com D3DUSAGE de \_ consulta \_ SRGBREAD podem ser lineares. O estado de amostra D3DSAMP \_ SRGBTEXTURE é ignorado para o restante. Espera-se que somente os formatos de textura não assinados ofereçam suporte a essa conversão. Os formatos de textura não assinados incluem apenas os componentes R, G, B e L. Se o canal alfa estiver presente, ele será ignorado. Se os formatos mistos oferecerem suporte à linearidade de sRGB, somente os canais não assinados serão afetados. Idealmente, o hardware deve executar a linearidade antes da filtragem, mas no Direct3D 9, o hardware tem permissão para executar a linearidade após a filtragem.

Nem todos os formatos de superfície podem ser gravados no espaço sRGB. Somente os formatos que passam o [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com o sinalizador de uso D3DUSAGE \_ consulta \_ SRGBWRITE podem ser lineares. O estado de renderização D3DRS \_ SRGBWRITEENABLE é ignorado para o restante. Espera-se que oito bits por canal de formatos RGB não assinados exponham essa capacidade.

O ideal é que o hardware execute as operações de mesclagem do buffer de quadros no espaço linear, mas o hardware tem permissão para executá-lo após o sombreador de pixel, mas antes do misturador de buffer de quadros. Isso significa que as operações de mesclagem do buffer de quadros que ocorrem no espaço sRGB produzirão resultados incorretos. D3DRS \_ SRGBWRITEENABLE é respeitado ao executar uma limpeza do destino de renderização. Para hardware que dá suporte a [vários destinos de renderização (Direct3D 9)](multiple-render-targets.md) ou [texturas de vários elementos (Direct3D 9)](multiple-element-textures.md), somente o primeiro destino de renderização ou elemento é gravado.

### <a name="api-changes"></a>Alterações de API


```
// New sampler state (DWORD)
// If this is nonzero, the texture is linearized on lookup.
D3DSAMP_SRGBTEXTURE       // Default FALSE

// New render state (DWORD)
D3DRS_SRGBWRITEENABLE     // Default FALSE

// New usage flags
D3DUSAGE_QUERY_SRGBWRITE
D3DUSAGE_QUERY_SRGBREAD
```



### <a name="windowed-swap-chains"></a>Cadeias de permuta em janelas

É importante que os aplicativos mantenham os buffers de fundo de suas cadeias de permuta em espaço linear para habilitar as operações de mesclagem corretas. Como a área de trabalho normalmente não está em espaço linear, uma correção gama é necessária antes que o conteúdo do buffer de fundo possa ser apresentado. O aplicativo pode afetar essa correção alocando um buffer adicional e executando sua própria cópia de correção do buffer linear para o buffer de fundo. Isso exige uma cópia extra que poderá ser evitada se o driver executar a correção gama como parte da apresentação blit.

No Direct3D 9, um novo sinalizador, [D3DPRESENT \_ linear \_ Content](d3dpresent.md), está disponível para o [**presente**](/windows/desktop/api) que permite que a apresentação converta implicitamente o espaço linear em sRGB/gama 2,2. Os aplicativos devem especificar esse sinalizador se o formato de BackBuffer for de ponto flutuante de 16 bits para corresponder ao modo de janela presente para o comportamento em tela inteira, desde que \_ \_ a apresentação D3DCAPS3 linear para \_ sRGB \_ seja retornada para os recursos de dispositivo recuperados por meio de [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffer de quadros](frame-buffer.md)
</dt> </dl>

 

 
