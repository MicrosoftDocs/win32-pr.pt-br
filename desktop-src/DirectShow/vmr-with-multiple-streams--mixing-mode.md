---
description: VMR com vários fluxos (modo de combinação)
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: VMR com vários fluxos (modo de combinação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21a954b0ad78afbceabf0fde493f920961b90dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757280"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>VMR com vários fluxos (modo de combinação)

O VMR pode renderizar vários fluxos de entrada. Nessa configuração, chamada de modo de combinação, o VMR carrega o mixer e o compositor para executar a mistura e a mesclagem antes da renderização. O modo de combinação pode ser usado enquanto o VMR está no modo de janela ou sem janela.

O modo de combinação requer que o driver de gráficos dê suporte aos \_ sinalizadores de recurso DDCAPS BLTFOURCC e DDCAPS \_ BLTSTRETCH (conversão de espaço de cor e transferência de disco de ampliação, respectivamente). Quase todos os novos drivers gráficos têm esses recursos. Além disso, o driver deve dar suporte à criação de destinos de renderização do Direct3D para a profundidade de pixels de exibição atual. Alguns dispositivos não dão suporte a operações de Direct3D quando a exibição é definida como 24 bits por pixel. Para obter mais informações, consulte a documentação do SDK de gráficos do DirectX.

> [!Note]  
> Quando o VMR combina vários fluxos de vídeo, o grafo de filtro não busca corretamente. Se você precisar buscar vários fluxos de vídeo, deverá criar gráficos de filtro separados que compartilhem o mesmo objeto de apresentador de alocador personalizado.

 

**Configurando o VMR-7 para vários fluxos**

Para renderizar vários fluxos de entrada com o VMR-7, faça o seguinte:

1.  Antes de conectar qualquer um dos Pins de entrada do VMR, chame o método [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) com o número de fluxos. Isso faz com que o VMR carregue o mixer e o compositor e crie o número especificado de Pins de entrada.
2.  Chame [**IVMRFilterConfig:: SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) para especificar várias preferências de renderização.
3.  Conecte os Pins aos filtros upstream. A maneira mais fácil de fazer isso é chamar [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para cada fluxo de entrada. Se o pino de saída no filtro upstream (geralmente um decodificador) e o pino de entrada no VMR não puderem concordar em uma conexão, uma nova instância do VMR com as configurações padrão será criada. Isso resultará em uma nova janela com "ActiveMovie" na barra de título. Para evitar que isso aconteça, o aplicativo sempre deve verificar se a instância correta do VMR está sendo usada chamando um método como [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto). Outra opção é adicionar o filtro de origem e, em seguida, conectar os Pins usando **IGraphBuilder:: Connect**.
4.  Use a interface [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) no VMR para controlar os parâmetros de cada fluxo, como o valor alfa, a ordenação Z e o retângulo de saída.
5.  Execute o gráfico de filtro.

**Configurando o VMR-9 para vários fluxos**

Por padrão, o VMR-9 cria quatro pinos de entrada. Se você quiser misturar mais de quatro fluxos de vídeo, chame [**IVMRFilterConfig9:: SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) antes de conectar qualquer pino de entrada. Use a interface [**IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) para definir os parâmetros de fluxo, como alfa, ordem Z e posição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de mixagem do VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



