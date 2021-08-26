---
title: Desenvolvimento de interface usando alças de contexto
description: Normalmente, você cria um identificador de contexto especificando o atributo \ context handle\ em uma \_ definição de tipo no arquivo IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e65e36384bda3d81526d5891eca92a77a67402e7cd3aa7af8b61e061a9d3b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020466"
---
# <a name="interface-development-using-context-handles"></a>Desenvolvimento de interface usando alças de contexto

Normalmente, você cria um identificador de contexto especificando o atributo de identificador \[ [**\_ de**](/windows/desktop/Midl/context-handle) contexto em \] uma definição de tipo no arquivo IDL. A definição de tipo também especifica implicitamente uma rotina de run down de contexto, que você deve fornecer. Se a comunicação entre o cliente e o servidor for corrompada, o tempo de execução do servidor invocará essa rotina para executar qualquer limpeza necessária. Para obter mais informações sobre rotinas de run-down de contexto, consulte [Rotina de run-down de](server-context-run-down-routine.md)contexto do servidor.

Uma interface que usa um alça de contexto deve ter um alça de associação para a associação inicial, que deve ocorrer antes que o servidor possa retornar um alça de contexto. Você pode usar um alça de associação automática, implícita ou explícita para criar a associação e estabelecer o contexto.

Um identificador de contexto deve ser [ * *do tipo void \** _](/windows/desktop/Midl/void) ou um tipo que resolve para _ [*void. \** *](/windows/desktop/Midl/void) O programa de servidor o lança para o tipo necessário.

> [!Note]  
> O uso de \[ [**em**](/windows/desktop/Midl/in), [**para parâmetros**](/windows/desktop/Midl/out-idl) de alça de contexto não é desacentado, exceto para \] rotinas que fecham os alças de contexto. Se o contexto tratar parâmetros marcados em , out serão usados, não passe um handle de contexto NULL ou não reinicializado do \[ [](/windows/desktop/Midl/in)cliente para [](/windows/desktop/Midl/out-idl) \] o servidor.  Um **ponteiro NULL** para um alça de contexto deve ser passado em vez disso. Observe que os parâmetros de alça de contexto \[ [**marcados em**](/windows/desktop/Midl/in) \] não aceitam **ponteiros NULL.**

 

O fragmento a seguir de uma definição de interface de exemplo mostra como um aplicativo distribuído pode usar um alça de contexto para abrir um servidor e atualizar um arquivo de dados para cada cliente.

A interface deve conter uma chamada de procedimento remoto para inicializar o handle e defini-lo como um **valor** não nulo. Neste exemplo, a função RemoteOpen executa essa operação. Especifica o alçamento de contexto com um \[ [**atributo direcional**](/windows/desktop/Midl/out-idl) \] de saída. Como alternativa, você pode retornar o alça de contexto como o valor de retorno do procedimento. No entanto, neste exemplo, passaremos o handle de contexto pela lista de parâmetros.

Neste exemplo, as informações de contexto são um handle de arquivo. Ele mantém o controle do local atual no arquivo. A interface pacotes o alça de arquivo como um alça de contexto e o passa como um parâmetro para chamadas de procedimento remoto. Uma estrutura contém o nome do arquivo e o alça de arquivo.

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

A função RemoteOpen cria um handle de contexto **válido,** não nulo. Ele passa o alça de contexto para o cliente. Chamadas de procedimento remoto subsequentes, como RemoteRead, usam o alça de contexto como um ponteiro in.

Além do procedimento remoto que inicializa o handle de contexto, a interface deve conter um procedimento que libera o contexto do servidor e define o handle de contexto como **NULL.** No exemplo anterior, a função RemoteClose executa essa operação.

 

 