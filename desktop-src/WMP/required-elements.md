---
title: Elementos necessários
description: Elementos necessários
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Windows Media Player Capas móveis, elementos
- skins,elements
- arquivos de definição de capa, elementos
- elementos, arquivos de definição de capa
- elements,Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18433e20c914cdc4b276857f97aab6a692d1d11c811660c73620b09a5b9a0f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746305"
---
# <a name="required-elements"></a>Elementos necessários

Você deve fornecer os seguintes elementos em seu arquivo de definição de capa:

-   **Cabeçalho.** O header do arquivo de definição de capa principal é necessário. Para obter informações sobre a versão do header, consulte a tabela na [seção Criando um arquivo de definição de capa.](creating-a-skin-definition-file.md)
-   **Seção de descrição.** A seção Descrição é necessária ao criar capas para Windows Media Player Série 9 para Windows Mobile. Ele deve ser a primeira seção no arquivo de definição de capa e deve especificar valores válidos para Dimensões. Especificar um valor para Orientação é opcional.
-   **Seção Bitmaps.** A seção Bitmaps é necessária. Além disso, a seção Bitmaps deve especificar nomes válidos para arquivos de Tela de Fundo, Desabilitado, Pressionado, Região e Superimagem.
-   **Arquivos de imagem.** Você deve fornecer arquivos de Tela de Fundo, Desabilitado, Por Pushed, Região e Superimagem como parte da sua capa. Se você estiver criando capas para o Windows Media Player 10 Mobile ou posterior, não será necessário incluir arquivos de Região ou Superimagem.

Se você criar uma capa com apenas imagens definidas, a capa ficará visível, mas não oferecerá nenhuma funcionalidade significativa para o usuário. Se você decidir criar uma capa sem botões, talvez para impedir que o usuário ignorar determinado conteúdo, esteja ciente de que ainda é possível mapear a funcionalidade para os botões de hardware no dispositivo.

Os arquivos thumb são necessários e as barras de faixa não podem ser usadas sem miniaturas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivo de definição de capa**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




