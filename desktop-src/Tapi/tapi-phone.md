---
description: A classe de dispositivo TAPI/telefone consiste em todos os dispositivos de telefone. Você acessa esses dispositivos usando as funções de telefone TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922211"
---
# <a name="tapiphone"></a><span data-ttu-id="454a0-104">TAPI/telefone</span><span class="sxs-lookup"><span data-stu-id="454a0-104">tapi/phone</span></span>

<span data-ttu-id="454a0-105">A classe de dispositivo TAPI/telefone consiste em todos os dispositivos de telefone.</span><span class="sxs-lookup"><span data-stu-id="454a0-105">The tapi/phone device class consists of all phone devices.</span></span> <span data-ttu-id="454a0-106">Você acessa esses dispositivos usando as funções de telefone TAPI.</span><span class="sxs-lookup"><span data-stu-id="454a0-106">You access these devices by using the TAPI phone functions.</span></span>

<span data-ttu-id="454a0-107">A função [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esse membro adicional:</span><span class="sxs-lookup"><span data-stu-id="454a0-107">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

<span data-ttu-id="454a0-108">O membro **dwDeviceId** é o identificador do dispositivo de telefone associado ao identificador de telefone fornecido pelo [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="454a0-108">The **dwDeviceId** member is the identifier of the phone device associated with the phone handle given by [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span>

<span data-ttu-id="454a0-109">A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) também preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo **dwStringFormat** como StringFormat \_ Binary e acrescentando esse membro adicional:</span><span class="sxs-lookup"><span data-stu-id="454a0-109">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

<span data-ttu-id="454a0-110">O membro **adwDeviceIds** é uma matriz que contém os identificadores de dispositivo de todos os dispositivos de telefone associados ao dispositivo de linha especificado.</span><span class="sxs-lookup"><span data-stu-id="454a0-110">The **adwDeviceIds** member is an array containing the device identifiers of all phone devices that are associated with the given line device.</span></span> <span data-ttu-id="454a0-111">Se não houver nenhum dispositivo de telefone associado, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) retornará o \_ valor de INVALDEVICECLASS LINEERR.</span><span class="sxs-lookup"><span data-stu-id="454a0-111">If there are no associated phone devices, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) returns the LINEERR\_INVALDEVICECLASS value.</span></span>

 

 



