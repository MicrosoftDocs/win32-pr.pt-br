---
description: Os logs de eventos armazenam registros de eventos significativos em nome do sistema e aplicativos em execução no sistema.
ms.assetid: 58a6569a-2775-4687-bf99-579fa4153191
title: Diretrizes de registro em log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1210757a7961d82d13d4887e40fbd3837b86138
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091454"
---
# <a name="logging-guidelines"></a>Diretrizes de registro em log

Os logs de eventos armazenam registros de eventos significativos em nome do sistema e aplicativos em execução no sistema. Como as funções de log são de uso geral, você deve decidir quais informações são apropriadas para o log. Em geral, você deve registrar apenas informações que podem ser úteis para diagnosticar um problema de hardware ou software. O log de eventos não se destina a ser usado como uma ferramenta de rastreamento.

## <a name="choosing-events-to-log"></a>Escolhendo eventos para registrar

Veja a seguir exemplos de casos em que o log de eventos pode ser útil:

-   Problemas de recursos. O registro em log de um evento de aviso quando a alocação de memória falha pode ajudar a indicar a causa de uma situação de baixa memória.
-   Problemas de hardware. Se um driver de dispositivo encontrar um tempo limite de controlador de disco, uma falha de energia em uma porta paralela ou um erro de dados de uma rede ou placa serial, o driver de dispositivo poderá registrar informações sobre esses eventos para ajudar o administrador do sistema a diagnosticar problemas de hardware.
-   Setores inválidos. Se um driver de disco encontrar um setor insatisfatório, ele poderá ser capaz de ler ou gravar no setor depois de repetir a operação, mas o setor vai ser inadequado eventualmente. Se o driver de disco puder continuar, ele deverá registrar um evento de aviso; caso contrário, ele deve registrar um evento de erro. Se um driver de sistema de arquivos encontrar um grande número de setores defeituosos e os corrigir, o log de eventos de aviso poderá ajudar um administrador a determinar que o disco pode estar prestes a falhar.
-   Eventos de informações. Um aplicativo de servidor (como um servidor de banco de dados) registra um logon de usuário, abrindo um banco de dados ou iniciando uma transferência de arquivo. O servidor também pode registrar outros eventos, como erros (não é possível acessar o arquivo, processo de host desconectado e assim por diante), corrupção de banco de dados ou se uma transferência de arquivo foi bem-sucedida.

## <a name="writing-messages"></a>Gravando mensagens

As mensagens devem fazer sentido para administradores e usuários que estão tentando solucionar um problema. Uma mensagem deve conter todas as informações necessárias para entender o que causou o problema e como corrigi-lo.

Evite escrever uma mensagem criptografada, como "um pacote de driver recebido do subsistema de e/s era inválido. Os dados são o pacote. " Uma mensagem melhor indicaria que o driver em questão está funcionando corretamente, mas está registrando em log os pacotes formatados incorretamente. Ele pode continuar a dizer que uma versão Unicode do driver é necessária para corrigir o problema. Para obter mais informações sobre como escrever boas mensagens de erro, consulte [diretrizes de mensagem de erro](/windows/desktop/Debug/error-message-guidelines).

Não use tabulações ou vírgulas no texto da mensagem, porque os logs de eventos podem ser salvos como arquivos de texto separados por vírgula ou por tabulação. Muitas organizações importam esses arquivos em bancos de dados e os caracteres de formatação extras exigirão a manipulação manual.

Ao usar nomes UNC ou outros links que contenham espaços, coloque o nome entre colchetes angulares. Por exemplo, <\\ \\ *ShareName* \\ *ServerName*>. Você pode gravar uma URL no final da mensagem que aponta o usuário para o material de ajuda relacionado. A URL deve ser um nome de host DNS totalmente qualificado. Por exemplo, você pode acrescentar o seguinte texto às suas mensagens: "para obter mais informações sobre esta mensagem, visite nosso site de suporte em https://www.microsoft.com/Support/ProdRedirect/ContentSearch.asp ." O link levaria a uma página ASP que redireciona o usuário para o conteúdo relacionado à mensagem de erro. Ele analisaria parâmetros adicionais (passados quando a URL é clicada) para determinar onde redirecionar o usuário.

Os argumentos passados para a função [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) são acrescentados à URL da seguinte maneira:

``` syntax
strHTTPQuery += L"?EvtSrc=" + _strEscapedSource;
strHTTPQuery += L"&EvtCat=" + _strEscapedCategory;
strHTTPQuery += L"&EvtID=" + _strEscapedEventID;
strHTTPQuery += L"&EvtCatID=" + _strEscapedCategoryID;
strHTTPQuery += L"&EvtType=" + _strEscapedType;
strHTTPQuery += L"&EvtTypeID=" + _strEscapedTypeID;
strHTTPQuery += L"&EvtRptTime=" + _strEscapedDateAndTime;
strHTTPQuery += L"&EvtTZBias=" + _strEscapedTimeZoneBias;
```

Se o nome da empresa, o nome do produto, a versão do produto, o nome do arquivo e a versão do arquivo do cabeçalho DLL da mensagem para a origem do evento forem válidos, eles também serão anexados à URL:

``` syntax
ADD_VER_STR(L"CoName",   _strEscapedCompanyName);
ADD_VER_STR(L"ProdName", _strEscapedProductName);
ADD_VER_STR(L"ProdVer",  _strEscapedProductVersion);
ADD_VER_STR(L"FileName", _strEscapedFileName);
ADD_VER_STR(L"FileVer",  _strEscapedFileVersion);
```

## <a name="reducing-overhead"></a>Reduzindo a sobrecarga

O log de eventos consome recursos como espaço em disco e tempo do processador. A quantidade de espaço em disco que um log de eventos requer e a sobrecarga para um aplicativo que registra os eventos dependem da quantidade de informações que você escolhe registrar. É por isso que é importante registrar apenas informações essenciais. Também é bom colocar chamadas de log de eventos em um caminho de erro no código, e não no caminho de código principal, o que reduziria o desempenho.

A quantidade de espaço em disco necessária para cada registro de log de eventos inclui os membros da estrutura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . Esta é uma estrutura de comprimento variável; cadeias de caracteres e dados binários são armazenados após a estrutura.

 

 
