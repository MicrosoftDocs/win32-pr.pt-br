---
description: Os conjuntos de estações sendo monitorados por meio de um link de terceiros são modelados como um dispositivo de linha e, possivelmente, um dispositivo de telefone associado.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Rádio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810994"
---
# <a name="stations"></a><span data-ttu-id="9bbc1-103">Rádio</span><span class="sxs-lookup"><span data-stu-id="9bbc1-103">Stations</span></span>

<span data-ttu-id="9bbc1-104">Os conjuntos de estações sendo monitorados por meio de um link de terceiros são modelados como um dispositivo de linha e, possivelmente, um dispositivo de telefone associado.</span><span class="sxs-lookup"><span data-stu-id="9bbc1-104">Station sets being monitored through a third-party link are modeled as a line device and possibly an associated phone device.</span></span> <span data-ttu-id="9bbc1-105">O dispositivo de linha pode ter vários endereços, se o terminal modelado der suporte a mais de um DN (número de diretório).</span><span class="sxs-lookup"><span data-stu-id="9bbc1-105">The line device can have multiple addresses, if the modeled terminal supports more than one directory number (DN).</span></span> <span data-ttu-id="9bbc1-106">Várias aparências de chamada no mesmo DN podem ser modeladas como um único endereço que dá suporte a várias chamadas.</span><span class="sxs-lookup"><span data-stu-id="9bbc1-106">Multiple call appearances on the same DN can be modeled as a single address that supports multiple calls.</span></span>

<span data-ttu-id="9bbc1-107">As chamadas entre duas estações no comutador têm dois identificadores de chamada, um fornecendo a exibição de chamada da primeira estação (em seu dispositivo de linha) e o outro que dá a exibição de chamada da segunda estação (em seu dispositivo de linha).</span><span class="sxs-lookup"><span data-stu-id="9bbc1-107">Calls between two stations on the switch have two call handles, one giving the call view from the first station (on its line device), and the other giving the call view from the second station (on its line device).</span></span> <span data-ttu-id="9bbc1-108">Por exemplo, um [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) de terceiros colocado por um aplicativo no servidor seria direcionado para o dispositivo de linha associado à estação da qual a chamada será discada; um identificador de chamada seria criado nessa linha, no endereço especificado em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (permitindo assim o controle sobre qual DN é usado em um telefone que dá suporte a vários DNS).</span><span class="sxs-lookup"><span data-stu-id="9bbc1-108">For example, a third-party [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) placed by an application on the server would be directed to the line device associated with the station from which the call is to be dialed; a call handle would be created on that line, on the address specified in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (thereby giving control over which DN is used on a phone that supports multiple DNs).</span></span> <span data-ttu-id="9bbc1-109">Quando a chamada é oferecida ao endereço de destino, um novo identificador de chamada mostrando uma chamada no estado de *oferta* é criado; os aplicativos sabem que era outra exibição da mesma chamada pelo membro **dwCallID** em [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) sendo igual para ambas as chamadas.</span><span class="sxs-lookup"><span data-stu-id="9bbc1-109">When the call is offered to the destination address, a new call handle showing a call in *offering* state is created; applications would know that it was another view of the same call by the **dwCallID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) being equal for both calls.</span></span> <span data-ttu-id="9bbc1-110">Ambas as chamadas ficarão *ociosas* quando a chamada fosse descartada; uma chamada pode ser descartada do aplicativo de terceiros fazendo um [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) em qualquer um dos identificadores de chamada.</span><span class="sxs-lookup"><span data-stu-id="9bbc1-110">Both calls would go *idle* when the call was dropped; a call could be dropped from the third-party application by doing a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on either of the call handles.</span></span>

 

 



