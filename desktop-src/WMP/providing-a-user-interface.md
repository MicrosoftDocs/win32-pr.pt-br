---
title: Fornecendo uma interface do usuário
description: Fornecendo uma interface do usuário
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- plug-ins Windows Media Player, páginas de propriedades
- plug-ins, páginas de propriedades
- plug-ins de processamento de sinal digital, páginas de propriedades
- Plug-ins do DSP, páginas de propriedades
- plug-ins de processamento de sinal digital, interface do usuário
- Plug-ins do DSP, interface do usuário
- páginas de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb80525fa4b32845608eebb32752871a038aa6e01088baeebce5bc5f8c84b4bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746734"
---
# <a name="providing-a-user-interface"></a>Fornecendo uma interface do usuário

Plug-ins do DSP podem fornecer uma página de propriedades para criar uma interface do usuário. Para fazer isso, o plug-in deve incluir um objeto de página de propriedades que fornece uma implementação de uma interface **IPropertyPage** . o objeto de plug-in DSP deve implementar **ISpecifyPropertyPages:: getpages**, que permite ao Windows Media Player localizar e identificar a página de propriedades correta para o plug-in.

**Exibindo um gráfico de status**

plug-ins DSP podem exibir um elemento gráfico pequeno ou uma série de gráficos, na área status Windows Media Player para notificar o usuário de que um plug-in está ativo. Para dar suporte a esse recurso, o plug-in deve implementar a interface **IPropertyBag** . Windows Media Player chama **IPropertyBag:: Read**, fornecendo um ponteiro para o nome da propriedade solicitada "IconStreams", que diferencia maiúsculas de minúsculas e um ponteiro para uma estrutura **VARIANT** que recebe os dados para o gráfico. O plug-in cria um objeto **IStream** (ou um SafeArray de objetos **IStream** se houver vários gráficos) e, em seguida, carrega os dados gráficos, incluindo informações de cabeçalho, para o fluxo e, em seguida, retorna um ponteiro para o objeto **IStream** usando o membro **punkVal** da estrutura **Variant** . Se o plug-in fornecer apenas um gráfico, ele especificará o membro **VT** da estrutura **Variant** como VT \_ desconhecido. Se o plug-in fornecer vários objetos de **IStream** gráfico usando um SafeArray, ele especificará o membro **VT** da estrutura **Variant** como a \_ matriz VT.

Os gráficos podem ser armazenados em uma variedade de formatos de arquivo, incluindo:

**BMP**

as imagens de Bitmap do Microsoft Windows são descompactadas.

**JPEG**

Formato de imagem compactado normalmente usado para páginas da Web. Os arquivos de formato JPEG geralmente têm .jpg extensões de nome de arquivo.

**Gifs**

Formato de imagem compactado normalmente usado para páginas da Web.

**PNG**

Formato de imagem compactado normalmente usado para páginas da Web.

As dimensões máximas para gráficos de plug-in DSP têm 38 pixels de largura e 14 pixels de altura.

O fluxo de bytes de **IStream** que contém o gráfico de status deve incluir informações de cabeçalho. sem informações de cabeçalho, Windows Media Player não pode identificar corretamente o tipo de elemento gráfico e, portanto, não carregará a imagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




