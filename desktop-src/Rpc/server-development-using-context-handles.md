---
title: Desenvolvimento de servidor usando identificadores de contexto
description: Da perspectiva do desenvolvimento do programa de servidor, um identificador de contexto é um ponteiro não tipado. Os programas de servidor inicializam identificadores de contexto apontando-os em dados na memória ou em alguma outra forma de armazenamento (como arquivos em discos).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005962"
---
# <a name="server-development-using-context-handles"></a>Desenvolvimento de servidor usando identificadores de contexto

Da perspectiva do desenvolvimento do programa de servidor, um identificador de contexto é um ponteiro não tipado. Os programas de servidor inicializam identificadores de contexto apontando-os em dados na memória ou em alguma outra forma de armazenamento (como arquivos em discos).

Por exemplo, suponha que um cliente use um identificador de contexto para solicitar uma série de atualizações para um registro em um banco de dados. O cliente chama um procedimento remoto no servidor e passa a ele uma chave de pesquisa. O programa de servidor pesquisa o banco de dados para a chave de pesquisa e Obtém o número de registro inteiro do registro correspondente. Em seguida, o servidor pode apontar um ponteiro para void em um local da memória que contém o número do registro. Quando ele retorna, o procedimento remoto precisaria retornar o ponteiro como um identificador de contexto por meio de seu valor de retorno ou sua lista de parâmetros. O cliente precisaria passar o ponteiro para o servidor cada vez que ele chamou procedimentos remotos para atualizar o registro. Durante cada uma dessas operações de atualização, o servidor converteria o ponteiro void para ser um ponteiro para um inteiro.

Depois que o programa do servidor apontar o identificador de contexto nos dados de contexto, o identificador será considerado aberto. Identificadores contendo um valor **nulo** são fechados. O servidor mantém um identificador de contexto aberto até que o cliente chame um procedimento remoto que o feche. Se a sessão do cliente for encerrada enquanto o identificador estiver aberto, o tempo de execução do RPC chamará a rotina de execução do servidor para liberar o identificador.

O fragmento de código a seguir demonstra como um servidor pode implementar um identificador de contexto. Neste exemplo, o servidor mantém um arquivo de dados que o cliente grava para usar procedimentos remotos. As informações de contexto são um identificador de arquivo que controla o local atual no arquivo em que o servidor gravará os dados. O identificador de arquivo é empacotado como um identificador de contexto na lista de parâmetros para chamadas de procedimento remoto. Uma estrutura contém o nome do arquivo e o identificador do arquivo. A definição de interface para este exemplo é mostrada em [desenvolvimento de interface usando identificadores de contexto](interface-development-using-context-handles.md).


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



A função RemoteClose fecha um arquivo no servidor. Observe que o aplicativo de servidor precisa atribuir **NULL** ao identificador de contexto como parte da função close. Isso se comunica com o stub do servidor e a biblioteca de tempo de execução RPC que o identificador de contexto foi excluído. Caso contrário, a conexão será mantida aberta e, eventualmente, uma execução de contexto ocorrerá.


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
> Embora seja esperado que o cliente passe um identificador de contexto válido para uma chamada com \[ \] atributos direcionais in, out, o RPC não rejeita identificadores de contexto **nulo** para essa combinação de atributos direcionais. O identificador de contexto **nulo** é passado para o servidor como um ponteiro **nulo** . O código do servidor para chamadas contendo um \[ identificador de contexto in, out \] deve ser escrito para evitar uma violação de acesso quando um ponteiro **NULL** é recebido.

 

 

 




