---
description: Em aplicativos Winsock, um descritor de soquete não é um descritor de arquivo e deve ser usado com as funções do Winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Tipo de dados Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297062"
---
# <a name="socket-data-type"></a>Tipo de dados Socket

Em aplicativos Winsock, um descritor de soquete não é um descritor de arquivo e deve ser usado com as funções do Winsock.

No UNIX, um descritor de soquete é representado por um descritor de arquivo padrão. Como resultado, um descritor de soquete no UNIX pode ser passado para qualquer uma das funções de e/s de arquivo padrão (leitura e gravação, por exemplo).

Além disso, todos os identificadores no UNIX, incluindo identificadores de soquete, são inteiros pequenos, não negativos e alguns aplicativos fazem suposições de que isso será verdade.

Os identificadores do Windows Sockets não têm restrições, além de que o valor do \_ soquete inválido não é um soquete válido. Os identificadores de soquete podem pegar qualquer valor no intervalo de 0 a um \_ soquete inválido – 1.

Como o tipo de **soquete** não é assinado, a compilação do código-fonte existente de, por exemplo, um ambiente UNIX pode levar a avisos do compilador sobre incompatibilidades de tipos de dados assinados/não-assinados.

Isso significa, por exemplo, que a verificação de erros quando o [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e a [**aceitação**](/windows/desktop/api/Winsock2/nf-winsock2-accept) das funções retorna não deve ser feita comparando o valor de retorno com – 1 ou vendo se o valor é negativo (abordagens comuns e legais no UNIX). Em vez disso, um aplicativo deve usar o soquete de constante inválida do manifesto, \_ conforme definido no arquivo de cabeçalho *Winsock2. h* . Por exemplo:

Estilo UNIX do BSD típico


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



Estilo preferencial


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



