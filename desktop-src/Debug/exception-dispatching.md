---
description: Quando ocorre uma exceção de hardware ou software, o processador interrompe a execução no ponto em que a exceção ocorreu e transfere o controle para o sistema.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Expedição de exceção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b7b4f73c9d2c3fbaf15b4390ee6ecc6b9aa06b50524ec080fc45319d3b94767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912726"
---
# <a name="exception-dispatching"></a>Expedição de exceção

Quando ocorre uma exceção de hardware ou software, o processador interrompe a execução no ponto em que a exceção ocorreu e transfere o controle para o sistema. Primeiro, o sistema salva o estado do computador do thread atual e as informações que descrevem a exceção. Em seguida, o sistema tenta encontrar um manipulador de exceção para lidar com a exceção.

O estado do computador do thread no qual a exceção ocorreu é salvo em uma [**estrutura CONTEXT.**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Essas informações (chamadas de registro *de contexto*) permitem que o sistema continue a execução no ponto da exceção se a exceção for tratada com êxito. A descrição da exceção (chamada de **registro de exceção**) é salva em uma estrutura [**EXCEPTION \_ RECORD.**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Como ele armazena as informações dependentes do computador do registro de contexto separadamente das informações independentes do computador do registro de exceção, o mecanismo de tratamento de exceções é portátil para diferentes plataformas.

As informações nos registros de contexto e exceção estão disponíveis por meio da função [**GetExceptionInformation**](getexceptioninformation.md) e podem ser disponibilizadas para quaisquer manipuladores de exceção executados como resultado da exceção. O registro de exceção inclui as informações a seguir.

-   Um código de exceção que identifica o tipo de exceção.
-   Sinalizadores que indicam se a exceção é continuavel. Qualquer tentativa de continuar a execução após uma exceção nãocontinuável gera outra exceção.
-   Um ponteiro para outro registro de exceção. Isso facilita a criação de uma lista vinculada de exceções se ocorrerem exceções aninhadas.
-   O endereço no qual ocorreu a exceção.
-   Uma matriz de argumentos que fornecem informações adicionais sobre a exceção.

Quando ocorre uma exceção no código de modo de usuário, o sistema usa a seguinte ordem de pesquisa para encontrar um manipulador de exceção:

1.  Se o processo estiver sendo depurado, o sistema notifica o depurador. Para obter mais informações, consulte [Tratamento de exceção do depurador](debugger-exception-handling.md).
2.  Se o processo não estiver sendo depurado ou se o depurador associado não tratar a exceção, o sistema tentará localizar um manipulador de exceção baseado em quadro pesquisando os quadros de pilha do thread no qual ocorreu a exceção. O sistema pesquisa o quadro de pilha atual primeiro e, em seguida, pesquisa os quadros de pilha anteriores na ordem inversa.
3.  Se nenhum manipulador baseado em quadro puder ser encontrado ou nenhum manipulador baseado em quadro tratar a exceção, mas o processo estiver sendo depurado, o sistema notifica o depurador uma segunda vez.
4.  Se o processo não estiver sendo depurado ou se o depurador associado não tratar a exceção, o sistema fornece tratamento padrão com base no tipo de exceção. Para a maioria das exceções, a ação padrão é chamar a [**função ExitProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)

Quando ocorre uma exceção no código de modo kernel, o sistema pesquisa os quadros de pilha da pilha de kernel em uma tentativa de localizar um manipulador de exceção. Se um manipulador não puder ser localizado ou nenhum manipulador tratar a exceção, o sistema será desligado como se a [**função ExitWindows**](/windows/win32/api/winuser/nf-winuser-exitwindows) tivesse sido chamada.

 

 
