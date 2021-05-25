---
title: Heaps de descritores não visíveis do sombreador
description: Alguns heaps de descritor não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparação dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível para sombreador é necessário.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343451"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Heaps de descritores não visíveis do sombreador

Alguns heaps de descritor não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparação dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível para sombreador é necessário.

-   [Exibições não visíveis](#non-visible-views)
-   [Resumo](#summary)
-   [Tópicos relacionados](#related-topics)

## <a name="non-visible-views"></a>Exibições não visíveis

Todos os heaps de descritor, incluindo os heaps de descritor acessíveis do sombreador descritos anteriormente, podem ser manipulados pelas listas de CPU e/ou comando, dependendo do pool de memória e das propriedades de acesso à CPU que o aplicativo seleciona para um heap de descritor.

Para heaps de [descritor](shader-visible-descriptor-heaps.md)visíveis do sombreador , o motivo óbvio para negar o acesso do sombreador a esses heaps de descritor é quando eles estão sendo analisados. Em seguida, esses heaps ficam visíveis para sombreador e acessados por meio de tabelas de descritor na execução da lista de comandos. No entanto, não há nenhum requisito para o estágio de heaps visíveis para sombreador, eles podem ser populados diretamente.

Outros descritores são vinculados ao pipeline fazendo com que seu conteúdo seja registrado diretamente na lista de comandos. Esses descritores servem apenas para converter os parâmetros de exibição no tempo de registro da lista de comandos. Esses heaps são sempre visíveis sem sombreador e contêm o seguinte.

-   Renderizar exibições de destino (RTVs)
-   DSVs (exibições de estêncil de profundidade)

IBVs (Exibições de Buffer de Índice), VBVs (Exibições de Buffer de VBVs) e SOVs (Exibições de Saída de Fluxo) são passados diretamente para métodos de API, não têm tipos de heap específicos.

Depois de gravar na lista de comandos (com uma chamada como [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), por exemplo), a memória usada para manter os descritores para essa chamada fica imediatamente disponível para rea uso após a chamada.

Até mesmo tabelas de descritor têm opções em que um aplicativo pode permitir que a implementação opte por registrar o conteúdo da tabela na gravação da lista de comandos (em vez de desreferenciar o ponteiro de tabela em execução).

## <a name="summary"></a>Resumo



|                   | Sombreador visível, somente gravação de CPU                                   | Não-sombreador visível, CPU de leitura/gravação                                       |
|-------------------|------------------------------------|----------------------------------------|
| **CBV, SRV, UAV** | sim                                | sim                                    |
| **CORES**       | sim                                | sim                                    |
| **DAF**           | não                                 | sim                                    |
| **DSV**           | não                                 | sim                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 




