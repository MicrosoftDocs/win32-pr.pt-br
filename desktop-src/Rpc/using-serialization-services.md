---
title: Usando os Serviços de Serialização
description: MIDL gera um stub de serialização para o procedimento com os atributos \ encode\ e \ decode\.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, usando serviços de serialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be20d513bdb74eca316b022dd8536e8988e32e93099981cc77830035048e55e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010624"
---
# <a name="using-serialization-services"></a>Usando os Serviços de Serialização

MIDL gera um stub de serialização para o procedimento com os atributos \[ [**codificar**](/windows/desktop/Midl/encode) \] e \[ [**decodificar**](/windows/desktop/Midl/decode) \] . Quando você chama essa rotina, executa uma chamada de serialização em vez de uma chamada remota. Os argumentos de procedimento são empacotados para ou desmarques de um buffer da maneira normal. Em seguida, você tem controle total dos buffers.

Por outro lado, quando seu programa executa a serialização de tipo (um tipo é rotulado com atributos de serialização), MIDL gera rotinas para tamanho, codificação e decodificar objetos desse tipo. Para serializar dados, você deve chamar essas rotinas da maneira apropriada. A serialização de tipo é uma extensão da Microsoft e, como tal, não está disponível quando você compila no modo de compatibilidade com DCE ([**/osf).**](/windows/desktop/Midl/-osf) Usando os atributos de codificação e decodificar como atributos de interface, o RPC aplica a codificação a todos os tipos e \[ [](/windows/desktop/Midl/encode) \] \[ [](/windows/desktop/Midl/decode) \] rotinas definidos no arquivo IDL.

Você deve fornecer buffers alinhados adequadamente ao usar serviços de serialização. O início do buffer deve ser alinhado a um endereço que seja um múltiplo de 8 ou 8 byte alinhado. Para serialização de procedimento, cada chamada de procedimento deve efetuar marshal in ou unmarshal de uma posição de buffer alinhada de 8 byte. Para serialização de tipo, o sizing, a codificação e a decodificação devem começar em uma posição alinhada de 8 byte.

Uma maneira de seu aplicativo garantir que seus buffers estejam alinhados é escrever a função de alocação de usuário médio, de modo que ele crie buffers alinhados. [**\_ \_**](/windows/desktop/Midl/midl-user-allocate-1) O exemplo de código a seguir demonstra como isso pode ser feito.


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



O exemplo a seguir mostra a [**função de usuário midl \_ \_ free**](/windows/desktop/Midl/midl-user-free-1) correspondente.


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 