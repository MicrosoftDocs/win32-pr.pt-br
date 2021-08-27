---
description: Em aplicativos Winsock, um descritor de soquete não é um descritor de arquivo e deve ser usado com as funções Winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Tipo de dados de soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a95f890a14f68a0422ec91d31cb09735e2c85ab15cad52f9bd40499cee1167c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121236"
---
# <a name="socket-data-type"></a>Tipo de dados de soquete

Em aplicativos Winsock, um descritor de soquete não é um descritor de arquivo e deve ser usado com as funções Winsock.

No UNIX, um descritor de soquete é representado por um descritor de arquivo padrão. Como resultado, um descritor de soquete no UNIX pode ser passado para qualquer uma das funções de E/S de arquivo padrão (leitura e gravação, por exemplo).

Além disso, todos os handles UNIX, incluindo os alças de soquete, são inteiros pequenos e não negativos, e alguns aplicativos fazem suposições de que isso será verdadeiro.

Windows Os alças de soquetes não têm restrições, além de que o valor INVALID \_ SOCKET não é um soquete válido. Os alças de soquete podem ter qualquer valor no intervalo de 0 a INVALID \_ SOCKET–1.

Como o tipo **SOCKET** é não assinado, compilar o código-fonte existente de, por exemplo, um ambiente UNIX pode levar a avisos do compilador sobre incompatibilidades de tipo de dados assinados/não assinados.

Isso significa, por exemplo, que a [](/windows/desktop/api/Winsock2/nf-winsock2-socket) verificação de erros quando as funções socket e [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) retornam não deve ser feita comparando o valor de retorno com –1 ou vendo se o valor é negativo (abordagens comuns e legais no UNIX). Em vez disso, um aplicativo deve usar a constante de manifesto INVALID SOCKET conforme definido no arquivo de \_ título *Winsock2.h.* Por exemplo:

Estilo de UNIX BSD típico


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

[Considerações sobre programação winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



