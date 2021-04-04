---
description: 'Os seguintes tipos de dados são definidos na API de cópia de sombra de volume:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Tipos de dados da API de cópia de sombra de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647170"
---
# <a name="volume-shadow-copy-api-data-types"></a><span data-ttu-id="dceb3-103">Tipos de dados da API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="dceb3-103">Volume Shadow Copy API Data Types</span></span>

<span data-ttu-id="dceb3-104">Os seguintes tipos de dados são definidos na API de cópia de sombra de volume:</span><span class="sxs-lookup"><span data-stu-id="dceb3-104">The following data types are defined in the Volume Shadow Copy API:</span></span>

<dl> <dt>

<span data-ttu-id="dceb3-105"><span id="VSS_ID"></span><span id="vss_id"></span>ID do VSS \_</span><span class="sxs-lookup"><span data-stu-id="dceb3-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS\_ID</span></span>
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

<span data-ttu-id="dceb3-106">A definição de **\_ ID do VSS** especifica o formato geral do identificador VSS.</span><span class="sxs-lookup"><span data-stu-id="dceb3-106">The **VSS\_ID** definition specifies the general VSS identifier format.</span></span> <span data-ttu-id="dceb3-107">A **\_ ID do VSS** é um tipo de dados GUID padrão.</span><span class="sxs-lookup"><span data-stu-id="dceb3-107">The **VSS\_ID** is a standard GUID data type.</span></span>

<span data-ttu-id="dceb3-108">**VSS \_** Os s de ID são usados para identificar o seguinte: cópias de sombra, conjuntos de cópias de sombra, provedores, versões do provedor, gravadores (identificador de classe do gravador) e instâncias de gravadores.</span><span class="sxs-lookup"><span data-stu-id="dceb3-108">**VSS\_ID** s are used to identify the following: shadow copies, shadow copy sets, providers, provider versions, writers (writer's class identifier), and instances of writers.</span></span>

</dd> <dt>

<span data-ttu-id="dceb3-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>\_PWSZ VSS</span><span class="sxs-lookup"><span data-stu-id="dceb3-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS\_PWSZ</span></span>
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

<span data-ttu-id="dceb3-110">A definição de **\_ PWSZ do VSS** especifica uma cadeia de caracteres largo (WCHAR) terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="dceb3-110">The **VSS\_PWSZ** definition specifies a null-terminated wide character string (wchar).</span></span>

</dd> <dt>

<span data-ttu-id="dceb3-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_carimbo de data/hora VSS</span><span class="sxs-lookup"><span data-stu-id="dceb3-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS\_TIMESTAMP</span></span>
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

<span data-ttu-id="dceb3-112">A definição de **\_ carimbo de data/** hora do VSS mantém informações de carimbo de data/hora como um valor inteiro de 64 bits que contém o número de intervalos de 100 nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="dceb3-112">The **VSS\_TIMESTAMP** definition holds time-stamp information as a 64-bit integer value containing the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="dceb3-113">Essa definição é intercambiável com a estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="dceb3-113">This definition is interchangeable with the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> </dl>

 

 
