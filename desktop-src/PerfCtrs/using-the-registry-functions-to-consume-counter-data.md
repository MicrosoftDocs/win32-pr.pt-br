---
description: Você pode usar as funções de registro para coletar dados de desempenho.
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: Usando as funções de registro para consumir dados de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 69f64f6e4cb44dd98d4f5097ca791054cd04c7e07219dc0e270cbfdff4cdbdc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033116"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>Usando as funções de registro para consumir dados de contador

Use as [funções de registro](/windows/desktop/SysInfo/registry-functions) para coletar dados de desempenho da `HKEY_PERFORMANCE_DATA` chave do registro especial.

Os dados de desempenho não são realmente armazenados no registro. Chamar as funções de registro faz com que o sistema colete os dados do provedor de dados de desempenho apropriado.

> [!Note]
> Normalmente, você não deve usar as funções de registro para consumir dados do contador. Em vez disso, você deve [usar as funções de PDH (auxiliar de dados de desempenho)](using-the-pdh-functions-to-consume-counter-data.md). As funções de PDH são mais fáceis de usar e evitam muitos problemas de desempenho e confiabilidade que podem ocorrer por meio do uso incorreto das funções de registro.

> [!Note]
> você não poderá usar as funções de registro se estiver gravando Windows OneCore aplicativos. Em vez disso, use as [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).

As funções de registro são a API de nível baixo para coletar dados de **provedores v1**. As funções de registro também dão suporte à coleta de dados de **provedores v2** por meio de uma camada de conversão que chama as [funções de consumidor v2](using-the-perflib-functions-to-consume-counter-data.md).

Para obter dados de desempenho do sistema local, chame a função [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) . Use `HKEY_PERFORMANCE_DATA` como a chave. A primeira chamada abre a chave. Você não precisa abrir a chave explicitamente primeiro.

Para obter dados de desempenho de um sistema remoto, chame a função [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) . Use o nome do computador do sistema remoto e use `HKEY_PERFORMANCE_DATA` como a chave. Essa chamada recupera uma chave que representa os dados de desempenho para o sistema remoto. Use essa chave em vez `HKEY_PERFORMANCE_DATA` da chave para recuperar os dados.

Certifique-se de usar a função [**falha RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) para fechar o identificador para a chave quando terminar de obter os dados de desempenho. Isso é importante para os casos local e remoto:

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` na verdade, não fecha um identificador de registro, mas apaga todos os dados armazenados em cache e libera as DLLs de desempenho carregadas.
- `RegCloseKey(hkeyRemotePerformanceData)` Fecha o identificador para o registro do computador remoto.

> [!IMPORTANT]
> Não chame `RegCloseKey(HKEY_PERFORMANCE_DATA)` durante `DLL_PROCESS_DETACH` .

Use o `lpValueName` parâmetro da função [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) para indicar as informações a serem recuperadas. A tabela a seguir lista os valores que você pode especificar para `lpValueName` . Observe que as cadeias de caracteres de valor não diferenciam maiúsculas de minúsculas.

|Valor|Descrição
|-----|-----------
|`Global`| Recupera dados de desempenho para todos os objetos de desempenho registrados no computador, exceto aqueles incluídos na `Costly` categoria.
|`OLD_Global`| **Windows Vista e posterior:** Recupera dados de desempenho para todos os objetos de desempenho **v1** registrados no computador, exceto aqueles incluídos na `Costly` categoria. Use isso em vez de `Global` para evitar a coleta de dados de provedor v2 desnecessários quando você sabe que os dados de interesse vêm de um provedor v1.
|`n1 n2 ...`| Recupera dados de desempenho para um ou mais objetos de desempenho. Especifique o índice decimal associado a cada objeto que você deseja recuperar em uma lista separada por espaços. Por exemplo, se você quiser recuperar objetos de sistema e memória e tiver determinado que os índices das cadeias de caracteres de nome correspondentes são 2 e 4, especifique a cadeia de caracteres `"2 4"` . Observe que a consulta pode retornar um número diferente de objetos que você solicitou. Isso pode acontecer se o objeto especificado não estiver disponível, se o objeto especificado depender de outro tipo de objeto ou se um provedor retornar dados que não foram solicitados diretamente. Por exemplo, os threads dependem de processos, portanto, se você solicitar dados do `Thread` objeto, os resultados incluirão dados do `Process` objeto.
|`Counter n`| Recupera cadeias de caracteres de nome para o identificador de idioma especificado, por exemplo, inglês para `Counter 9` . Use as cadeias de caracteres de nome retornadas para localizar o índice correspondente a um determinado nome ou para localizar o nome correspondente a um determinado índice. Consulte [recuperando nomes de contadores e texto de ajuda](retrieving-counter-names-and-help-text.md) para obter detalhes. Observe que a lista retornada inclui nomes de objeto (CounterSet) e nomes de contadores – não há uma maneira simples de determinar se um nome é um nome de objeto ou um nome de contador.
|`Help n`| Recupera cadeias de caracteres de ajuda para o identificador de idioma especificado, por exemplo, inglês para `Help 9` . Use as cadeias de caracteres de ajuda retornadas para localizar descrições correspondentes aos índices de objeto (CounterSet) ou de ajuda do contador. Consulte [recuperando nomes de contadores e texto de ajuda](retrieving-counter-names-and-help-text.md) para obter detalhes.
|`Costly`| **Preterido:** Recupera dados de desempenho para tipos de objetos cujos dados são caros para coletar em termos de tempo de processador ou uso de memória. Essa coleção pode levar vários minutos em um computador muito carregado. Você deve executar a coleção em um thread de trabalho se seu aplicativo precisar responder ao usuário durante essa coleta de dados.

Para obter detalhes sobre o formato dos dados de desempenho que o registro retorna, consulte [formato de dados de desempenho](performance-data-format.md).

Para obter um exemplo que obtém os nomes e as descrições dos contadores registrados no computador, consulte [recuperando nomes de contadores e texto de ajuda](retrieving-counter-names-and-help-text.md).

Para obter um exemplo que acessa os componentes dos dados de desempenho, consulte [exibindo nomes de objeto, instância e contador](displaying-object-instance-and-counter-names.md).

Para obter um exemplo que recupera, computa e imprime valores de contadores, consulte [recuperando dados de contador](retrieving-counter-data.md) e [calculando valores de contador](calculating-counter-values.md).
