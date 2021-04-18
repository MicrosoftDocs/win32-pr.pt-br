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
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a><span data-ttu-id="654e6-103">Adição de nomes e descrições de contadores ao Registro</span><span class="sxs-lookup"><span data-stu-id="654e6-103">Adding Counter Names and Descriptions to the Registry</span></span>

> [!IMPORTANT]
> <span data-ttu-id="654e6-104">Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="654e6-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="654e6-105">Em vez disso, a Microsoft recomenda que você use o método descrito em [fornecendo dados de contador usando a versão 2,0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e migrar contadores de desempenho existentes para usar esse método.</span><span class="sxs-lookup"><span data-stu-id="654e6-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters and that you migrate existing performance counters to use that method.</span></span>

<span data-ttu-id="654e6-106">Os nomes e descrições de todos os objetos de desempenho v1 e seus contadores devem ser instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="654e6-106">The names and descriptions of all V1 performance objects and their counters must be installed the system.</span></span> <span data-ttu-id="654e6-107">Para armazenar nomes e descrições para os objetos e contadores do seu [provedor v1](providing-counter-data.md):</span><span class="sxs-lookup"><span data-stu-id="654e6-107">To store names and descriptions for the objects and counters from your [V1 provider](providing-counter-data.md):</span></span>

- <span data-ttu-id="654e6-108">[Crie um arquivo de cabeçalho. h](#creating-a-symbolic-constants-h-file) que contenha as constantes simbólicas para os deslocamentos para seus objetos e contadores.</span><span class="sxs-lookup"><span data-stu-id="654e6-108">[Create a .h header file](#creating-a-symbolic-constants-h-file) that contains the symbolic constants for the offsets to your objects and counters.</span></span>
- <span data-ttu-id="654e6-109">[Criar uma inicialização (. INI)](#creating-an-initialization-ini-file) que contém as cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="654e6-109">[Create an initialization (.INI) file](#creating-an-initialization-ini-file) that contains the strings.</span></span>
- <span data-ttu-id="654e6-110">Ao instalar o componente, [Execute a ferramenta **lodctr**](#running-the-lodctr-tool) para instalar os nomes e as descrições no registro.</span><span class="sxs-lookup"><span data-stu-id="654e6-110">When installing your component, [run the **lodctr** tool](#running-the-lodctr-tool) to install the names and descriptions into the registry.</span></span>
- <span data-ttu-id="654e6-111">Ao desinstalar o componente, execute a ferramenta Unlodctr para remover os nomes e as descrições do registro.</span><span class="sxs-lookup"><span data-stu-id="654e6-111">When uninstalling your component, run the unlodctr tool to remove the names and descriptions from the registry.</span></span>

## <a name="creating-a-symbolic-constants-h-file"></a><span data-ttu-id="654e6-112">Criando um arquivo de constantes simbólicas (. h)</span><span class="sxs-lookup"><span data-stu-id="654e6-112">Creating a symbolic constants (.h) file</span></span>

<span data-ttu-id="654e6-113">Crie um arquivo de cabeçalho. h que define constantes (macros) para os deslocamentos para os objetos e contadores que seu provedor fornece.</span><span class="sxs-lookup"><span data-stu-id="654e6-113">Create a .h header file that defines constants (macros) for the offsets to the objects and counters that your provider provides.</span></span> <span data-ttu-id="654e6-114">O cabeçalho. h é usado como entrada para **lodctr** durante a instalação do seu provedor e também pode ser usado pelo código C/C++ do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="654e6-114">The .h header is used as input to **lodctr** during installation of your provider, and may also be used by the C/C++ code of your provider.</span></span>

<span data-ttu-id="654e6-115">Os valores constantes devem ser consecutivos, até números que começam com zero.</span><span class="sxs-lookup"><span data-stu-id="654e6-115">The constant values must be consecutive, even numbers beginning with zero.</span></span> <span data-ttu-id="654e6-116">Agrupe as constantes por objetos (ou seja, inicie cada grupo com o deslocamento do objeto e, em seguida, siga com os deslocamentos dos contadores para esse objeto).</span><span class="sxs-lookup"><span data-stu-id="654e6-116">Group the constants by objects (i.e. start each group with the object offset, then follow with the offsets of the counters for that object).</span></span>

<span data-ttu-id="654e6-117">As constantes no cabeçalho determinam a ordem na qual os contadores são adicionados ao nome e ao texto de ajuda no registro.</span><span class="sxs-lookup"><span data-stu-id="654e6-117">The constants in the header determine the order in which the counters are added to the name and help text in the registry.</span></span> <span data-ttu-id="654e6-118">O provedor usa os deslocamentos para determinar qual objeto está sendo consultado e os valores de índice a serem usados ao retornar os dados.</span><span class="sxs-lookup"><span data-stu-id="654e6-118">The provider uses the offsets to determine which object is being queried and the index values to use when returning the data.</span></span> <span data-ttu-id="654e6-119">Para obter detalhes, consulte [implementando OpenPerformanceData](implementing-openperformancedata.md).</span><span class="sxs-lookup"><span data-stu-id="654e6-119">For details, see [Implementing OpenPerformanceData](implementing-openperformancedata.md).</span></span>

<span data-ttu-id="654e6-120">Veja a seguir um exemplo de um arquivo constante simbólico, chamado comoffsets. h, que é usado no exemplo [criando um DLL de extensão de desempenho](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="654e6-120">The following shows an example of a symbolic constant file, named CounterOffsets.h, that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) example.</span></span>

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

## <a name="creating-an-initialization-ini-file"></a><span data-ttu-id="654e6-121">Criando uma inicialização (. INI)</span><span class="sxs-lookup"><span data-stu-id="654e6-121">Creating an initialization (.INI) file</span></span>

<span data-ttu-id="654e6-122">A inicialização (. INI) contém as cadeias de caracteres de nome e de ajuda para cada objeto e contador definidos no arquivo de símbolo.</span><span class="sxs-lookup"><span data-stu-id="654e6-122">The initialization (.INI) file contains the name and help strings for each object and counter defined in your symbol file.</span></span> <span data-ttu-id="654e6-123">Dos. O arquivo INI é usado como entrada para **lodctr** durante a instalação do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="654e6-123">The .INI file is used as input to **lodctr** during installation of your provider.</span></span>

<span data-ttu-id="654e6-124">Dos. O arquivo INI deve ser codificado como UTF-16LE (com a marca de ordem de byte) e deve ter as seguintes seções e chaves:</span><span class="sxs-lookup"><span data-stu-id="654e6-124">The .INI file should be encoded as UTF-16LE (with byte order mark) and should have the following sections and keys:</span></span>

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

### <a name="info-section"></a><span data-ttu-id="654e6-125">seção [informações]</span><span class="sxs-lookup"><span data-stu-id="654e6-125">[info] section</span></span>

<span data-ttu-id="654e6-126">A `[info]` seção contém informações gerais sobre o provedor.</span><span class="sxs-lookup"><span data-stu-id="654e6-126">The `[info]` section contains general information about the provider.</span></span> <span data-ttu-id="654e6-127">As chaves de seção são definidas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="654e6-127">The section keys are defined as follows:</span></span>

|<span data-ttu-id="654e6-128">Chave</span><span class="sxs-lookup"><span data-stu-id="654e6-128">Key</span></span>|<span data-ttu-id="654e6-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="654e6-129">Description</span></span>
|---|-----------
|<span data-ttu-id="654e6-130">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="654e6-130">**DriverName**</span></span>| <span data-ttu-id="654e6-131">Especifique o nome da chave de desempenho do provedor localizada no registro sob a `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` chave.</span><span class="sxs-lookup"><span data-stu-id="654e6-131">Specify the name of the provider's performance key located in the registry under the `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` key.</span></span> <span data-ttu-id="654e6-132">Para obter informações sobre como criar essa chave, consulte [criando a chave de desempenho do aplicativo](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="654e6-132">For information on creating this key, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span>
|<span data-ttu-id="654e6-133">**Símbolo de**</span><span class="sxs-lookup"><span data-stu-id="654e6-133">**SymbolFile**</span></span>| <span data-ttu-id="654e6-134">Especifique o arquivo de cabeçalho. h que contém valores simbólicos dos objetos e contadores do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="654e6-134">Specify the .h header file that contains symbolic values of your provider's objects and counters.</span></span> <span data-ttu-id="654e6-135">Durante a instalação (ao invocar **lodctr**), o arquivo de cabeçalho deve estar no mesmo diretório que o. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="654e6-135">During installation (when invoking **lodctr**), the header file must be in the same directory as the .INI file.</span></span>
|<span data-ttu-id="654e6-136">**Confiável**</span><span class="sxs-lookup"><span data-stu-id="654e6-136">**Trusted**</span></span>| <span data-ttu-id="654e6-137">Se você incluir essa chave na `[info]` seção, **lodctr** adicionará um valor de registro de código de validação de biblioteca à sua chave de desempenho com uma assinatura binária de sua DLL de desempenho.</span><span class="sxs-lookup"><span data-stu-id="654e6-137">If you include this key in the `[info]` section, **lodctr** will add a Library Validation Code registry value to your performance key with a binary signature of your performance DLL.</span></span> <span data-ttu-id="654e6-138">Quando o PERFLIB chama sua DLL, ele compara a assinatura com sua DLL para determinar se a DLL foi modificada.</span><span class="sxs-lookup"><span data-stu-id="654e6-138">When PERFLIB calls your DLL it compares the signature with your DLL to determine if the DLL has been modified.</span></span> <span data-ttu-id="654e6-139">O valor da chave **confiável** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="654e6-139">The value of the **Trusted** key is ignored.</span></span>

<span data-ttu-id="654e6-140">As `DriverName` `SymbolFile` chaves e são obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="654e6-140">The `DriverName` and `SymbolFile` keys are required.</span></span>

### <a name="objects-section"></a><span data-ttu-id="654e6-141">seção [objetos]</span><span class="sxs-lookup"><span data-stu-id="654e6-141">[objects] section</span></span>

<span data-ttu-id="654e6-142">A `[objects]` seção fornece uma lista dos objetos de desempenho aos quais o provedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="654e6-142">The `[objects]` section provides a list of the performance objects that the provider supports.</span></span> <span data-ttu-id="654e6-143">Isso é usado para determinar se cada símbolo da `[text]` seção refere-se a um objeto ou um contador.</span><span class="sxs-lookup"><span data-stu-id="654e6-143">This is used to determine whether each symbol from the `[text]` section refers an object or a counter.</span></span>

<span data-ttu-id="654e6-144">Para cada objeto (CounterSet) com suporte pelo seu provedor, adicione uma chave chamada `<symbol>_<langid>_NAME=` à `[objects]` seção, em que `<symbol>` é o nome do objeto e `<langid>` é a ID de idioma de um dos idiomas com suporte.</span><span class="sxs-lookup"><span data-stu-id="654e6-144">For each object (counterset) supported by your provider, add one key named `<symbol>_<langid>_NAME=` to the `[objects]` section, where `<symbol>` is the name of the object and `<langid>` is the language id of one of the supported languages.</span></span> <span data-ttu-id="654e6-145">O valor é ignorado.</span><span class="sxs-lookup"><span data-stu-id="654e6-145">The value is ignored.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="654e6-146">A `[objects]` seção melhora o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="654e6-146">The `[objects]` section improves the performance of the system.</span></span> <span data-ttu-id="654e6-147">Embora a seção objetos seja opcional, você sempre deve incluir esta seção no seu. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="654e6-147">Although the objects section is optional, you should always include this section in your .INI file.</span></span> <span data-ttu-id="654e6-148">Se você incluir esta seção, sua DLL de desempenho será chamada somente se você oferecer suporte ao objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="654e6-148">If you include this section, your performance DLL is called only if you support the requested object.</span></span> <span data-ttu-id="654e6-149">Se você não incluir a seção objetos, sua DLL será chamada para cada consulta porque o sistema não sabe a quais objetos seu provedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="654e6-149">If you do not include the objects section, your DLL is called for every query because the system does not know which objects your provider supports.</span></span> <span data-ttu-id="654e6-150">Se a seção de objeto não for incluída, **lodctr** gerará uma mensagem no log de eventos do aplicativo informando que o. O arquivo INI não continha uma seção Objects.</span><span class="sxs-lookup"><span data-stu-id="654e6-150">If the object section is not included, **lodctr** generates a message in the application event log stating that the .INI file did not contain an objects section.</span></span> <span data-ttu-id="654e6-151">O identificador de evento dessa mensagem é 2000.</span><span class="sxs-lookup"><span data-stu-id="654e6-151">The event identifier of this message is 2000.</span></span>

### <a name="languages-section"></a><span data-ttu-id="654e6-152">seção [Idiomas]</span><span class="sxs-lookup"><span data-stu-id="654e6-152">[languages] section</span></span>

<span data-ttu-id="654e6-153">A `[languages]` seção fornece uma lista dos identificadores de idioma de cada idioma para o qual seu provedor fornece o nome e as cadeias de caracteres de ajuda.</span><span class="sxs-lookup"><span data-stu-id="654e6-153">The `[languages]` section provides a list of the language identifiers of each language for which your provider supplies name and help strings.</span></span> <span data-ttu-id="654e6-154">Todos os provedores devem dar suporte a `009` (inglês).</span><span class="sxs-lookup"><span data-stu-id="654e6-154">All providers should support `009` (English).</span></span>

<span data-ttu-id="654e6-155">Para cada idioma com suporte, adicione uma chave chamada `<langid>=` .</span><span class="sxs-lookup"><span data-stu-id="654e6-155">For each supported language, add one key named `<langid>=`.</span></span> <span data-ttu-id="654e6-156">O valor é ignorado, mas para fins de documentação, o valor normalmente é definido como o nome do idioma correspondente, por exemplo, `009=English` .</span><span class="sxs-lookup"><span data-stu-id="654e6-156">The value is ignored, but for documentation purposes the value is normally set to the name of the corresponding language, e.g. `009=English`.</span></span>

<span data-ttu-id="654e6-157">Para a maioria dos idiomas, você deve usar o identificador de idioma primário.</span><span class="sxs-lookup"><span data-stu-id="654e6-157">For most languages, you should use the primary language identifier.</span></span> <span data-ttu-id="654e6-158">A lista completa de identificadores de idioma está no arquivo de cabeçalho WinNT. h, sob o título "IDs de idioma primário".</span><span class="sxs-lookup"><span data-stu-id="654e6-158">The complete list of language identifiers is in the Winnt.h header file, under the heading "Primary Language Ids."</span></span> <span data-ttu-id="654e6-159">Converta o valor encontrado em Winnt. h em uma sequência de 3 dígitos hexadecimais removendo o `0x` prefixo e adicionando os dígitos à esquerda `0` até que a sequência tenha 3 dígitos de comprimento.</span><span class="sxs-lookup"><span data-stu-id="654e6-159">Convert the value found in Winnt.h into a sequence of 3 hexadecimal digits by removing the `0x` prefix and adding leading `0` digits until the sequence is 3 digits long.</span></span> <span data-ttu-id="654e6-160">Por exemplo, para especificar cadeias de caracteres em inglês (0x9), use 009.</span><span class="sxs-lookup"><span data-stu-id="654e6-160">For example, to specify English strings (0x9), use 009.</span></span> <span data-ttu-id="654e6-161">Para especificar as cadeias de caracteres italianas (0x10), use 010.</span><span class="sxs-lookup"><span data-stu-id="654e6-161">To specify Italian strings (0x10), use 010.</span></span>

<span data-ttu-id="654e6-162">Os idiomas chinês e Português exigem os identificadores primário e subidioma.</span><span class="sxs-lookup"><span data-stu-id="654e6-162">Chinese and Portuguese languages require both the primary and sublanguage identifiers.</span></span> <span data-ttu-id="654e6-163">Use 404, 804, 416 ou 816 em vez de 004 ou 016.</span><span class="sxs-lookup"><span data-stu-id="654e6-163">Use 404, 804, 416, or 816 instead of 004 or 016.</span></span>

### <a name="text-section"></a><span data-ttu-id="654e6-164">seção [texto]</span><span class="sxs-lookup"><span data-stu-id="654e6-164">[text] section</span></span>

<span data-ttu-id="654e6-165">A `[text]` seção fornece as cadeias de caracteres de nome e de ajuda para seus objetos e contadores.</span><span class="sxs-lookup"><span data-stu-id="654e6-165">The `[text]` section provides the name and help strings for your objects and counters.</span></span>

<span data-ttu-id="654e6-166">Para cada objeto ou contador, e para cada idioma com suporte, você deve fornecer uma chave de nome (contendo o nome ou a cadeia de caracteres de título para o objeto ou contador) e, opcionalmente, fornecer uma chave de ajuda (que contém a descrição ou a cadeia de caracteres de explicação para o objeto ou contador).</span><span class="sxs-lookup"><span data-stu-id="654e6-166">For each object or counter, and for each supported language, you must provide a NAME key (containing the name or title string for your object or counter) and you may optionally provide a HELP key (containing the description or explanation string for your object or counter).</span></span> <span data-ttu-id="654e6-167">As chaves devem ser nomeadas `<symbol>_<langid>_NAME` e `<symbol>_<langid>_HELP` , em que `<symbol>` é a constante simbólica para o objeto ou contador (conforme definido no arquivo constante. h do simbólico) e `<langid>` é o identificador de idioma usado para esta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="654e6-167">The keys should be named `<symbol>_<langid>_NAME` and `<symbol>_<langid>_HELP`, where `<symbol>` is the symbolic constant for the object or counter (as defined in the symbolic constant .h file), and `<langid>` is the language identifier used for this string.</span></span>

<span data-ttu-id="654e6-168">Por exemplo, as cadeias de caracteres em inglês para um contador com símbolo `MY_COUNTER` seriam especificadas como:</span><span class="sxs-lookup"><span data-stu-id="654e6-168">For example, the English strings for a counter with symbol `MY_COUNTER` would be specified as:</span></span>

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

<span data-ttu-id="654e6-169">As chaves de texto podem aparecer em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="654e6-169">The text keys can appear in any order.</span></span> <span data-ttu-id="654e6-170">As cadeias de texto não devem conter caracteres de formatação, como guias.</span><span class="sxs-lookup"><span data-stu-id="654e6-170">The text strings should not contain formatting characters such as tabs.</span></span>

### <a name="example-ini-file"></a><span data-ttu-id="654e6-171">Arquivo INI de exemplo</span><span class="sxs-lookup"><span data-stu-id="654e6-171">Example INI file</span></span>

<span data-ttu-id="654e6-172">Veja a seguir um exemplo de um arquivo de inicialização que é usado no exemplo [criando uma DLL de extensão de desempenho](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="654e6-172">The following is an example of an initialization file that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) sample.</span></span>

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

## <a name="running-the-lodctr-tool"></a><span data-ttu-id="654e6-173">Executando a ferramenta LodCtr</span><span class="sxs-lookup"><span data-stu-id="654e6-173">Running the Lodctr tool</span></span>

<span data-ttu-id="654e6-174">Para carregar os nomes e as cadeias de caracteres de ajuda definidas no seu. Arquivo INI (durante a instalação do seu provedor), execute a ferramenta **lodctr** na pasta que contém o. Arquivo INI e arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="654e6-174">To load the names and help strings defined in your .INI file (during the installation of your provider), run the **lodctr** tool from the folder that contains your .INI file and header file.</span></span> <span data-ttu-id="654e6-175">A ferramenta está incluída no computador.</span><span class="sxs-lookup"><span data-stu-id="654e6-175">The tool is included with the computer.</span></span> <span data-ttu-id="654e6-176">Você deve executar o **lodctr** com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="654e6-176">You must run **lodctr** with elevated privileges.</span></span> <span data-ttu-id="654e6-177">O parâmetro para **lodctr** é o caminho para o. Arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="654e6-177">The parameter to **lodctr** is the path to your .INI file.</span></span> <span data-ttu-id="654e6-178">Por exemplo, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span><span class="sxs-lookup"><span data-stu-id="654e6-178">For example, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span></span>

<span data-ttu-id="654e6-179">Para descarregar os nomes e as cadeias de caracteres de ajuda (durante a desinstalação), execute a ferramenta **Unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="654e6-179">To unload the names and help strings (during uninstall), run the **unlodctr** tool.</span></span> <span data-ttu-id="654e6-180">Você deve executar o **Unlodctr** com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="654e6-180">You must run **unlodctr** with elevated privileges.</span></span> <span data-ttu-id="654e6-181">O parâmetro para **Unlodctr** é o DriverName do seu provedor (o nome da chave de desempenho do provedor).</span><span class="sxs-lookup"><span data-stu-id="654e6-181">The parameter to **unlodctr** is the DriverName of your provider (the name of the provider's performance key).</span></span> <span data-ttu-id="654e6-182">Por exemplo, `unlodctr "MyProvider"`.</span><span class="sxs-lookup"><span data-stu-id="654e6-182">For example, `unlodctr "MyProvider"`.</span></span>

<span data-ttu-id="654e6-183">Antes de executar **lodctr**, certifique-se de que seu aplicativo tem uma entrada sob a chave de **Serviços** .</span><span class="sxs-lookup"><span data-stu-id="654e6-183">Before running **lodctr**, be sure that your application has an entry under the **Services** key.</span></span> <span data-ttu-id="654e6-184">Para obter detalhes, consulte [criando a chave de desempenho do aplicativo](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="654e6-184">For details, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span> <span data-ttu-id="654e6-185">Se a chave não existir, **lodctr** não atualizará o registro com seus nomes e descrições.</span><span class="sxs-lookup"><span data-stu-id="654e6-185">If the key does not exist, **lodctr** will not update the registry with your names and descriptions.</span></span>

<span data-ttu-id="654e6-186">Como alternativa à execução de **lodctr**, você pode chamar [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definido em LoadPerf. h) de seu programa de instalação para carregar as descrições de nomes de contadores.</span><span class="sxs-lookup"><span data-stu-id="654e6-186">As an alternative to running **lodctr**, you can call [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (defined in Loadperf.h) from your installation program to load your counter names descriptions.</span></span> <span data-ttu-id="654e6-187">Em seguida, você pode chamar [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) durante a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="654e6-187">You can then call [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) during uninstall.</span></span>

<span data-ttu-id="654e6-188">O utilitário **lodctr** copia as cadeias de caracteres do. INI para os **contadores** e os valores de registro da **ajuda** nas subchaves de idioma apropriadas.</span><span class="sxs-lookup"><span data-stu-id="654e6-188">The **lodctr** utility copies the strings from the .INI file to the **Counters** and **Help** registry values under the appropriate language subkeys.</span></span> <span data-ttu-id="654e6-189">Se a subchave de idioma correspondente não existir, as cadeias de caracteres desse idioma não serão copiadas.</span><span class="sxs-lookup"><span data-stu-id="654e6-189">If the corresponding language subkey does not exist, the strings for that language are not copied.</span></span> <span data-ttu-id="654e6-190">O utilitário também atualiza o **último contador** e o último valor de **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="654e6-190">The utility also updates the **Last Counter** and **Last Help** value.</span></span> <span data-ttu-id="654e6-191">Os nomes e as descrições do contador de desempenho são armazenados no seguinte local no registro.</span><span class="sxs-lookup"><span data-stu-id="654e6-191">The performance counter names and descriptions are stored in the following location in the registry.</span></span>

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

<span data-ttu-id="654e6-192">Além de adicionar valores sob a chave **PerfLib** , a ferramenta **lodctr** também adiciona os valores a seguir ao nó de **Serviços** para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="654e6-192">In addition to adding values under the **PerfLib** key, the **lodctr** tool also adds the following values to the **Services** node for the application.</span></span> <span data-ttu-id="654e6-193">Na maioria dos casos, o aplicativo e o provedor terão uma relação um-para-um; no entanto, é possível que um provedor forneça dados de contador para vários aplicativos, motivo pelo qual a chave é baseada no aplicativo e não no provedor.</span><span class="sxs-lookup"><span data-stu-id="654e6-193">In most cases, the application and provider will have a one-to-one relationship; however, it is possible for a provider to provide counter data for multiple applications, which is why the key is based on the application and not the provider.</span></span>

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
