---
title: Processar conexão com uma estação de janela
description: Um processo estabelece automaticamente uma conexão com uma estação de janela e área de trabalho quando chama pela primeira vez uma função USER32 ou GDI32 (que não seja a estação de janela e as funções de desktop).
ms.assetid: 280f69e7-5c99-41a7-94e3-da13deaac9f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a87e97b19ac1210b04447652268c5f53b7e2a6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366434"
---
# <a name="process-connection-to-a-window-station"></a>Processar conexão com uma estação de janela

Um processo estabelece automaticamente uma conexão com uma estação de janela e área de trabalho quando chama pela primeira vez uma função USER32 ou GDI32 (que não seja a estação de janela e as funções de desktop). O sistema determina a estação de janela à qual um processo se conecta de acordo com as seguintes regras:

1.  Se o processo tiver chamado a função [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) , ele se conectará à estação de janela especificada nessa chamada.
2.  Se o processo não chamou [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation), ele se conecta à estação de janela herdada do processo pai.
3.  Se o processo não chamou [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) e não herdou uma estação de janela, o sistema tenta abrir para o máximo de \_ acesso permitido e se conectar a uma estação de janela da seguinte maneira:
    -   Se um nome de estação de janela tiver sido especificado no membro **lpDesktop** da estrutura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que foi usada quando o processo foi criado, o processo se conectará à estação de janela especificada.
    -   Caso contrário, se o processo estiver sendo executado na sessão de logon do usuário interativo, o processo se conectará à estação de janela interativa.
    -   Se o processo estiver sendo executado em uma sessão de logon não interativa, o nome da estação de janela será formado com base no identificador de sessão de logon e será feita uma tentativa de abrir essa estação de janela. Se a operação de abertura falhar porque essa estação de janela não existe, o sistema tenta criar a estação de janela e uma área de trabalho padrão.

A estação de janela atribuída durante esse processo de conexão não pode ser fechada chamando a função [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) .

Quando um processo está se conectando a uma estação de janela, o sistema pesquisa a tabela identificador do processo em busca de identificadores herdados. O sistema usa o primeiro identificador de estação da janela que encontra. Se você quiser que um processo filho se conecte a uma estação de janela herdada específica, certifique-se de que apenas o identificador desejado esteja marcado como herdável. Se um processo filho herdar vários identificadores de estação de janela, os resultados da conexão de estação do Windows serão indefinidos.

Os identificadores para uma estação de janela que o sistema abre ao conectar um processo a uma estação de janela não são herdáveis.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conexão de thread com uma área de trabalho](thread-connection-to-a-desktop.md)
</dt> </dl>

 

 