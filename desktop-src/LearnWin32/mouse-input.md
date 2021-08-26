---
title: Entrada do mouse (Introdução com Win32 e C++)
description: Entrada do mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ff39b798b1438bca33bc9ab9b077333dca351e32a5945b939beba2c13f5894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897036"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Entrada do mouse (Introdução com Win32 e C++)

Windows dá suporte a mouses com até cinco botões: left, middle e right, além de dois botões adicionais chamados XBUTTON1 e XBUTTON2.

![uma ilustração que mostra os botões left (1), right (2), middle (3) e xbutton1 (4).](images/mouse.png)

A maioria dos Windows tem pelo menos os botões esquerdo e direito. O botão esquerdo do mouse é usado para apontar, selecionar, arrastar e assim por diante. O botão direito do mouse normalmente exibe um menu de contexto. Alguns mouses têm uma roda de rolagem localizada entre os botões esquerdo e direito. Dependendo do mouse, a roda de rolagem também pode ser clicável, tornando-a o botão central.

Os botões XBUTTON1 e XBUTTON2 geralmente estão localizados nos lados do mouse, próximos à base. Esses botões extras não estão presentes em todos os mouses. Se presente, os botões XBUTTON1 e XBUTTON2 geralmente são mapeados para uma função de aplicativo, como navegação para frente e para trás em um navegador da Web.

Os usuários com a esquerda costumam achar mais confortável trocar as funções dos botões esquerdo e direito, usando o botão direito como o ponteiro e o botão esquerdo para mostrar o menu de contexto. Por esse motivo, a documentação Windows  ajuda usa os termos botão primário e botão secundário *,* que se referem à função lógica em vez do posicionamento físico. Na configuração padrão (com a mão direita), o botão esquerdo é o botão primário e a direita é o botão secundário. No entanto, os termos *clicar com o botão direito do mouse* e clicar com o *botão* esquerdo do mouse referem-se a ações lógicas. *Clicar com o botão* direito do mouse significa clicar no botão primário, independentemente de o botão estar fisicamente no lado direito ou esquerdo do mouse.

Independentemente de como o usuário configura o mouse, Windows automaticamente converte mensagens do mouse para que elas sejam consistentes. O usuário pode trocar os botões primário e secundário no meio do uso do programa e não afetará o comportamento do programa.

A documentação do MSDN usa os termos *botão direito* e *botão esquerdo* para significar *o botão* primário *e secundário.* Essa terminologia é consistente com os nomes das mensagens da janela para entrada do mouse. Lembre-se apenas de que os botões físicos esquerdo e direito podem ser trocados.

## <a name="next"></a>Avançar

[Respondendo a cliques do mouse](mouse-clicks.md)

 

 




