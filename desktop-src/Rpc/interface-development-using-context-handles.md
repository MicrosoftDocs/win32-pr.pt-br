---
title: Desenvolvimento de interface usando identificadores de contexto
description: Normalmente, você cria um identificador de contexto especificando o atributo \ Context \_ Handle \ em uma definição de tipo no arquivo IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641602"
---
# <a name="interface-development-using-context-handles"></a>Desenvolvimento de interface usando identificadores de contexto

Normalmente, você cria um identificador de contexto especificando o \[ atributo de [**\_ identificador de contexto**](/windows/desktop/Midl/context-handle) \] em uma definição de tipo no arquivo IDL. A definição de tipo também especifica implicitamente uma rotina de execução de contexto que você deve fornecer. Se a comunicação entre o cliente e o servidor for interrompida, o tempo de execução do servidor invoca essa rotina para executar qualquer limpeza necessária. Para obter mais informações sobre rotinas de execução de contexto, consulte [rotina de execução de contexto de servidor](server-context-run-down-routine.md).

Uma interface que usa um identificador de contexto deve ter um identificador de associação para a associação inicial, que precisa ocorrer antes que o servidor possa retornar um identificador de contexto. Você pode usar um identificador de associação automático, implícito ou explícito para criar a associação e estabelecer o contexto.

Um identificador de contexto deve ser do [**tipo \* void**](/windows/desktop/Midl/void) ou um tipo que resolve para [**void \***](/windows/desktop/Midl/void). O programa do servidor o converte para o tipo necessário.

> [!Note]  
> O uso de \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] para parâmetros de identificador de contexto é desencorajado, exceto para rotinas que fecham identificadores de contexto. Se o contexto manipula os parâmetros marcados como \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] são usados, não passe um identificador de contexto **nulo** ou não inicializado do cliente para o servidor. Em vez disso, um ponteiro **nulo** para um identificador de contexto deve ser passado. Observe que os parâmetros de identificador de contexto marcados \[ [**em**](/windows/desktop/Midl/in) não \] aceitam ponteiros **nulos** .

 

O fragmento a seguir de uma definição de interface de exemplo mostra como um aplicativo distribuído pode usar um identificador de contexto para ter um servidor aberto e atualizar um arquivo de dados para cada cliente.

A interface deve conter uma chamada de procedimento remoto para inicializar o identificador e defini-lo como um valor não **nulo** . Neste exemplo, a função RemoteOpen executa essa operação. Especifica o identificador de contexto com um \[ [](/windows/desktop/Midl/out-idl) \] atributo direcional out. Como alternativa, você pode retornar o identificador de contexto como o valor de retorno do procedimento. No entanto, neste exemplo, passaremos a alça de contexto por meio da lista de parâmetros.

Neste exemplo, as informações de contexto são um identificador de arquivo. Ele controla o local atual no arquivo. A interface empacota o identificador de arquivo como um identificador de contexto e o passa como um parâmetro para chamadas de procedimento remoto. Uma estrutura contém o nome do arquivo e o identificador do arquivo.

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

A função RemoteOpen cria um identificador de contexto válido e não **nulo** . Ele passa o identificador de contexto para o cliente. As chamadas de procedimento remoto subsequentes, como RemoteRead, usam o identificador de contexto como um ponteiro de entrada.

Além do procedimento remoto que inicializa o identificador de contexto, a interface deve conter um procedimento que libera o contexto do servidor e define o identificador de contexto como **nulo**. No exemplo anterior, a função RemoteClose executa essa operação.

 

 