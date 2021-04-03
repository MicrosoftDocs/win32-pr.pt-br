---
title: Localizando sistemas de host de servidor
description: Localizando sistemas de host de servidor usando associações de cadeia de caracteres e consultando um banco de dados de serviço de nome para o local de um programa de servidor.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822709"
---
# <a name="finding-server-host-systems"></a>Localizando sistemas de host de servidor

Um sistema host do servidor é o computador que executa o programa do servidor do aplicativo distribuído. Pode haver um ou vários sistemas de host de servidor em uma rede. A forma como o programa cliente encontra um servidor para se conectar depende das necessidades do seu programa.

Há dois métodos para localizar sistemas de host de servidor:

-   Usar informações armazenadas em cadeias de caracteres no código-fonte do cliente, variáveis de ambiente ou arquivos de configuração específicos do aplicativo. O aplicativo cliente pode usar os dados na cadeia de caracteres para compor uma associação entre o cliente e o servidor.
-   Consultando um banco de dados de serviço de nome para o local de um programa de servidor.

Esta seção apresenta informações sobre essas duas técnicas nos tópicos a seguir:

-   [Usando associações de cadeia de caracteres](#using-string-bindings)
-   [Importando de bancos de dados de serviço de nome](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Usando associações de cadeia de caracteres

Os aplicativos podem criar associações de informações armazenadas em cadeias de caracteres. O aplicativo cliente compõe essas informações como uma cadeia de caracteres e, em seguida, chama a função [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) . O cliente deve fornecer as seguintes informações para identificar o servidor:

-   O nome da interface, o GUID (identificador global exclusivo) do objeto ou UUID do objeto. Para obter mais informações, consulte [gerando UUIDs de interface](generating-interface-uuids.md) e [UUID de cadeia de caracteres](string-uuid.md).
-   O tipo de transporte para se comunicar, como pipes nomeados ou TCP/IP. Para obter detalhes, consulte [terminologia de ligação de RPC essencial](essential-rpc-binding-terminology.md) e [selecionando uma sequência de protocolo](selecting-a-protocol-sequence.md).
-   O endereço de rede ou o nome do computador host do servidor.
-   O ponto de extremidade do programa de servidor no computador host do servidor. Para obter mais informações, consulte [localizando pontos de extremidade](finding-endpoints.md)e [especificando pontos de extremidade](specifying-endpoints.md).

(O UUID do objeto e as informações do ponto de extremidade são opcionais.)

Nos exemplos a seguir, o parâmetro *pszNetworkAddress* e outros parâmetros incluem barras invertidas incorporadas. A barra invertida é um caractere de escape na linguagem de programação C. Duas barras invertidas são necessárias para representar cada caractere de barra invertida literal único. A estrutura de associação de cadeia de caracteres deve conter quatro caracteres de barra invertida para representar os dois caracteres de barra invertida literal que precedem o nome do servidor.

O exemplo a seguir mostra que o nome do servidor deve ser precedido por oito barras invertidas para que quatro caracteres de barra invertida literal apareçam na estrutura de dados de vinculação de cadeia de caracteres depois que a função **sprintf \_ s** processa a cadeia de caracteres.


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

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *nomeservidor* \[ \\ \\ \\ \\  pipe pipeName\]

Em seguida, o cliente chama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obter o identificador de associação:


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



Uma função de conveniência, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) , monta o UUID do objeto, a sequência de protocolos, o endereço de rede e o ponto de extremidade na sintaxe correta para a chamada para [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding). Você não precisa se preocupar em colocar o e comercial, dois-pontos e os vários componentes para cada sequência de protocolo no local certo; Você apenas fornece as cadeias de caracteres como parâmetros para a função. A biblioteca de tempo de execução mesmo aloca a memória necessária para a associação de cadeia de caracteres.


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



Outra função de conveniência, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), usa um identificador de associação como entrada e produz a associação de cadeia de caracteres correspondente.

## <a name="importing-from-name-service-databases"></a>Importando de bancos de dados de serviço de nome

