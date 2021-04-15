---
description: A classe de dispositivo TAPI/linha consiste em todos os dispositivos de linha. Você acessa esses dispositivos usando as funções de linha TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753531"
---
# <a name="tapiline"></a><span data-ttu-id="2f83b-104">TAPI/linha</span><span class="sxs-lookup"><span data-stu-id="2f83b-104">tapi/line</span></span>

<span data-ttu-id="2f83b-105">A classe de dispositivo TAPI/linha consiste em todos os dispositivos de linha.</span><span class="sxs-lookup"><span data-stu-id="2f83b-105">The tapi/line device class consists of all line devices.</span></span> <span data-ttu-id="2f83b-106">Você acessa esses dispositivos usando as funções de linha TAPI.</span><span class="sxs-lookup"><span data-stu-id="2f83b-106">You access these devices using the TAPI line functions.</span></span>

<span data-ttu-id="2f83b-107">A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esse membro adicional.</span><span class="sxs-lookup"><span data-stu-id="2f83b-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member.</span></span>

``` syntax
DWORD dwDeviceI;  // line device identifier
```

<span data-ttu-id="2f83b-108">O membro **dwDeviceId** é o identificador do dispositivo de linha associado ao identificador de linha fornecido pelo [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="2f83b-108">The **dwDeviceId** member is the identifier of the line device associated with the line handle given by [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="2f83b-109">A função [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) também preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo **dwStringFormat** como StringFormat \_ Binary e acrescentando esse membro adicional:</span><span class="sxs-lookup"><span data-stu-id="2f83b-109">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

<span data-ttu-id="2f83b-110">O membro **adwDeviceIds** é uma matriz que contém os identificadores de todos os dispositivos de linha associados ao dispositivo telefônico.</span><span class="sxs-lookup"><span data-stu-id="2f83b-110">The **adwDeviceIds** member is an array containing the device identifiers of all line devices that are associated with the phone device.</span></span> <span data-ttu-id="2f83b-111">Se não houver nenhum dispositivo de linha associado, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) retornará o \_ valor de INVALDEVICECLASS PHONEERR.</span><span class="sxs-lookup"><span data-stu-id="2f83b-111">If there are no associated line devices, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) returns the PHONEERR\_INVALDEVICECLASS value.</span></span>

 

 



