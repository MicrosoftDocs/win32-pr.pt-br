---
description: Outras funções de telefone TAPI usam um identificador para um dispositivo de telefone aberto para identificar o dispositivo de telefone aberto.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: IDs de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759477"
---
# <a name="device-ids"></a><span data-ttu-id="074ce-103">IDs de dispositivo</span><span class="sxs-lookup"><span data-stu-id="074ce-103">Device IDs</span></span>

<span data-ttu-id="074ce-104">Outras funções de telefone TAPI usam um identificador para um dispositivo de telefone aberto para identificar o dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="074ce-104">Other TAPI phone functions use a handle to an open phone device to identify the open phone device.</span></span> <span data-ttu-id="074ce-105">As únicas funções para dispositivos de telefone que usam um parâmetro de identificador de dispositivo de telefone (em oposição a um identificador de telefone) são as funções [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) .</span><span class="sxs-lookup"><span data-stu-id="074ce-105">The only functions for phone devices that take a phone device identifier parameter (as opposed to a phone handle) are the [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) functions.</span></span> <span data-ttu-id="074ce-106">Um aplicativo pode recuperar o identificador de dispositivo do telefone usando a função [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) com o identificador de telefone como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="074ce-106">An application can retrieve the phone's device identifier by using the [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function with the phone handle as a parameter.</span></span>

<span data-ttu-id="074ce-107">Um aplicativo também pode obter identificadores de dispositivo para várias classes de dispositivo associadas a um telefone aberto invocando [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="074ce-107">An application can also obtain device identifiers for various device classes associated with an opened phone by invoking [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span> <span data-ttu-id="074ce-108">Consulte [classes de dispositivo TAPI](tapi-device-classes.md) para nomes de classe de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="074ce-108">See [TAPI Device Classes](tapi-device-classes.md) for device class names.</span></span>

<span data-ttu-id="074ce-109">Essa função usa um identificador de telefone e uma descrição de classe de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="074ce-109">This function takes a phone handle and a device class description.</span></span> <span data-ttu-id="074ce-110">Ele retorna o identificador de dispositivo para o dispositivo da classe de dispositivo fornecida que está associada ao dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="074ce-110">It returns the device identifier for the device of the given device class that is associated with the open phone device.</span></span> <span data-ttu-id="074ce-111">Se a classe de dispositivo for "TAPI/telefone", o identificador de dispositivo do dispositivo de telefone será retornado.</span><span class="sxs-lookup"><span data-stu-id="074ce-111">If the device class is "tapi/phone", the device identifier of the phone device is returned.</span></span>

<span data-ttu-id="074ce-112">Em contraste com os dispositivos de linha, para os quais os serviços de linha básica fornecem o equivalente de POTS, nenhum conjunto mínimo garantido de funções é definido para dispositivos de telefone.</span><span class="sxs-lookup"><span data-stu-id="074ce-112">In contrast with line devices, for which the basic line services provide the equivalent of POTS, no minimum guaranteed set of functions is defined for phone devices.</span></span> <span data-ttu-id="074ce-113">Embora cada dispositivo de telefone forneça pelo menos as funções e mensagens descritas nesta seção, eles não oferecem nenhuma operação real no dispositivo de telefone físico.</span><span class="sxs-lookup"><span data-stu-id="074ce-113">While each phone device provides at least the functions and messages described in this section, they do not offer any actual operations on the physical phone device.</span></span>

 

 