Os bancos de dados do serviço de nome armazenam, entre outras coisas, identificadores e UUIDs de associação. O aplicativo cliente pode procurar um ou ambos quando precisar fazer a ligação com o servidor. Para obter uma discussão sobre as informações que um serviço de nome armazena e o formato de armazenamento, consulte [o banco de dados do serviço de nome RPC](the-rpc-name-service-database.md).

A Biblioteca RPC fornece dois conjuntos de funções que seu programa cliente pode usar para pesquisar o banco de dados do serviço de nome. Os nomes de um conjunto começam com RpcNsBindingImport. Os nomes do outro conjunto começam com RpcNsBindingLookup. A diferença entre os dois grupos de funções é que as funções RpcNsBindingImport retornam um único identificador de associação por chamada e as funções RpcNsBindingLookup retornam grupos de identificadores por chamada.

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



Quando as funções RPC pesquisam o banco de dados do serviço de nome, elas precisam de um local para iniciar a pesquisa. Na terminologia de RPC, isso é chamado de nome de entrada. O programa cliente passa o nome da entrada como o segundo parâmetro para [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Esse parâmetro poderá ser **nulo** se você quiser pesquisar todo o banco de dados do serviço de nome. Como alternativa, você pode pesquisar a entrada de servidor passando um nome de entrada de servidor ou pesquisar a entrada de grupo passando um nome de entrada de grupo. Passar um nome de entrada restringe a pesquisa para o conteúdo dessa entrada.

No exemplo anterior, o valor padrão da \_ sintaxe RPC C \_ ns \_ \_ é passado como o primeiro parâmetro para [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Isso seleciona a sintaxe de nome de entrada padrão. Atualmente, essa é a única sintaxe de nome de entrada com suporte.

Seu aplicativo cliente pode pesquisar o nome do banco de dados do serviço de nome de uma interface, um UUID ou ambos. Se você quiser que ele pesquise uma interface por nome, passe a variável de interface global que o compilador MIDL gera de seu arquivo IDL como o terceiro parâmetro para [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Você encontrará sua declaração no arquivo de cabeçalho que o compilador MIDL gerou quando gerou o stub do cliente. Se você quiser que o programa cliente pesquise por UUID somente, defina o terceiro parâmetro como **nulo**.

Ao pesquisar o banco de dados do serviço de nome para um UUID, defina o quarto parâmetro de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) como o UUID que você deseja pesquisar. Se você não estiver procurando um UUID, defina esse parâmetro como **NULL**.

A função [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) passa o endereço de um serviço de nome – identificador de contexto de pesquisa por meio de seu quinto parâmetro. Você passa esse parâmetro para outras funções RpcNsBindingImport.

Em particular, a próxima função que seu aplicativo cliente chamaria é [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext). Os programas cliente usam essa função para recuperar identificadores de associação compatíveis do banco de dados do serviço de nome. O fragmento de código a seguir demonstra como essa função pode ser chamada:


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Depois de chamar a função [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obter um identificador de associação, o aplicativo cliente pode determinar se o identificador recebido é aceitável. Caso contrário, o programa cliente pode executar um loop e chamar **RpcNsBindingImportNext** novamente para ver se o serviço de nome contém um identificador mais apropriado. Para cada chamada para **RpcNsBindingImportNext**, deve haver uma chamada correspondente para RpcNsBindingFree. Quando a pesquisa for concluída, chame a função [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) para liberar o contexto de pesquisa.

Depois que o aplicativo cliente tem um identificador de associação aceitável, ele deve verificar se o aplicativo do servidor está em execução. Há dois métodos que o cliente pode usar para executar essa verificação. A primeira é chamar uma função na interface do cliente. Se o programa do servidor estiver em execução, a chamada será concluída. Caso contrário, a chamada falhará. Uma maneira melhor de verificar se o servidor está em execução é invocar [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), seguido de uma chamada para [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening). Para obter mais informações sobre o nome de banco de dados do serviço, consulte [o banco de dados do serviço de nome RPC](the-rpc-name-service-database.md).

 

 




