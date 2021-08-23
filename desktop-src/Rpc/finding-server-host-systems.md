---
title: Localizar sistemas de host do servidor
description: Localizando sistemas de host do servidor usando vinculações de cadeia de caracteres e consultando um banco de dados de serviço de nome para o local de um programa de servidor.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180e2e43c0350f55defb74762d6ab1b6b656dafbc1468bcc7f077ed9780a2e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929985"
---
# <a name="finding-server-host-systems"></a>Localizar sistemas de host do servidor

Um sistema de host do servidor é o computador que executa o programa de servidor do aplicativo distribuído. Pode haver um ou muitos sistemas de host de servidor em uma rede. A maneira como o programa cliente encontra um servidor ao qual se conectar depende das necessidades do programa.

Há dois métodos para localizar sistemas de host do servidor:

-   Usando informações armazenadas em cadeias de caracteres no código-fonte do cliente, variáveis de ambiente ou arquivos de configuração específicos do aplicativo. Seu aplicativo cliente pode usar os dados na cadeia de caracteres para compor uma associação entre o cliente e o servidor.
-   Consultando um banco de dados de serviço de nome para o local de um programa de servidor.

Esta seção apresenta informações sobre essas duas técnicas nos tópicos a seguir:

-   [Usando vinculações de cadeia de caracteres](#using-string-bindings)
-   [Importando de bancos de dados de serviço de nome](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Usando vinculações de cadeia de caracteres

Os aplicativos podem criar vinculações de informações armazenadas em cadeias de caracteres. Seu aplicativo cliente compõe essas informações como uma cadeia de caracteres e, em seguida, chama a [**função RpcBindingFromStringBinding.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) O cliente deve fornecer as seguintes informações para identificar o servidor:

-   O nome da interface, o GUID (identificador global exclusivo) do objeto ou UUID do objeto. Para obter mais informações, consulte [Gerando UUIDs](generating-interface-uuids.md) de interface e [UUID de cadeia de caracteres.](string-uuid.md)
-   O tipo de transporte pelo qual se comunicar, como pipes nomeados ou TCP/IP. Para obter detalhes, consulte [Terminologia de associação RPC essencial](essential-rpc-binding-terminology.md) e [Selecionando uma sequência de protocolo](selecting-a-protocol-sequence.md).
-   O endereço de rede ou o nome do computador host do servidor.
-   O ponto de extremidade do programa de servidor no computador host do servidor. Para obter mais informações, [consulte Localizar pontos de extremidade](finding-endpoints.md)e [Especificando pontos de extremidade](specifying-endpoints.md).

(O UUID do objeto e as informações do ponto de extremidade são opcionais.)

Nos exemplos a seguir, o *parâmetro pszNetworkAddress* e outros parâmetros incluem backslashes inseridos. A faixa invertida é um caractere de escape na linguagem de programação C. Duas malhas invertida são necessárias para representar cada caractere de invertida literal único. A estrutura de associação de cadeia de caracteres deve conter quatro caracteres de faixa invertida para representar os dois caracteres de invertida literais que precedem o nome do servidor.

O exemplo a seguir mostra que o nome do servidor deve ser precedido por oito linhas invertidas para que quatro caracteres de invertida literal apareçam na estrutura de dados de associação de cadeia de caracteres depois que a função **sprintf \_** processa a cadeia de caracteres.


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



No exemplo a seguir, a associação de cadeia de caracteres aparece como:

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np: \\ \\ \\ \\ *servername* \[ \\ \\ \\ \\ *pipename*\]

Em seguida, o [**cliente chama RpcBindingFromStringBinding para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) obter o handle de associação:


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



Uma função de conveniência, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) monta o objeto UUID, a sequência de protocolo, o endereço de rede e o ponto de extremidade na sintaxe correta para a chamada para [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding). Você não precisa se preocupar em colocar o e vírgula, os dois-pontos e os vários componentes de cada sequência de protocolo no lugar certo; você apenas fornece as cadeias de caracteres como parâmetros para a função. A biblioteca em tempo de executar aloca até mesmo a memória necessária para a associação de cadeia de caracteres.


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



Outra função de conveniência, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), aceita um alça de associação como entrada e produz a associação de cadeia de caracteres correspondente.

## <a name="importing-from-name-service-databases"></a>Importando de bancos de dados de serviço de nome

