---
title: Desenvolvimento de servidor usando alças de contexto
description: Da perspectiva do desenvolvimento do programa de servidor, um indicador de contexto é um ponteiro sem tipo. Os programas de servidor inicializam os handles de contexto apontando-os para dados na memória ou em alguma outra forma de armazenamento (como arquivos em discos).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db05441f7314fba628d1ec07db5f99266c595c84e672ada976b38f7576ab5d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925332"
---
# <a name="server-development-using-context-handles"></a>Desenvolvimento de servidor usando alças de contexto

Da perspectiva do desenvolvimento do programa de servidor, um indicador de contexto é um ponteiro sem tipo. Os programas de servidor inicializam os handles de contexto apontando-os para dados na memória ou em alguma outra forma de armazenamento (como arquivos em discos).

Por exemplo, suponha que um cliente use um alça de contexto para solicitar uma série de atualizações para um registro em um banco de dados. O cliente chama um procedimento remoto no servidor e passa uma chave de pesquisa. O programa de servidor pesquisa a chave de pesquisa no banco de dados e obtém o número de registro inteiro do registro correspondente. Em seguida, o servidor pode apontar um ponteiro para nulo em um local de memória que contém o número do registro. Quando ele retorna, o procedimento remoto precisaria retornar o ponteiro como um indicador de contexto por meio de seu valor de retorno ou sua lista de parâmetros. O cliente precisaria passar o ponteiro para o servidor sempre que chamasse procedimentos remotos para atualizar o registro. Durante cada uma dessas operações de atualização, o servidor poderia lançar o ponteiro nulo para ser um ponteiro para um inteiro.

Depois que o programa de servidor aponta o alça de contexto em dados de contexto, o handle é considerado aberto. Os alças que contêm **um valor NULL** são fechados. O servidor mantém um alça de contexto aberto até que o cliente chama um procedimento remoto que o fecha. Se a sessão do cliente for encerrada enquanto o handle estiver aberto, o tempo de executar RPC chamará a rotina de run-down do servidor para liberar o handle.

O fragmento de código a seguir demonstra como um servidor pode implementar um lidar com contexto. Neste exemplo, o servidor mantém um arquivo de dados que o cliente grava usando procedimentos remotos. As informações de contexto são um alça de arquivo que mantém o controle do local atual no arquivo em que o servidor gravará dados. O alça de arquivo é empacotado como um alça de contexto na lista de parâmetros para chamadas de procedimento remoto. Uma estrutura contém o nome do arquivo e o alça de arquivo. A definição de interface para este exemplo é mostrada em [Desenvolvimento de interface usando alças de contexto](interface-development-using-context-handles.md).


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



A função RemoteOpen abre um arquivo no servidor:


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



A função RemoteRead lê um arquivo no servidor.


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



A função RemoteClose fecha um arquivo no servidor. Observe que o aplicativo de servidor precisa atribuir **NULL ao** alça de contexto como parte da função close. Isso se comunica com o stub do servidor e com a biblioteca em tempo de executar RPC que o alça de contexto foi excluído. Caso contrário, a conexão será mantida aberta e, eventualmente, ocorrerá um run-down de contexto.


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> Embora seja esperado que o cliente passe um alça de contexto válido para uma chamada com atributos direcionais de entrada e saída, o RPC não rejeita os alças de contexto NULL para essa combinação de atributos \[ \] direcionais.  O **handle de** contexto NULL é passado para o servidor como um ponteiro **NULL.** O código do servidor para chamadas que contêm um handle de contexto de entrada e saída deve ser gravado para evitar uma violação de acesso \[ quando um ponteiro \] **NULL** é recebido.

 

 

 




