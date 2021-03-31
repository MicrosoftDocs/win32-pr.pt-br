---
title: Sobre caixas de diálogo de tarefas
description: Um diálogo de tarefa é uma caixa de diálogo que pode ser usada para exibir informações e receber a entrada simples do usuário.
ms.assetid: vs|controls|~\controls\toolbar\taskdialogsoverview.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb5cafa452a4ed653c404d053e888c6de644236
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916111"
---
# <a name="about-task-dialogs"></a>Sobre caixas de diálogo de tarefas

Um diálogo de tarefa é uma caixa de diálogo que pode ser usada para exibir informações e receber a entrada simples do usuário. Como uma caixa de mensagem, ela é formatada pelo sistema operacional de acordo com os parâmetros definidos. No entanto, uma caixa de diálogo de tarefa tem muito mais recursos do que uma mensagem.

> [!Note]  
> As caixas de diálogo de tarefa exigem o modelo STA (single-threaded apartment).

 

## <a name="parts-of-a-task-dialog"></a>Partes de uma caixa de diálogo de tarefa

Uma caixa de diálogo de tarefa consiste em vários elementos, a maioria dos quais são opcionais. A ilustração a seguir mostra as várias partes de uma caixa de diálogo de tarefa.

![captura de tela de uma janela mostrando vários botões, incluindo um ao lado do texto de controle recolhido](images/taskdialog.jpg)

Na ilustração a seguir, o usuário clicou no botão ao lado do texto de controle recolhido, fazendo com que o texto alternativo seja exibido lá e no rodapé.

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
| Botão personalizado          | Um botão que não é um dos botões comuns. Pode ser um botão normal ou, conforme mostrado na ilustração, um link de comando com até duas linhas de texto.                                                                                                                                                                                                                    | **pButtons**                                               |
| Botão expandir/recolher | Um botão que pode ser usado para alternar entre o texto de controle recolhido definido pelo aplicativo (como "ver mais detalhes") e o texto de controle expandido, que pode estar em duas ou mais linhas. Quando o texto de controle é expandido, o texto adicional em **pszExpandedInformation** também é mostrado, seja após o texto do conteúdo ou (conforme mostrado na segunda ilustração) no rodapé. | **pszCollapsedControlText** e **pszExpandedControlText** |
| Caixa de seleção de verificação | Uma caixa de seleção, acompanhada pelo texto definido pelo aplicativo, para opções simples, como "não mostrar esta caixa de diálogo novamente".                                                                                                                                                                                                                                                                     | **pszVerificationText**                                    |
| Ícone de rodapé            | Um pequeno ícone que significa a finalidade do texto do rodapé.                                                                                                                                                                                                                                                                                                                          | **hFooterIcon** ou **pszFooterIcon**                       |
| Texto do rodapé            | Texto adicional. Nas ilustrações, o texto contém um hiperlink.                                                                                                                                                                                                                                                                                                                | **pszFooter**                                              |
| Botão comum          | Um botão padrão; nas ilustrações, o botão OK.                                                                                                                                                                                                                                                                                                                              | **dwCommonButtons**                                        |



 

 

 




