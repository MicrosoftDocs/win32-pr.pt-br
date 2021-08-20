---
description: Esta seção descreve as considerações de portação do Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Portando aplicativos de soquete para Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97b545c679d9ceb13e3173550dd04b4724309d078b2e8e39fb20419921ba941f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111864"
---
# <a name="porting-socket-applications-to-winsock"></a>Portando aplicativos de soquete para Winsock

Esta seção descreve as considerações de portação do Winsock.

Há um número limitado de instâncias em que Windows Sockets desviou da adesão estrita às convenções de Berkeley, geralmente devido a dificuldades de implementação no ambiente microsoft Windows.

Quando ocorre um desvio das convenções de Berkeley Windows soquetes, o desvio é especificamente e claramente notado. Por exemplo, se uma função for específica Windows Soquetes, esse desvio será especificado com uma frase na descrição da função semelhante à seguinte:

A **\[ função \] function-name** é uma extensão específica da Microsoft para a API Windows Sockets 2.

Esta seção fornece informações sobre como portar aplicativos de soquete de UNIX Berkeley (BSD) para o Winsock:

-   [Tipo de dados de soquete](socket-data-type-2.md)
-   [Macros Select, FD \_ SET e FD \_ XXX](select-and-fd---2.md)
-   [Códigos de erro – errno, h \_ errno e WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [Ponteiros](pointers-2.md)
-   [Funções renomeadas](renamed-functions-2.md)
-   [Número máximo de soquetes com suporte](maximum-number-of-sockets-supported-2.md)
-   [Incluir arquivos](include-files-2.md)
-   [Valores de retorno em falha de função](return-values-on-function-failure-2.md)
-   [Soquetes brutos](service-provided-raw-sockets-2.md)
-   [Ordenação de byte](byte-ordering-2.md)
-   [Rotinas Byte-Order conversão estendidas](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erros winsock](handling-winsock-errors.md)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Códigos de erro de soquetes](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considerações sobre programação winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



