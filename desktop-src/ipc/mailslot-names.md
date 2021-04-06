---
description: Nome de processadores e colocação de mensagens em processadores.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nomes de processador de processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646696"
---
# <a name="mailslot-names"></a>Nomes de processador de processadores

Quando um processo cria um processador de itens, o nome do processador de processadores deve ter o seguinte formato.

\\\\.\\ nome do \\ \[ *caminho* \\ \]  do processador de processadores

Um nome de processador de texto requer os seguintes elementos: duas barras invertidas para iniciar o nome, um ponto, uma barra invertida após o período, a palavra "processador de texto" e uma barra invertida à direita. Os nomes não diferenciam maiúsculas de minúsculas. Um nome de processador de itens pode ser precedido por um caminho que consiste nos nomes de um ou mais diretórios, separados por barras invertidas. Por exemplo, se um usuário espera mensagens no assunto de impostos de Bob, Pete e Suzana, o aplicativo do processador de mensagens do usuário pode permitir que o usuário crie processadores de mensagens individuais para cada remetente, como mostrado aqui:<dl> \\\\.\\ \\ \\ comentários bobs de taxas de processador de processadores \_  
\\\\.\\ os impostos do processador de \\ taxas \\ petem \_ comentários  
\\\\.\\ \\ \\ comentários sues de taxas de processador de processadores \_  
</dl>

Para colocar uma mensagem em um processador de mensagens, um processo abre um processador por nome. Para gravar em um processador de processadores no computador local, um processo pode usar um nome de processador de processadores que tenha a mesma forma usada para criar um processador de processadores. No entanto, essa situação é relativamente incomum. Com mais frequência, você usaria o seguinte formulário para gravar em um processador de processadores em um computador remoto específico:

\\\\*ComputerName* \\ nome do \\ \[ *caminho* \\ \]  do processador de processadores

Para colocar uma mensagem em cada processador de mensagens no domínio especificado com um determinado nome, use o seguinte formato:

\\\\*Nome_do_domínio* \\ nome do \\ \[ *caminho* \\ \]  do processador de processadores

Para colocar uma mensagem em cada processador de mensagens com um nome específico no domínio primário do sistema, use o seguinte formato:

\\\\\*\\nome do \\ \[ *caminho* \\ \]  do processador de processadores

 

 



