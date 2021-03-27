---
description: Quando você fornece uma visualização, as diretrizes a seguir devem ser seguidas.
title: Diretrizes do Gerenciador de visualização
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828906"
---
# <a name="preview-handler-guidelines"></a>Diretrizes do Gerenciador de visualização

Quando você fornece uma visualização, as diretrizes a seguir devem ser seguidas.

-   Uma visualização deve conter a interface do usuário mínima — é simplesmente uma visualização. Ele deve exibir apenas o conteúdo do arquivo. Ele não deve exibir caixas de diálogo, telas de abertura, barras de ferramentas ou painéis de tarefas. O painel de leitura normalmente será usado em conjunto com a pesquisa para identificar rapidamente um arquivo. Tudo que obstrui o painel de leitura ou, de outra forma, reduz o conteúdo do arquivo ou causa atrasos na exibição da visualização.
-   A visualização deve permitir que o usuário navegue no documento. O usuário também deve ser capaz de selecionar e copiar o texto.
-   A visualização não deve ter uso intensivo de memória, deve consumir recursos mínimos e deve ter um tempo de inicialização rápido.
-   Todo script e macros no arquivo que está sendo visualizado devem ser impedidos de serem executados para fins de segurança e privacidade.
-   A visualização deve dar suporte a aceleradores de teclado para navegação e seleção, conforme suportado pelo aplicativo. Ele também deve exibir um menu de contexto quando clicado com o botão direito do mouse.
-   Quando um arquivo é exibido como uma visualização, a visualização não deve bloquear o próprio arquivo. Um arquivo pode ser visualizado e aberto em seu aplicativo associado ao mesmo tempo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciadores de visualização e host de visualização do Shell](preview-handlers.md)
</dt> <dt>

[Criando gerenciadores de visualização](building-preview-handlers.md)
</dt> </dl>

 

 



