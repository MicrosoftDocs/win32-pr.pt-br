---
title: Elementos necessários
description: Elementos necessários
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Capas do Windows Media Player Mobile, elementos
- capas, elementos
- arquivos de definição de capa, elementos
- elementos, arquivos de definição de capa
- elementos, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636027"
---
# <a name="required-elements"></a>Elementos necessários

Você deve fornecer os seguintes elementos em seu arquivo de definição de capa:

-   **Verga.** O cabeçalho principal do arquivo de definição de capa é necessário. Para obter informações de versão do cabeçalho, consulte a tabela na seção [criando um arquivo de definição de aparência](creating-a-skin-definition-file.md) .
-   **Seção de descrição.** A seção descrição é necessária ao criar capas para o Windows Media Player 9 Series para Windows Mobile. Ele deve ser a primeira seção no arquivo de definição de capa e deve especificar valores válidos para dimensões. A especificação de um valor para a orientação é opcional.
-   **Seção bitmaps.** A seção bitmaps é necessária. Além disso, a seção bitmaps deve especificar nomes válidos para arquivos de plano de fundo, desabilitados, enviados por push, região e super Image.
-   **Arquivos de imagem.** Você deve fornecer arquivos de plano de fundo, desabilitados, enviados por push, região e super Image como parte de sua capa. Se você estiver criando capas para o Windows Media Player 10 Mobile ou posterior, não será necessário incluir arquivos de região ou de superimagem.

Se você criar uma capa com apenas imagens definidas, a capa ficará visível, mas não oferecerá nenhuma funcionalidade significativa para o usuário. Se você decidir criar uma capa sem botões, talvez para impedir que o usuário ignore um determinado conteúdo, lembre-se de que ainda pode ser possível mapear a funcionalidade para os botões de hardware no dispositivo.

Os arquivos Thumb são necessários e seu trackbars não pode ser usado sem thumbs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivo de definição de capa**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




