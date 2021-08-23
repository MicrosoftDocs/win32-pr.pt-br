---
description: Nomeando emailslots e colocando mensagens em emailslots.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nomes do Maillot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f96cc5300b3472abe7d6e824266bd0abd0e7b668e38f9f3462eee3cbf3dfb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716896"
---
# <a name="mailslot-names"></a>Nomes do Maillot

Quando um processo cria um maillot, o nome do maillot deve ter o formulário a seguir.

\\\\.\\ nome \\ do \[ caminho \\ \]  do maillot

Um nome maillot requer os seguintes elementos: duas malhas invertida para iniciar o nome, um ponto, uma faixa invertida após o período, a palavra "maillot" e uma faixa invertida à parte final. Os nomes não são sensíveis a minúsculas. Um nome de maillot pode ser precedido por um caminho que consiste nos nomes de um ou mais diretórios, separados por malhas in-back. Por exemplo, se um usuário espera mensagens sobre o assunto de impostos de Bob, Mail e Maillot, o aplicativo maillot do usuário pode permitir que o usuário crie emailslots individuais para cada remetente, conforme mostrado aqui:<dl> \\\\.\\ emailslot \\ impostos \\ bobs \_ comments  
\\\\.\\ emailslot \\ impostos \\ sobre comentários \_  
\\\\.\\ impostos do maillot \\ \\ \_ acionará comentários  
</dl>

Para colocar uma mensagem em um maillot, um processo abre um maillot por nome. Para gravar em um maillot no computador local, um processo pode usar um nome maillot que tenha o mesmo formulário usado para criar um maillot. No entanto, essa situação é relativamente incomum. Com mais frequência, você usaria o seguinte formulário para gravar em um maillot em um computador remoto específico:

\\\\*ComputerName* \\ nome \\ do \[ caminho \\ \]  do maillot

Para colocar uma mensagem em cada maillot no domínio especificado com um determinado nome, use o seguinte formulário:

\\\\*DomainName* \\ nome \\ do \[ caminho \\ \]  do maillot

Para colocar uma mensagem em cada maillot com um determinado nome no domínio primário do sistema, use o seguinte formulário:

\\\\\*\\nome \\ do \[ caminho \\ \]  do maillot

 

 



