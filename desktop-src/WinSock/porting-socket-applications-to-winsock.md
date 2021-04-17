---
description: Esta seção descreve as considerações de portabilidade do Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Portando aplicativos de soquete para Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811728"
---
# <a name="porting-socket-applications-to-winsock"></a>Portando aplicativos de soquete para Winsock

Esta seção descreve as considerações de portabilidade do Winsock.

Há um número limitado de instâncias em que o Windows Sockets diverteu da adesão estrita às convenções de Berkeley, geralmente devido a dificuldades de implementação no ambiente do Microsoft Windows.

Quando um desvio das convenções de Berkeley ocorre no Windows Sockets, o desvio é especificamente indicado e claramente anotado. Por exemplo, se uma função for específica para o Windows Sockets, esse desvio será especificado com uma frase na descrição da função semelhante à seguinte:

A função **\[ Function- \] Name** é uma extensão específica da Microsoft para a API do Windows Sockets 2.

Esta seção fornece informações sobre portabilidade de aplicativos de soquete UNIX do Berkeley (BSD) para Winsock:

-   [Tipo de dados Socket](socket-data-type-2.md)
-   [Macros Select, FD \_ set e FD \_ xxx](select-and-fd---2.md)
-   [Códigos de erro-errno, h \_ errno e WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [Ponteiros](pointers-2.md)
-   [Funções renomeadas](renamed-functions-2.md)
-   [Número máximo de soquetes com suporte](maximum-number-of-sockets-supported-2.md)
-   [Incluir arquivos](include-files-2.md)
-   [Valores de retorno em falha de função](return-values-on-function-failure-2.md)
-   [Soquetes brutos](service-provided-raw-sockets-2.md)
-   [Ordenação de bytes](byte-ordering-2.md)
-   [Rotinas de conversão de Byte-Order estendidas](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulando erros do Winsock](handling-winsock-errors.md)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Códigos de erro do Windows Sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



