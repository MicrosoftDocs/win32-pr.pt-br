---
description: Como os dispositivos de hardware participam do grafo de filtro
ms.assetid: 27e1c097-9bb4-4f9c-b9f9-0d4225c0d290
title: Como os dispositivos de hardware participam do grafo de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68794bbc046e633e9a435b2628a20b8ea8aab174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456379"
---
# <a name="how-hardware-devices-participate-in-the-filter-graph"></a>Como os dispositivos de hardware participam do grafo de filtro

Este artigo descreve como o DirectShow interage com o hardware de áudio e vídeo.

**Filtros de wrapper**

Todos os filtros do DirectShow são componentes de software no modo de usuário. Para um dispositivo de hardware de modo kernel, como um cartão de captura de vídeo, para ingressar em um grafo de filtro do DirectShow, o dispositivo deve ser representado como um filtro de modo de usuário. Essa função é executada por filtros "wrapper" especializados fornecidos com o DirectShow. Esses filtros incluem o filtro de [captura de áudio](audio-capture.md) , o filtro de [captura VFW](vfw-capture-filter.md) , o filtro de [sintonização de TV](tv-tuner-filter.md) , o filtro de áudio de [TV](tv-audio-filter.md) e o filtro [Crossbar de vídeo analógico](analog-video-crossbar-filter.md) . O DirectShow também fornece um filtro chamado KsProxy, que pode representar qualquer tipo de dispositivo de streaming de Windows Driver Model (WDM). Os fornecedores de hardware podem estender o KsProxy para dar suporte à funcionalidade personalizada, fornecendo um *plug-in KsProxy*, que é um objeto com agregado pelo KsProxy.

Os filtros de wrapper expõem interfaces COM que representam os recursos do dispositivo. O aplicativo usa essas interfaces para passar informações de e para o filtro. O filtro converte as chamadas de método COM em chamadas de driver de dispositivo, passa essas informações para o driver no modo kernel e converte o resultado de volta para o aplicativo. Os filtros TV Tuner, áudio de TV, vídeo analógico e KsProxy dão suporte a propriedades de driver personalizadas por meio da interface [**IKsPropertySet**](ikspropertyset.md) . O filtro de captura VFW e o filtro de captura de áudio não são extensíveis dessa maneira.

Para desenvolvedores de aplicativos, os filtros de wrapper permitem que o aplicativo controle dispositivos da mesma forma que controlam qualquer outro filtro do DirectShow. Nenhuma programação especial é necessária; os detalhes da comunicação com o dispositivo de modo kernel são encapsulados dentro do filtro.

**Vídeo para dispositivos Windows**

O filtro de captura VFW dá suporte aos cartões de captura de vídeo para Windows (VfW) anteriores. Quando um cartão VfW está presente no sistema de destino, ele pode ser descoberto e adicionado ao gráfico de filtro usando o [enumerador de dispositivo do sistema](system-device-enumerator.md)DirectShow. Para obter detalhes, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).

**Dispositivos de captura e mixagem de áudio (cartões de som)**

Placas de som mais novas têm conectores de entrada para microfones e outros tipos de dispositivos. Normalmente, esses cartões também têm recursos de mixagem integrada para controlar o volume, os agudos e os graves de cada entrada individual. No DirectShow, as entradas e o mixer da placa de som são encapsulados pelo filtro de captura de áudio. Cada placa de som pode ser descoberta com o enumerador de dispositivo do sistema. Para exibir as placas de som em seu sistema, execute GraphEdit e selecione na categoria fontes de captura de áudio. Cada filtro nessa categoria é uma instância separada do filtro de captura de áudio. (Consulte [usando GraphEdit](using-graphedit.md).)

**Dispositivos de streaming WDM**

Os decodificadores de hardware mais recentes e os cartões de captura estão em conformidade com a especificação de Windows Driver Model (WDM). Esses dispositivos têm maior funcionalidade do que os dispositivos VfW. Os cartões de captura de vídeo WDM podem dar suporte a recursos que não estão disponíveis em VfW, incluindo a enumeração de formatos de captura, o controle programático de parâmetros de vídeo, como matiz e brilho, seleção de entrada programática e suporte a sintonizador de TV.

Para oferecer suporte a dispositivos de streaming WDM, o DirectShow fornece o filtro KsProxy (ksproxy.ax). KsProxy foi chamado de "filtro de faca do exército suíço", pois ele faz muitas coisas diferentes. O número de Pins no filtro e o número de interfaces COM expostas pelo filtro dependem dos recursos do driver subjacente. KsProxy não aparece no grafo de filtro sob o nome "KsProxy". Ele sempre usa o nome amigável do dispositivo, que é encontrado no registro. Para exibir os dispositivos WDM no seu sistema, execute GraphEdit e selecione nas categorias de streaming WDM. Mesmo que você tenha apenas uma placa WDM em seu sistema, esse cartão pode conter mais de um dispositivo. Cada dispositivo é representado como um filtro separado, e cada um desses filtros é realmente KsProxy.

Um aplicativo usa o enumerador de dispositivo do sistema para localizar monikers de dispositivo WDM no sistema. KsProxy é instanciado chamando **BindToObject** no moniker. Como KsProxy pode representar todos os tipos de dispositivos WDM, ele deve consultar o driver para determinar a quais conjuntos de propriedades o driver dá suporte. Os conjuntos de propriedades são coleções de estruturas de dados usadas por drivers WDM e também por alguns filtros de modo de usuário, como decodificadores de software MPEG-2. O KsProxy se configura para expor as interfaces COM que correspondem a esses conjuntos de propriedades. KsProxy converte as chamadas de método COM em conjuntos de propriedades e as envia para o driver. Os fornecedores de hardware podem estender o KsProxy fornecendo plug-ins, que são interfaces específicas do fornecedor que expõem os recursos especiais de um dispositivo. Todos esses detalhes estão ocultos do aplicativo. O aplicativo controla o dispositivo por meio do KsProxy, da mesma forma que qualquer outro filtro do DirectShow.

**Streaming de kernel**

Os dispositivos WDM dão suporte ao streaming de kernel, no qual os dados são transmitidos inteiramente no modo kernel sem mudar para o modo de usuário. Alternar entre o modo kernel e o modo de usuário é computacionalmente caro; o streaming de kernel permite taxas de bits altas sem sobrecarregar a CPU do host. Os filtros baseados em WDM podem usar o streaming de kernel para transmitir dados de multimídia diretamente de um dispositivo de hardware para outro, seja no mesmo cartão ou em um cartão diferente, sem copiar os dados para a memória principal do sistema.

Do ponto de vista de um aplicativo, ele aparece como se os dados se movem de um filtro de modo de usuário para o próximo. Na realidade, os dados podem nunca passar para o modo de usuário, mas podem ser transmitidos diretamente de um dispositivo de modo kernel para outro até que ele seja renderizado na placa gráfica de vídeo. Alguns cenários, como a captura de um arquivo, exigem que os dados passem do modo kernel para o modo de usuário em algum momento. No entanto, essa opção não exige necessariamente que os dados sejam copiados para um novo local na memória.

Os desenvolvedores de aplicativos geralmente não precisam se preocupar com os detalhes do streaming de kernel, exceto como informações de segundo plano. Consulte o Microsoft DDK para obter informações mais detalhadas sobre WDM, kernel streaming, KsProxy e tópicos relacionados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O gráfico de filtro e seus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



