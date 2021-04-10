---
title: Conexão de thread com uma área de trabalho
description: Depois que um processo se conecta a uma estação de janela, o sistema atribui uma área de trabalho ao thread que faz a conexão.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162304"
---
# <a name="thread-connection-to-a-desktop"></a>Conexão de thread com uma área de trabalho

Depois que um processo se conecta a uma estação de janela, o sistema atribui uma área de trabalho ao thread que faz a conexão. O sistema determina a área de trabalho a ser atribuída ao thread de acordo com as seguintes regras:

1.  Se o thread tiver chamado a função [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , ele se conectará à área de trabalho especificada.
2.  Se o thread não chamou [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), ele se conecta ao desktop herdado do processo pai.
3.  Se o thread não chamou [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) e não herdou uma área de trabalho, o sistema tenta abrir para o máximo de \_ acesso permitido e se conectar a uma área de trabalho da seguinte maneira:
    -   Se um nome de área de trabalho tiver sido especificado no membro **lpDesktop** da estrutura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que foi usada quando o processo foi criado, o thread se conectará à área de trabalho especificada.
    -   Caso contrário, o thread se conecta à área de trabalho padrão da estação de janela à qual o processo está conectado.

A área de trabalho atribuída durante esse processo de conexão não pode ser fechada chamando a função [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) .

Quando um processo está se conectando a uma área de trabalho, o sistema pesquisa a tabela identificador do processo em busca de identificadores herdados. O sistema usa o primeiro identificador de área de trabalho que encontra. Se você quiser que um processo filho se conecte a uma área de trabalho herdada específica, certifique-se de que o único identificador desejado esteja marcado como herdável. Se um processo filho herdar vários identificadores de área de trabalho, os resultados da conexão de área de trabalho serão indefinidos.

Os identificadores para um desktop que o sistema abre ao conectar um processo a uma área de trabalho não são herdáveis.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar conexão com uma estação de janela](process-connection-to-a-window-station.md)
</dt> </dl>

 

 