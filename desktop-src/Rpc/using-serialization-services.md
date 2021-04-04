---
title: Usando serviços de serialização
description: MIDL gera um stub de serialização para o procedimento com os atributos \ Encode \ e \ decodificar \.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando serviços de serialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008320"
---
# <a name="using-serialization-services"></a>Usando serviços de serialização

MIDL gera um stub de serialização para o procedimento com os atributos \[ [**Encode**](/windows/desktop/Midl/encode) \] e \[ [**decodificação**](/windows/desktop/Midl/decode) \] . Ao chamar essa rotina, você executa uma chamada de serialização em vez de uma chamada remota. Os argumentos de procedimento são empacotados ou desempacotados de um buffer da maneira usual. Em seguida, você tem controle total dos buffers.

Por outro lado, quando o programa executa a serialização de tipo (um tipo é rotulado com atributos de serialização), o MIDL gera rotinas para dimensionar, codificar e decodificar objetos desse tipo. Para serializar dados, você deve chamar essas rotinas da maneira apropriada. A serialização de tipo é uma extensão da Microsoft e, como tal, não está disponível quando você compila no modo de compatibilidade de DCE ([**/OSF**](/windows/desktop/Midl/-osf)). Usando os atributos de \[ [**codificação**](/windows/desktop/Midl/encode) \] e \[ [**decodificação**](/windows/desktop/Midl/decode) \] como atributos de interface, o RPC aplica a codificação a todos os tipos e rotinas definidos no arquivo IDL.

Você deve fornecer buffers adequadamente alinhados ao usar os serviços de serialização. O início do buffer deve ser alinhado em um endereço que seja múltiplo de 8 ou 8 bytes alinhados. Para serialização de procedimento, cada chamada de procedimento deve realizar marshaling ou Unmarshal de uma posição de buffer que esteja alinhada em 8 bytes. Para serialização de tipo, o dimensionamento, a codificação e a decodificação devem começar em uma posição que esteja alinhada em 8 bytes.

Uma maneira de seu aplicativo garantir que seus buffers estejam alinhados é gravar a função [**de \_ \_ alocação de usuário MIDL**](/windows/desktop/Midl/midl-user-allocate-1) de forma que ele crie buffers alinhados. O exemplo de código a seguir demonstra como isso pode ser feito.


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



O exemplo a seguir mostra a [**função \_ \_ gratuita do usuário MIDL**](/windows/desktop/Midl/midl-user-free-1) correspondente.


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



 

 