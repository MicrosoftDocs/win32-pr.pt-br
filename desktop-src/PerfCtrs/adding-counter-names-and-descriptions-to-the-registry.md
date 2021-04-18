---
description: Os nomes e descrições de todos os objetos de desempenho e seus contadores são armazenados no registro.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Adição de nomes e descrições de contadores ao Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753110"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Adição de nomes e descrições de contadores ao Registro

> [!IMPORTANT]
> Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use o método descrito em [fornecendo dados de contador usando a versão 2,0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e migrar contadores de desempenho existentes para usar esse método.

Os nomes e descrições de todos os objetos de desempenho v1 e seus contadores devem ser instalados no sistema. Para armazenar nomes e descrições para os objetos e contadores do seu [provedor v1](providing-counter-data.md):

- [Crie um arquivo de cabeçalho. h](#creating-a-symbolic-constants-h-file) que contenha as constantes simbólicas para os deslocamentos para seus objetos e contadores.
- [Criar uma inicialização (. INI)](#creating-an-initialization-ini-file) que contém as cadeias de caracteres.
- Ao instalar o componente, [Execute a ferramenta **lodctr**](#running-the-lodctr-tool) para instalar os nomes e as descrições no registro.
- Ao desinstalar o componente, execute a ferramenta Unlodctr para remover os nomes e as descrições do registro.

## <a name="creating-a-symbolic-constants-h-file"></a>Criando um arquivo de constantes simbólicas (. h)

Crie um arquivo de cabeçalho. h que define constantes (macros) para os deslocamentos para os objetos e contadores que seu provedor fornece. O cabeçalho. h é usado como entrada para **lodctr** durante a instalação do seu provedor e também pode ser usado pelo código C/C++ do seu provedor.

Os valores constantes devem ser consecutivos, até números que começam com zero. Agrupe as constantes por objetos (ou seja, inicie cada grupo com o deslocamento do objeto e, em seguida, siga com os deslocamentos dos contadores para esse objeto).

As constantes no cabeçalho determinam a ordem na qual os contadores são adicionados ao nome e ao texto de ajuda no registro. O provedor usa os deslocamentos para determinar qual objeto está sendo consultado e os valores de índice a serem usados ao retornar os dados. Para obter detalhes, consulte [implementando OpenPerformanceData](implementing-openperformancedata.md).

Veja a seguir um exemplo de um arquivo constante simbólico, chamado comoffsets. h, que é usado no exemplo [criando um DLL de extensão de desempenho](creating-a-performance-extension-dll.md) .

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

## <a name="creating-an-initialization-ini-file"></a>Criando uma inicialização (. INI)

A inicialização (. INI) contém as cadeias de caracteres de nome e de ajuda para cada objeto e contador definidos no arquivo de símbolo. Dos. O arquivo INI é usado como entrada para **lodctr** durante a instalação do seu provedor.

Dos. O arquivo INI deve ser codificado como UTF-16LE (com a marca de ordem de byte) e deve ter as seguintes seções e chaves:

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

### <a name="info-section"></a>seção [informações]

A `[info]` seção contém informações gerais sobre o provedor. As chaves de seção são definidas da seguinte maneira:

|Chave|Descrição
|---|-----------
|**DriverName**| Especifique o nome da chave de desempenho do provedor localizada no registro sob a `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` chave. Para obter informações sobre como criar essa chave, consulte [criando a chave de desempenho do aplicativo](creating-the-applications-performance-key.md).
|**Símbolo de**| Especifique o arquivo de cabeçalho. h que contém valores simbólicos dos objetos e contadores do seu provedor. Durante a instalação (ao invocar **lodctr**), o arquivo de cabeçalho deve estar no mesmo diretório que o. Arquivo INI.
|**Confiável**| Se você incluir essa chave na `[info]` seção, **lodctr** adicionará um valor de registro de código de validação de biblioteca à sua chave de desempenho com uma assinatura binária de sua DLL de desempenho. Quando o PERFLIB chama sua DLL, ele compara a assinatura com sua DLL para determinar se a DLL foi modificada. O valor da chave **confiável** é ignorado.

As `DriverName` `SymbolFile` chaves e são obrigatórias.

### <a name="objects-section"></a>seção [objetos]

A `[objects]` seção fornece uma lista dos objetos de desempenho aos quais o provedor dá suporte. Isso é usado para determinar se cada símbolo da `[text]` seção refere-se a um objeto ou um contador.

Para cada objeto (CounterSet) com suporte pelo seu provedor, adicione uma chave chamada `<symbol>_<langid>_NAME=` à `[objects]` seção, em que `<symbol>` é o nome do objeto e `<langid>` é a ID de idioma de um dos idiomas com suporte. O valor é ignorado.

> [!IMPORTANT]
> A `[objects]` seção melhora o desempenho do sistema. Embora a seção objetos seja opcional, você sempre deve incluir esta seção no seu. Arquivo INI. Se você incluir esta seção, sua DLL de desempenho será chamada somente se você oferecer suporte ao objeto solicitado. Se você não incluir a seção objetos, sua DLL será chamada para cada consulta porque o sistema não sabe a quais objetos seu provedor dá suporte. Se a seção de objeto não for incluída, **lodctr** gerará uma mensagem no log de eventos do aplicativo informando que o. O arquivo INI não continha uma seção Objects. O identificador de evento dessa mensagem é 2000.

### <a name="languages-section"></a>seção [Idiomas]

A `[languages]` seção fornece uma lista dos identificadores de idioma de cada idioma para o qual seu provedor fornece o nome e as cadeias de caracteres de ajuda. Todos os provedores devem dar suporte a `009` (inglês).

Para cada idioma com suporte, adicione uma chave chamada `<langid>=` . O valor é ignorado, mas para fins de documentação, o valor normalmente é definido como o nome do idioma correspondente, por exemplo, `009=English` .

Para a maioria dos idiomas, você deve usar o identificador de idioma primário. A lista completa de identificadores de idioma está no arquivo de cabeçalho WinNT. h, sob o título "IDs de idioma primário". Converta o valor encontrado em Winnt. h em uma sequência de 3 dígitos hexadecimais removendo o `0x` prefixo e adicionando os dígitos à esquerda `0` até que a sequência tenha 3 dígitos de comprimento. Por exemplo, para especificar cadeias de caracteres em inglês (0x9), use 009. Para especificar as cadeias de caracteres italianas (0x10), use 010.

Os idiomas chinês e Português exigem os identificadores primário e subidioma. Use 404, 804, 416 ou 816 em vez de 004 ou 016.

### <a name="text-section"></a>seção [texto]

A `[text]` seção fornece as cadeias de caracteres de nome e de ajuda para seus objetos e contadores.

Para cada objeto ou contador, e para cada idioma com suporte, você deve fornecer uma chave de nome (contendo o nome ou a cadeia de caracteres de título para o objeto ou contador) e, opcionalmente, fornecer uma chave de ajuda (que contém a descrição ou a cadeia de caracteres de explicação para o objeto ou contador). As chaves devem ser nomeadas `<symbol>_<langid>_NAME` e `<symbol>_<langid>_HELP` , em que `<symbol>` é a constante simbólica para o objeto ou contador (conforme definido no arquivo constante. h do simbólico) e `<langid>` é o identificador de idioma usado para esta cadeia de caracteres.

Por exemplo, as cadeias de caracteres em inglês para um contador com símbolo `MY_COUNTER` seriam especificadas como:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

As chaves de texto podem aparecer em qualquer ordem. As cadeias de texto não devem conter caracteres de formatação, como guias.

### <a name="example-ini-file"></a>Arquivo INI de exemplo

Veja a seguir um exemplo de um arquivo de inicialização que é usado no exemplo [criando uma DLL de extensão de desempenho](creating-a-performance-extension-dll.md) .

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

## <a name="running-the-lodctr-tool"></a>Executando a ferramenta LodCtr

Para carregar os nomes e as cadeias de caracteres de ajuda definidas no seu. Arquivo INI (durante a instalação do seu provedor), execute a ferramenta **lodctr** na pasta que contém o. Arquivo INI e arquivo de cabeçalho. A ferramenta está incluída no computador. Você deve executar o **lodctr** com privilégios elevados. O parâmetro para **lodctr** é o caminho para o. Arquivo INI. Por exemplo, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Para descarregar os nomes e as cadeias de caracteres de ajuda (durante a desinstalação), execute a ferramenta **Unlodctr** . Você deve executar o **Unlodctr** com privilégios elevados. O parâmetro para **Unlodctr** é o DriverName do seu provedor (o nome da chave de desempenho do provedor). Por exemplo, `unlodctr "MyProvider"`.

Antes de executar **lodctr**, certifique-se de que seu aplicativo tem uma entrada sob a chave de **Serviços** . Para obter detalhes, consulte [criando a chave de desempenho do aplicativo](creating-the-applications-performance-key.md). Se a chave não existir, **lodctr** não atualizará o registro com seus nomes e descrições.

Como alternativa à execução de **lodctr**, você pode chamar [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definido em LoadPerf. h) de seu programa de instalação para carregar as descrições de nomes de contadores. Em seguida, você pode chamar [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) durante a desinstalação.

O utilitário **lodctr** copia as cadeias de caracteres do. INI para os **contadores** e os valores de registro da **ajuda** nas subchaves de idioma apropriadas. Se a subchave de idioma correspondente não existir, as cadeias de caracteres desse idioma não serão copiadas. O utilitário também atualiza o **último contador** e o último valor de **ajuda** . Os nomes e as descrições do contador de desempenho são armazenados no seguinte local no registro.

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

Além de adicionar valores sob a chave **PerfLib** , a ferramenta **lodctr** também adiciona os valores a seguir ao nó de **Serviços** para o aplicativo. Na maioria dos casos, o aplicativo e o provedor terão uma relação um-para-um; no entanto, é possível que um provedor forneça dados de contador para vários aplicativos, motivo pelo qual a chave é baseada no aplicativo e não no provedor.

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
