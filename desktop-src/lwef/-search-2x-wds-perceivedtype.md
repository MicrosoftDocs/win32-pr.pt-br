---
title: tipos observados (recursos de ambiente de Windows herdados)
description: Percebidotype é uma propriedade que classifica um item no índice.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de2baa37a46a9bd78e6e8a7ad94806dffe3a918046253bb09d4dab6090838b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610826"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>tipos observados (recursos de ambiente de Windows herdados)

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use [Windows pesquisa](../search/-search-3x-wds-overview.md) em vez disso.

`PerceivedType` é uma propriedade que classifica um item no índice. Essa classificação é diferente da classificação "Kind" usada pela sintaxe de [consulta avançada](-search-2x-wds-aqsreference.md) , mas, da mesma forma, permite que os usuários refinam seus resultados de pesquisa. O tipo AQS permite que os usuários limitem sua consulta de pesquisa enquanto a propriedade Percebidatype permite que os usuários filtrem seu conjunto de resultados.

## <a name="types"></a>Tipos

Use a propriedade Percebidotype para classificar o tipo de arquivo para que os usuários possam filtrar os resultados da pesquisa por tipo. A saída deve ser uma das seguintes cadeias de caracteres:

-   contact
-   comunicações
-   comunicações/email
-   comunicações/calendário
-   comunicações/tarefa
-   comunicações/mensagens instantâneas
-   documento
-   documento/anotação
-   documento/texto
-   documento/planilha
-   documento/apresentação
-   music
-   images
-   imagens/imagem
-   imagens/vídeo
-   folder
-   programa

Por exemplo, quando você deseja criar um suplemento de filtro para um novo tipo de arquivo de imagem, você precisa implementar o seguinte na interface do [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter):

-   **GetChunk** para retornar um FULLPROPSPEC que inclui: D5CDD505-2E9C-101B-9397-08002B2CF9AE/percebidotype
-   **GetValue** para retornar um PROPVARIANT que inclui: VT \_ LPWSTR = "images/Picture"

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Desenvolvendo suplementos do IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

[Sintaxe de consulta avançada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Esquematable](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
