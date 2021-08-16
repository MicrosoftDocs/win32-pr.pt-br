---
description: Os nomes e as descrições de todos os objetos de desempenho e seus contadores são armazenados no Registro.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Adição de nomes e descrições de contadores ao Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58333e9694b9aa74ff1d5ade6a399aaa813e7735ea315be529587e813fec0fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794051"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Adição de nomes e descrições de contadores ao Registro

> [!IMPORTANT]
> Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use o método descrito em Fornecendo dados de contador usando a versão [2.0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e que você migre contadores de desempenho existentes para usar esse método.

Os nomes e descrições de todos os objetos de desempenho V1 e seus contadores devem ser instalados no sistema. Para armazenar nomes e descrições para os objetos e contadores do seu [provedor V1:](providing-counter-data.md)

- [Crie um arquivo de título .h que](#creating-a-symbolic-constants-h-file) contém as constantes simbólicas para os deslocamentos para seus objetos e contadores.
- [Crie um arquivo de inicialização (.INI)](#creating-an-initialization-ini-file) que contém as cadeias de caracteres.
- Ao instalar o componente, [execute a **ferramenta lodctr**](#running-the-lodctr-tool) para instalar os nomes e as descrições no Registro.
- Ao desinstalar o componente, execute a ferramenta unlodctr para remover os nomes e descrições do Registro.

## <a name="creating-a-symbolic-constants-h-file"></a>Criando um arquivo de constantes simbólicas (.h)

Crie um arquivo de header .h que define constantes (macros) para os deslocamentos para os objetos e contadores que seu provedor fornece. O header .h é usado como entrada para **lodctr** durante a instalação do seu provedor e também pode ser usado pelo código C/C++ do seu provedor.

Os valores constantes devem ser consecutivos, até mesmo números começando com zero. A agrupar as constantes por objetos (ou seja, iniciar cada grupo com o deslocamento do objeto e, em seguida, seguir com os deslocamentos dos contadores para esse objeto).

As constantes no header determinam a ordem na qual os contadores são adicionados ao nome e ao texto de ajuda no Registro. O provedor usa os deslocamentos para determinar qual objeto está sendo consultado e os valores de índice a serem usado ao retornar os dados. Para obter detalhes, [consulte Implementando OpenPerformanceData](implementing-openperformancedata.md).

O exemplo a seguir mostra um exemplo de um arquivo constante simbólico, chamado CounterOffsets.h, que é usado no exemplo criar uma [DLL de extensão de](creating-a-performance-extension-dll.md) desempenho.

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a>Criando um arquivo de inicialização (.INI)

O arquivo de inicialização (.INI) contém o nome e as cadeias de caracteres de ajuda para cada objeto e contador definidos no arquivo de símbolo. O .INI é usado como entrada para **lodctr durante** a instalação do provedor.

O .INI deve ser codificado como UTF-16LE (com marca de ordem de byte) e deve ter as seguintes seções e chaves:

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a>Seção [info]

A `[info]` seção contém informações gerais sobre o provedor. As chaves da seção são definidas da seguinte forma:

|Chave|Descrição
|---|-----------
|**Drivername**| Especifique o nome da chave de desempenho do provedor localizada no Registro sob a `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` chave. Para obter informações sobre como criar essa chave, consulte [Criando a chave de desempenho do aplicativo.](creating-the-applications-performance-key.md)
|**SymbolFile**| Especifique o arquivo de título .h que contém valores simbólicos dos objetos e contadores do provedor. Durante a instalação (ao invocar **lodctr),** o arquivo de .INI deve estar no mesmo diretório.
|**Confiável**| Se você incluir essa chave na seção , lodctr adicionará um valor de Registro de Código de Validação de Biblioteca à sua chave de desempenho com uma assinatura binária da `[info]` DLL de  desempenho. Quando PERFLIB chama sua DLL, ele compara a assinatura com sua DLL para determinar se a DLL foi modificada. O valor da **chave Confiável** é ignorado.

As `DriverName` chaves e são `SymbolFile` necessárias.

### <a name="objects-section"></a>Seção [objetos]

A `[objects]` seção fornece uma lista dos objetos de desempenho compatíveis com o provedor. Isso é usado para determinar se cada símbolo da `[text]` seção se refere a um objeto ou um contador.

Para cada objeto (counterset) com suporte pelo provedor, adicione uma chave chamada à seção , em que é o nome do objeto e é a ID de idioma de um dos idiomas com `<symbol>_<langid>_NAME=` `[objects]` `<symbol>` `<langid>` suporte. O valor é ignorado.

> [!IMPORTANT]
> A `[objects]` seção melhora o desempenho do sistema. Embora a seção de objetos seja opcional, você sempre deve incluir esta seção no arquivo .INI dados. Se você incluir esta seção, sua DLL de desempenho será chamada somente se você dar suporte ao objeto solicitado. Se você não incluir a seção de objetos, sua DLL será chamada para cada consulta porque o sistema não sabe a quais objetos seu provedor dá suporte. Se a seção de objeto não estiver incluída, **lodctr** gerará uma mensagem no log de eventos do aplicativo informando que o arquivo .INI não continha uma seção de objetos. O identificador de evento dessa mensagem é 2000.

### <a name="languages-section"></a>Seção [idiomas]

A seção fornece uma lista dos identificadores de idioma de cada idioma para o qual seu provedor fornece cadeias de caracteres de `[languages]` nome e ajuda. Todos os provedores devem dar suporte `009` (inglês).

Para cada idioma com suporte, adicione uma chave chamada `<langid>=` . O valor é ignorado, mas para fins de documentação, o valor normalmente é definido como o nome do idioma correspondente, por exemplo, `009=English` .

Para a maioria dos idiomas, você deve usar o identificador de idioma primário. A lista completa de identificadores de idioma está no arquivo de título Winnt.h, sob o título "IDs de idioma primário". Converta o valor encontrado em Winnt.h em uma sequência de três dígitos hexadecimais removendo o prefixo e adicionando dígitos à frente até que a sequência tenha `0x` `0` três dígitos. Por exemplo, para especificar cadeias de caracteres em inglês (0x9), use 009. Para especificar cadeias de caracteres italianos (0x10), use 010.

Os idiomas chinês e português exigem os identificadores primário e de sublânguo. Use 404, 804, 416 ou 816 em vez de 004 ou 016.

### <a name="text-section"></a>Seção [texto]

A `[text]` seção fornece as cadeias de caracteres de nome e ajuda para seus objetos e contadores.

Para cada objeto ou contador e para cada idioma com suporte, você deve fornecer uma chave NAME (que contém o nome ou a cadeia de caracteres de título para seu objeto ou contador) e, opcionalmente, você pode fornecer uma chave HELP (que contém a descrição ou a cadeia de caracteres de explicação para seu objeto ou contador). As chaves devem ser nomeadas e , em que é a constante simbólica para o objeto ou contador (conforme definido no arquivo .h constante simbólico) e é o identificador de idioma usado para essa cadeia de `<symbol>_<langid>_NAME` `<symbol>_<langid>_HELP` `<symbol>` `<langid>` caracteres.

Por exemplo, as cadeias de caracteres em inglês para um contador com `MY_COUNTER` símbolo seriam especificadas como:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

As chaves de texto podem aparecer em qualquer ordem. As cadeias de caracteres de texto não devem conter caracteres de formatação, como guias.

### <a name="example-ini-file"></a>Exemplo de arquivo INI

A seguir está um exemplo de um arquivo de inicialização que é usado no exemplo [criando uma DLL de extensão de](creating-a-performance-extension-dll.md) desempenho.

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a>Executando a ferramenta Lodctr

Para carregar os nomes e as cadeias de caracteres de ajuda definidas no arquivo .INI (durante a instalação do provedor), execute a ferramenta **lodctr** da pasta que contém o arquivo .INI e o arquivo de header. A ferramenta está incluída no computador. Você deve executar **lodctr** com privilégios elevados. O parâmetro a **lodctr** é o caminho para o arquivo .INI arquivo. Por exemplo, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Para descarregar os nomes e as cadeias de caracteres de ajuda (durante a desinstalação), execute a **ferramenta unlodctr.** Você deve executar **unlodctr** com privilégios elevados. O parâmetro para **unlodctr** é o DriverName do seu provedor (o nome da chave de desempenho do provedor). Por exemplo, `unlodctr "MyProvider"`.

Antes de **executar lodctr**, certifique-se de que seu aplicativo tenha uma entrada sob a **chave Serviços.** Para obter detalhes, [consulte Criando a chave de desempenho do aplicativo.](creating-the-applications-performance-key.md) Se a chave não existir, **lodctr** não atualizará o Registro com seus nomes e descrições.

Como alternativa à execução **do lodctr**, você pode chamar [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definido em Loadperf.h) do programa de instalação para carregar as descrições dos nomes do contador. Em seguida, você [**pode chamar UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) durante a desinstalação.

O **utilitário lodctr** copia as cadeias de caracteres do  arquivo .INI para os valores do registro **Contadores** e Ajuda nas sub-chaves de idioma apropriadas. Se a sub-chave de idioma correspondente não existir, as cadeias de caracteres desse idioma não serão copiadas. O utilitário também atualiza o **valor do Último Contador** e da Última **Ajuda.** Os nomes e as descrições do contador de desempenho são armazenados no seguinte local no Registro.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

Além de adicionar valores sob a chave **PerfLib,** a ferramenta **lodctr** também adiciona os seguintes valores ao **nó** Serviços para o aplicativo. Na maioria dos casos, o aplicativo e o provedor terão uma relação um-para-um; No entanto, é possível que um provedor forneça dados de contador para vários aplicativos, por isso a chave é baseada no aplicativo e não no provedor.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
