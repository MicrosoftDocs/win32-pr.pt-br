---
description: Quando você fornece uma versão prévia, as diretrizes a seguir devem ser seguidas.
title: Diretrizes do manipulador de visualização
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2ed9250e06d2b970ba92bffd10bf80fc6495793b8a9b0237d257b45feb10a99a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719624"
---
# <a name="preview-handler-guidelines"></a>Diretrizes do manipulador de visualização

Quando você fornece uma versão prévia, as diretrizes a seguir devem ser seguidas.

-   Uma versão prévia deve conter interface do usuário mínima– é simplesmente uma versão prévia. Ele deve exibir apenas o conteúdo do arquivo. Ele não deve exibir caixas de diálogo, telas insitivas, barras de ferramentas ou painéis de tarefas. O painel de leitura normalmente será usado em conjunto com a pesquisa para identificar rapidamente um arquivo. Qualquer coisa que desorganizar o painel de leitura ou, de outra forma, prejudicar o conteúdo do arquivo ou causar atrasos na exibição de visualização deve ser evitada.
-   A versão prévia deve permitir que o usuário navegue no documento. O usuário também deve ser capaz de selecionar e copiar texto.
-   A versão prévia não deve ter uso intensivo de memória, deve consumir recursos mínimos e deve ter um tempo de inicialização rápido.
-   Todos os scripts e macros no arquivo que está sendo visualizado devem ser impedidos de serem executados para fins de segurança e privacidade.
-   A versão prévia deve dar suporte a aceleradores de teclado para navegação e seleção, conforme o aplicativo. Ele também deve exibir um menu de contexto quando clicado com o botão direito do mouse.
-   Quando um arquivo é exibido como uma visualização, a versão prévia não deve bloquear o arquivo em si. Um arquivo pode ser visualizado e aberto em seu aplicativo associado ao mesmo tempo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipuladores de visualização e host de visualização do Shell](preview-handlers.md)
</dt> <dt>

[Criando manipuladores de visualização](building-preview-handlers.md)
</dt> </dl>

 

 



