---
description: As anotações e a semântica padrão (DXSAS) fornecem um método de uso de sombreadores de forma padrão que permite que os sombreadores sejam usados com ferramentas, aplicativos e mecanismos de jogos.
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: Referência de semântica e anotações padrão do DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c989f4aed7c01c62d6133e01fe035223b74c8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456618"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>Referência de semântica e anotações padrão do DirectX

As anotações e a semântica padrão (DXSAS) fornecem um método de uso de sombreadores de forma padrão que permite que os sombreadores sejam usados com ferramentas, aplicativos e mecanismos de jogos. DXSAS define um conjunto de semânticas e anotações que são anexadas aos valores de aplicativo host e parâmetros de efeito para fins de compartilhamento de efeitos. Para que essas anotações e semânticas sejam úteis, elas devem ser implementadas no aplicativo host e no arquivo de efeito. Este documento descreve o padrão DXSAS, que aproveita o poder da estrutura de efeito do DirectX para permitir que aplicativos e ferramentas de host compartilhem os efeitos do DirectX (arquivos. FX) programaticamente, bem como o design de interação com a interface do usuário.

## <a name="background-information"></a>Informações gerais

As anotações e as semânticas padrão são projetadas para ligar os parâmetros de efeito e de arquivo X para hospedar valores de aplicativo. A estrutura de efeito D3DX (ou os efeitos) encapsula o estado de renderização. Ao encapsular o estado de renderização (incluindo o estado de vértice, de textura e de processamento de pixel) em um efeito, você pode criar uma biblioteca de efeitos que abrangem uma ampla gama de opções de renderização. Isso pode incluir opções como a renderização em diferentes tipos de hardware ou a renderização com mesclagem única ou múltipla. Para obter mais informações sobre a estrutura de efeito, consulte [referência de efeito](dx9-graphics-reference-effects.md). O DXSAS se baseia nessa estrutura, permitindo uma experiência mais consistente para os desenvolvedores. Depois que a configuração de renderização é encapsulada em um efeito, o padrão DXSAS permite que o desenvolvedor de efeito exponha a intenção dos parâmetros de efeito por meio de anotações. Essas anotações podem ser lidas por qualquer aplicativo host ou ferramenta (não apenas aquela que foi projetada para usar o efeito) que é compatível com o padrão entenderá como usar o efeito da maneira que foi projetada.

Padronizar o conjunto de semânticas de efeito e anotações que hospedam aplicativos dão suporte a permitir que os autores de efeito criem efeitos que podem ser usados em vários projetos e, portanto, promovem uma comunidade maior de usuários de efeito. O padrão DXSAS torna os arquivos legíveis para os desenvolvedores, intercambiáveis entre ferramentas e permite que os desenvolvedores aproveitem as ferramentas de terceiros para efeitos de criação para seus pipelines.

Este documento descreve o padrão DXSAS que usa anotações para expressar os parâmetros de intenção de efeito, bem como definir uma coleção de valores de aplicativo host que hospedam aplicativos que concordam em tornar disponíveis para um efeito.

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>Efeitos de criação com anotações padrão e semântica

Como você pode ver no diagrama a seguir, o padrão DXSAS requer anotações em um arquivo de efeito, bem como um aplicativo host que segue as diretrizes descritas aqui para trabalhar com o arquivo.

![diagrama do padrão dxsas para aplicativos host e arquivos de efeito](images/sas-2.png)

O aplicativo host deve implementar a lógica da interface do usuário e o ambiente de host. Para implementar efeitos em conformidade com o DXSAS, leia os seguintes tópicos:

-   O [parâmetro global](global-parameter.md) define informações pertinentes ao efeito, como a versão ou o autor do efeito.
-   A [vinculação de dados](data-binding.md) define a coleção de parâmetros (bem como seu tipo e estrutura) que pode ser usada por um efeito que pode ser definido pelo aplicativo host exposto a efeitos.
-   Para associar um controle de interface de usuário a um parâmetro de efeito, use uma [anotação de IU](ui-annotation.md). Essas anotações incluem: [SasUiMax](ui-annotation.md), [SasUiMin](ui-annotation.md), [SasUiSteps](ui-annotation.md), [SasUiStepsPower](ui-annotation.md)e [SasUiStride](ui-annotation.md).
-   Para inicializar um parâmetro de efeito com dados contidos em um arquivo externo, use uma [anotação de inicialização de parâmetro](parameter-initialization-annotation.md).
-   Quando os dados são transferidos entre o aplicativo host e um efeito (ou vice-versa), ocorrerá a [conversão e converter](casting-and-conversion.md) quando os tipos não corresponderem exatamente. Esta seção especifica como os dados são gravados quando os tipos de origem e destino são diferentes. Além disso, use [ParameterValueModifiers](casting-and-conversion.md) para modificar como o aplicativo host deve interpretar os dados lidos do parâmetro Effect. Essas anotações incluem: [SasNormalize](casting-and-conversion.md) e [SasUnits](casting-and-conversion.md).

## <a name="case-sensitivity"></a>Diferenciação de maiúsculas e minúsculas

Todos os identificadores, semânticas e valores de anotação não diferenciam maiúsculas de minúsculas. Os nomes das anotações (não valores) diferenciam maiúsculas de minúsculas. Os nomes das anotações são reconhecidos pelo sistema de efeitos D3DX e, portanto, os nomes de anotações SAS também são.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de efeito](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



