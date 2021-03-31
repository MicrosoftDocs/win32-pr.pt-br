---
title: Fornecendo uma interface do usuário
description: Fornecendo uma interface do usuário
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades
- plug-ins, páginas de propriedades
- plug-ins de processamento de sinal digital, páginas de propriedades
- Plug-ins do DSP, páginas de propriedades
- plug-ins de processamento de sinal digital, interface do usuário
- Plug-ins do DSP, interface do usuário
- páginas de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160221"
---
# <a name="providing-a-user-interface"></a>Fornecendo uma interface do usuário

Plug-ins do DSP podem fornecer uma página de propriedades para criar uma interface do usuário. Para fazer isso, o plug-in deve incluir um objeto de página de propriedades que fornece uma implementação de uma interface **IPropertyPage** . O objeto de plug-in DSP deve implementar **ISpecifyPropertyPages:: GetPages**, que permite que o Windows Media Player Localize e identifique a página de propriedades correta para o plug-in.

**Exibindo um gráfico de status**

Plug-ins DSP podem exibir um elemento gráfico pequeno ou uma série de gráficos, na área status do Windows Media Player, para notificar o usuário de que um plug-in está ativo. Para dar suporte a esse recurso, o plug-in deve implementar a interface **IPropertyBag** . O Windows Media Player chama **IPropertyBag:: Read**, fornecendo um ponteiro para o nome da propriedade solicitada "iconstreams", que diferencia maiúsculas de minúsculas e um ponteiro para uma estrutura **variante** que recebe os dados para o gráfico. O plug-in cria um objeto **IStream** (ou um SafeArray de objetos **IStream** se houver vários gráficos) e, em seguida, carrega os dados gráficos, incluindo informações de cabeçalho, para o fluxo e, em seguida, retorna um ponteiro para o objeto **IStream** usando o membro **punkVal** da estrutura **Variant** . Se o plug-in fornecer apenas um gráfico, ele especificará o membro **VT** da estrutura **Variant** como VT \_ desconhecido. Se o plug-in fornecer vários objetos de **IStream** gráfico usando um SafeArray, ele especificará o membro **VT** da estrutura **Variant** como a \_ matriz VT.

Os gráficos podem ser armazenados em uma variedade de formatos de arquivo, incluindo:

**BMP**

As imagens de bitmap do Microsoft Windows são descompactadas.

**JPEG**

Formato de imagem compactado normalmente usado para páginas da Web. Os arquivos de formato JPEG geralmente têm extensões de nome de arquivo. jpg.

**GIF**

Formato de imagem compactado normalmente usado para páginas da Web.

**PNG**

Formato de imagem compactado normalmente usado para páginas da Web.

As dimensões máximas para gráficos de plug-in DSP têm 38 pixels de largura e 14 pixels de altura.

O fluxo de bytes de **IStream** que contém o gráfico de status deve incluir informações de cabeçalho. Sem informações de cabeçalho, o Windows Media Player não pode identificar corretamente o tipo de elemento gráfico e, portanto, não carregará a imagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




