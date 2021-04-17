---
description: A classe de dispositivo TAPI/terminal consiste nos dispositivos de telefone associados a cada terminal em uma linha ou ao terminal em cada linha associada a um dispositivo de telefone. Você acessa esses dispositivos usando o dispositivo de linha TAPI ou as funções de dispositivo de telefone.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789842"
---
# <a name="tapiterminal"></a><span data-ttu-id="3c472-104">TAPI/terminal</span><span class="sxs-lookup"><span data-stu-id="3c472-104">tapi/terminal</span></span>

<span data-ttu-id="3c472-105">A classe de dispositivo TAPI/terminal consiste nos dispositivos de telefone associados a cada terminal em uma linha ou ao terminal em cada linha associada a um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="3c472-105">The tapi/terminal device class consists of the phone devices associated with each terminal on a line or the terminal on each line associated with a phone device.</span></span> <span data-ttu-id="3c472-106">Você acessa esses dispositivos usando o dispositivo de [linha](line-device-functions.md) TAPI ou as [funções de dispositivo de telefone](phone-device-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3c472-106">You access these devices by using the TAPI [line device](line-device-functions.md) or [phone device functions](phone-device-functions.md).</span></span>

<span data-ttu-id="3c472-107">A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esse membro adicional:</span><span class="sxs-lookup"><span data-stu-id="3c472-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

<span data-ttu-id="3c472-108">O membro **adwDeviceId** é uma matriz de identificadores de dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="3c472-108">The **adwDeviceId** member is an array of phone device identifiers.</span></span> <span data-ttu-id="3c472-109">Há um elemento de matriz para cada terminal especificado pelo membro **dwNumTerminals** na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) do dispositivo de linha especificado.</span><span class="sxs-lookup"><span data-stu-id="3c472-109">There is one array element for each terminal specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the given line device.</span></span> <span data-ttu-id="3c472-110">Cada elemento Especifica o identificador do dispositivo de telefone associado ao terminal correspondente na linha.</span><span class="sxs-lookup"><span data-stu-id="3c472-110">Each element specifies the identifier of the phone device associated with the corresponding terminal on the line.</span></span> <span data-ttu-id="3c472-111">Se não houver nenhum dispositivo telefônico associado a um terminal, o elemento será definido como – 1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="3c472-111">If there is no phone device associated with a terminal, the element is set to –1 (0xFFFFFFFF).</span></span>

<span data-ttu-id="3c472-112">A função [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esse membro adicional:</span><span class="sxs-lookup"><span data-stu-id="3c472-112">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

<span data-ttu-id="3c472-113">O membro **adwTerminalID** é uma matriz de identificadores de terminal.</span><span class="sxs-lookup"><span data-stu-id="3c472-113">The **adwTerminalID** member is an array of terminal identifiers.</span></span> <span data-ttu-id="3c472-114">Há um elemento de matriz para cada identificador de dispositivo de linha especificado pela função [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="3c472-114">There is one array element for each line device identifier specified by the [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) function.</span></span> <span data-ttu-id="3c472-115">Cada elemento de matriz contém o identificador de terminal associado ao dispositivo de telefone para o dispositivo de linha especificado.</span><span class="sxs-lookup"><span data-stu-id="3c472-115">Each array element contains the terminal identifier associated with the phone device for the given line device.</span></span> <span data-ttu-id="3c472-116">Se não houver nenhum dispositivo telefônico, o elemento será definido como – 1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="3c472-116">If there is no phone device, the element is set to –1 (0xFFFFFFFF).</span></span> <span data-ttu-id="3c472-117">Os identificadores de terminal variam em valor de zero a um menor que o número especificado pelo membro **dwNumTerminals** na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="3c472-117">The terminal identifiers range in value from zero to one less than the number specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>

 

 



