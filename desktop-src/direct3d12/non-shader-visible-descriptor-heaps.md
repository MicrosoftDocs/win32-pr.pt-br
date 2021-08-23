---
title: Heaps de descritores não visíveis do sombreador
description: Alguns heaps de descritores não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparo dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível de sombreador é necessário.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73383659727fea4ef385e56788ce97e18e7976dc5d040a4c1f3a6fc51c3616d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608276"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Heaps de descritores não visíveis do sombreador

Alguns heaps de descritores não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparo dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível de sombreador é necessário.

-   [Exibições não visíveis](#non-visible-views)
-   [Resumo](#summary)
-   [Tópicos relacionados](#related-topics)

## <a name="non-visible-views"></a>Exibições não visíveis

Todos os heaps de descritores, incluindo os heaps de descritores acessíveis ao sombreador descritos anteriormente, podem ser manipulados pelas listas de CPU e/ou comando, dependendo do pool de memória e das propriedades de acesso da CPU que o aplicativo seleciona para um heap de descritor.

Para [heaps de descritor visíveis do sombreador](shader-visible-descriptor-heaps.md), o motivo óbvio para negar o acesso do sombreador a esses heaps de descritor é enquanto eles estão sendo preparados. Em seguida, esses heaps tornam-se visíveis ao sombreador e acessados por meio de tabelas de descritores na execução da lista de comandos. No entanto, não há nenhum requisito para preparar os heaps visíveis do sombreador, eles podem ser preenchidos diretamente.

Outros descritores são vinculados ao pipeline com seu conteúdo registrado diretamente na lista de comandos. Esses descritores só servem para converter os parâmetros de exibição no tempo de registro da lista de comandos. Esses heaps sempre são visíveis sem sombreador e contêm o seguinte.

-   Renderizar exibições de destino (RTVs)
-   Exibições de estêncil de profundidade (DSVs)

As exibições do buffer de índice (IBVs), as exibições de buffer de vértice (VBVs) e as exibições de saída de fluxo (SOVs) são passadas diretamente para métodos de API, não têm tipos de heap específicos.

Após a gravação na lista de comandos (com uma chamada como [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), por exemplo), a memória usada para manter os descritores dessa chamada estará imediatamente disponível para reutilização após a chamada.

Até mesmo as tabelas de descritor têm opções em que um aplicativo pode permitir que a implementação escolha registrar o conteúdo da tabela na gravação da lista de comandos (em vez de desreferenciar o ponteiro da tabela na execução).

## <a name="summary"></a>Resumo



|                   | Sombreador visível, CPU somente gravação                                   | Não-sombreador visível, CPU de leitura/gravação                                       |
|-------------------|------------------------------------|----------------------------------------|
| **CBV, SRV, UAV** | sim                                | sim                                    |
| **CORES**       | sim                                | sim                                    |
| **DAF**           | não                                 | sim                                    |
| **DSV**           | não                                 | sim                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 




