---
title: Sobre caixas de diálogo de tarefa
description: Uma caixa de diálogo de tarefa é uma caixa de diálogo que pode ser usada para exibir informações e receber entradas simples do usuário.
ms.assetid: vs|controls|~\controls\toolbar\taskdialogsoverview.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2367e3cadff68f10af9d883d4ed7959e4e862a6f406a83361ea2f40b2f69c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061416"
---
# <a name="about-task-dialogs"></a>Sobre caixas de diálogo de tarefa

Uma caixa de diálogo de tarefa é uma caixa de diálogo que pode ser usada para exibir informações e receber entradas simples do usuário. Como uma caixa de mensagem, ela é formatada pelo sistema operacional de acordo com os parâmetros definidos. No entanto, uma caixa de diálogo de tarefa tem muito mais recursos do que uma caixa de mensagem.

> [!Note]  
> As caixas de diálogo de tarefa exigem o modelo STA (single-threaded apartment).

 

## <a name="parts-of-a-task-dialog"></a>Partes de uma caixa de diálogo de tarefa

Uma caixa de diálogo de tarefa consiste em vários elementos, a maioria dos quais são opcionais. A ilustração a seguir mostra as várias partes de uma caixa de diálogo de tarefa.

![captura de tela de uma janela mostrando vários botões, incluindo um ao lado do texto de controle recolhido](images/taskdialog.jpg)

Na ilustração a seguir, o usuário clicou no botão ao lado do texto do controle recolhido, fazendo com que texto alternativo seja exibido lá e no rodapé.

![captura de tela da janela anterior, mas com duas linhas de texto de controle expandido](images/taskdialogexpand.jpg)

As ilustrações mostram as seguintes partes:



| Parte                   | Descrição                                                                                                                                                                                                                                                                                                                                                                          | Membro TASKDIALOGCONFIG                                    |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Título da janela           | Legenda da janela.                                                                                                                                                                                                                                                                                                                                                               | **pszWindowTitle**                                         |
| Ícone principal              | Um ícone grande que significa a finalidade da caixa de diálogo de tarefa.                                                                                                                                                                                                                                                                                                                          | **hMainIcon** ou **pszMainIcon**                           |
| Instrução principal       | Texto principal.                                                                                                                                                                                                                                                                                                                                                                      | **pszMainInstruction**                                     |
| Conteúdo                | Texto extra.                                                                                                                                                                                                                                                                                                                                                                          | **pszContent**                                             |
| Barra de progresso           | Uma barra animada que mostra o progresso de alguma tarefa.                                                                                                                                                                                                                                                                                                                                | **dwFlags**                                                |
| Botões de opção          | Opções definidas pelo aplicativo para o usuário.                                                                                                                                                                                                                                                                                                                                            | **pRadioButtons**                                          |
| Botão personalizado          | Um botão que não é um dos botões comuns. Isso pode ser um botão normal ou, conforme mostrado na ilustração, um link de comando com até duas linhas de texto.                                                                                                                                                                                                                    | **pButtons**                                               |
| Botão Expandir/fechar | Um botão que pode ser usado para alternar entre o texto de controle recolhido definido pelo aplicativo (como "Ver mais detalhes") e o texto de controle expandido, que pode estar em duas ou mais linhas. Quando o texto de controle é expandido, o texto adicional em **pszExpandedInformation** também é mostrado, após o texto do conteúdo ou (conforme mostrado na segunda ilustração) no rodapé. | **pszCollapsedControlText** **e pszExpandedControlText** |
| Caixa de seleção Verificação | Uma caixa de seleção, acompanhada por texto definido pelo aplicativo, para opções simples, como "Não mostrar essa caixa de diálogo novamente".                                                                                                                                                                                                                                                                     | **pszVerificationText**                                    |
| Ícone do rodapé            | Um ícone pequeno que significa a finalidade do texto do rodapé.                                                                                                                                                                                                                                                                                                                          | **hFooterIcon** ou **pszFooterIcon**                       |
| Texto do rodapé            | Texto adicional. Nas ilustrações, o texto contém um hiperlink.                                                                                                                                                                                                                                                                                                                | **pszFooter**                                              |
| Botão comum          | Um botão padrão; nas ilustrações, o botão OK.                                                                                                                                                                                                                                                                                                                              | **dwCommonButtons**                                        |



 

 

 




