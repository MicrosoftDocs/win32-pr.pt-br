---
title: Entrada do mouse (introdução ao Win32 e ao C++)
description: Entrada do mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105810161"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Entrada do mouse (introdução ao Win32 e ao C++)

O Windows dá suporte a mouses com até cinco botões: esquerdo, meio e direito, além de dois botões adicionais chamados XBUTTON1 e XBUTTON2.

![uma ilustração que mostra os botões esquerdo (1), direito (2), médio (3) e XButton1 (4).](images/mouse.png)

A maioria dos mouses para Windows tem pelo menos os botões esquerdo e direito. O botão esquerdo do mouse é usado para apontar, selecionar, arrastar e assim por diante. O botão direito do mouse normalmente exibe um menu de contexto. Alguns mouses têm uma roda de rolagem localizada entre os botões esquerdo e direito. Dependendo do mouse, a roda de rolagem também pode ser clicável, tornando-o o botão do meio.

Os botões XBUTTON1 e XBUTTON2 geralmente estão localizados nos lados do mouse, perto da base. Esses botões extras não estão presentes em todos os mouses. Se houver, os botões XBUTTON1 e XBUTTON2 geralmente são mapeados para uma função de aplicativo, como navegação para frente e para trás em um navegador da Web.

Os usuários da mão esquerda geralmente acham mais confortável trocar as funções dos botões esquerdo e direito — usando o botão direito como ponteiro e o botão esquerdo para mostrar o menu de contexto. Por esse motivo, a documentação de ajuda do Windows usa o botão de termos *primário* e o *botão secundário*, que se referem à função lógica em vez do posicionamento físico. Na configuração padrão (canhoto), o botão esquerdo é o botão principal e a direita é o botão secundário. No entanto, os termos clique com o *botão direito do mouse* e *esquerdo clique em* consulte ações lógicas. *Clicando com o botão direito do mouse* significa clicar no botão primário, se esse botão está fisicamente no lado direito ou esquerdo do mouse.

Independentemente de como o usuário configura o mouse, o Windows converte automaticamente as mensagens do mouse para que elas sejam consistentes. O usuário pode trocar os botões primário e secundário no meio do uso do programa e não afetará a forma como o seu programa se comporta.

A documentação do MSDN usa o botão *direito do mouse* e o *botão esquerdo* para significar o botão *primário* e o *secundário* . Essa terminologia é consistente com os nomes das mensagens de janela para entrada do mouse. Apenas lembre-se de que os botões físico esquerdo e direito podem ser trocados.

## <a name="next"></a>Avançar

[Respondendo a cliques do mouse](mouse-clicks.md)

 

 