Nomes de armazenamento de bancos de dados de serviço, entre outras coisas, alças de associação e UUIDs. Seu aplicativo cliente pode pesquisar um ou ambos quando precisar se vincular ao servidor. Para obter uma discussão sobre as informações que um serviço de nome armazena e o formato de armazenamento, consulte O Banco de Dados do Serviço [de Nome RPC](the-rpc-name-service-database.md).

A biblioteca RPC fornece dois conjuntos de funções que seu programa cliente pode usar para pesquisar o nome do banco de dados de serviço. Os nomes de um conjunto começam com RpcNsBindingImport. Os nomes do outro conjunto começam com RpcNsBindingLookup. A diferença entre os dois grupos de funções é que as funções RpcNsBindingImport retornam um único alça de associação por chamada e as funções RpcNsBindingLookup retornam grupos de alças por chamada.

Para iniciar uma pesquisa com as funções RpcNsBindingImport, primeiro chame [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), conforme mostrado no fragmento de código a seguir.


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



Quando as funções RPC pesquisam o nome do banco de dados de serviço, elas precisam de um local para iniciar a pesquisa. Na terminologia RPC, isso é chamado de nome de entrada. O programa cliente passa o nome da entrada como o segundo parâmetro para [**RpcNsBindingImportBegin.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Esse parâmetro pode ser **NULL se** você quiser pesquisar o banco de dados de serviço de nome inteiro. Como alternativa, você pode pesquisar a entrada do servidor passando um nome de entrada de servidor ou pesquisar a entrada de grupo passando um nome de entrada de grupo. Passar um nome de entrada restringe a pesquisa ao conteúdo dessa entrada.

No exemplo anterior, o valor RPC C NS SYNTAX DEFAULT é passado como o primeiro \_ \_ parâmetro para \_ \_ [**RpcNsBindingImportBegin.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Isso seleciona a sintaxe de nome de entrada padrão. Atualmente, essa é a única sintaxe de nome de entrada com suporte.

Seu aplicativo cliente pode pesquisar o nome do banco de dados de serviço para um nome de interface, um UUID ou ambos. Se você quiser que ele pesquise uma interface por nome, passe a variável de interface global que o compilador MIDL gera do arquivo IDL como o terceiro parâmetro [**para RpcNsBindingImportBegin.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Você encontrará sua declaração no arquivo de header que o compilador MIDL gerou quando ele gerou o stub do cliente. Se você quiser que seu programa cliente pesquise apenas por UUID, de definir o terceiro parâmetro como **NULL.**

Ao pesquisar o nome do banco de dados de serviço para um UUID, de definir o quarto parâmetro [**de RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) como o UUID que você deseja pesquisar. Se você não estiver pesquisando um UUID, de definido esse parâmetro como **NULL.**

A [**função RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) passa o endereço de um nome service-search context handle por meio de seu quinto parâmetro. Você passa esse parâmetro para outras funções RpcNsBindingImport.

Em particular, a próxima função que seu aplicativo cliente chamaria é [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext). Os programas cliente usam essa função para recuperar os alças de associação compatíveis do banco de dados de serviço de nome. O fragmento de código a seguir demonstra como essa função pode ser chamada:


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Depois de chamar a [**função RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obter um alça de associação, o aplicativo cliente poderá determinar se o handle recebido é aceitável. Caso não, o programa cliente poderá executar um loop e chamar **RpcNsBindingImportNext** novamente para ver se o serviço de nome contém um alça mais apropriado. Para cada chamada para **RpcNsBindingImportNext**, deve haver uma chamada correspondente para RpcNsBindingFree. Quando a pesquisa for concluída, chame a [**função RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) para liberar o contexto de pesquisa.

Depois que o aplicativo cliente tiver um alça de associação aceitável, ele deverá verificar se o aplicativo do servidor está em execução. Há dois métodos que seu cliente pode usar para executar essa verificação. A primeira é chamar uma função na interface do cliente. Se o programa de servidor estiver em execução, a chamada será concluída. Caso não seja, a chamada falhará. Uma maneira melhor de verificar se o servidor está em execução é invocar [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), seguido por uma chamada para [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening). Para obter mais informações sobre o nome do banco de dados de serviço, consulte O banco de dados do serviço [de nome RPC](the-rpc-name-service-database.md).

 

 




