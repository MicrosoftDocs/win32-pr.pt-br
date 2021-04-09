---
description: Quando ocorre uma exceção de hardware ou software, o processador para a execução no ponto em que a exceção ocorreu e transfere o controle para o sistema.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Expedição de exceção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02b40aa132541fe88d692cbbf1881a8b620a209
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088842"
---
# <a name="exception-dispatching"></a>Expedição de exceção

Quando ocorre uma exceção de hardware ou software, o processador para a execução no ponto em que a exceção ocorreu e transfere o controle para o sistema. Primeiro, o sistema salva o estado da máquina do thread atual e as informações que descrevem a exceção. Em seguida, o sistema tenta encontrar um manipulador de exceção para manipular a exceção.

O estado da máquina do thread no qual a exceção ocorreu é salvo em uma estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) . Essas informações (chamadas de *registro de contexto*) permitem que o sistema continue a execução no ponto da exceção se a exceção for manipulada com êxito. A descrição da exceção (chamada de **registro de exceção**) é salva em uma estrutura de [**\_ registro de exceção**](/windows/desktop/api/WinNT/ns-winnt-exception_record) . Como ele armazena as informações dependentes do computador do registro de contexto separadamente das informações independentes da máquina do registro de exceção, o mecanismo de tratamento de exceções é portátil para diferentes plataformas.

As informações no contexto e nos registros de exceção estão disponíveis por meio da função [**GetExceptionInformation**](getexceptioninformation.md) e podem ser disponibilizadas para quaisquer manipuladores de exceção que são executados como resultado da exceção. O registro de exceção inclui as informações a seguir.

-   Um código de exceção que identifica o tipo de exceção.
-   Sinalizadores que indicam se a exceção é continuável. Qualquer tentativa de continuar a execução após uma exceção não continuável gera outra exceção.
-   Um ponteiro para outro registro de exceção. Isso facilita a criação de uma lista vinculada de exceções se ocorrerem exceções aninhadas.
-   O endereço no qual a exceção ocorreu.
-   Uma matriz de argumentos que fornece informações adicionais sobre a exceção.

Quando ocorre uma exceção no código de modo de usuário, o sistema usa a seguinte ordem de pesquisa para encontrar um manipulador de exceção:

1.  Se o processo estiver sendo depurado, o sistema notificará o depurador. Para obter mais informações, consulte [manipulação de exceção do depurador](debugger-exception-handling.md).
2.  Se o processo não estiver sendo depurado, ou se o depurador associado não tratar a exceção, o sistema tentará localizar um manipulador de exceção baseado em quadros pesquisando os quadros de pilha do thread no qual a exceção ocorreu. O sistema pesquisa primeiro o quadro de pilha atual e, em seguida, pesquisa os quadros de pilha anteriores na ordem inversa.
3.  Se nenhum manipulador baseado em quadros puder ser encontrado ou nenhum manipulador baseado em quadros tratar a exceção, mas o processo estiver sendo depurado, o sistema notificará o depurador uma segunda vez.
4.  Se o processo não estiver sendo depurado, ou se o depurador associado não tratar a exceção, o sistema fornecerá manipulação padrão com base no tipo de exceção. Para a maioria das exceções, a ação padrão é chamar a função [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .

Quando ocorre uma exceção no código do modo kernel, o sistema pesquisa os quadros de pilha da pilha do kernel em uma tentativa de localizar um manipulador de exceção. Se um manipulador não puder ser localizado ou nenhum manipulador tratar a exceção, o sistema será desligado como se a função [**ExitWindows**](/windows/win32/api/winuser/nf-winuser-exitwindows) tivesse sido chamada.

 

 
