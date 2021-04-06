---
description: Net.exe pode ser usado para parar e iniciar o protocolo IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827106"
---
# <a name="netexe"></a><span data-ttu-id="c6979-103">Net.exe</span><span class="sxs-lookup"><span data-stu-id="c6979-103">Net.exe</span></span>

<span data-ttu-id="c6979-104">Net.exe pode ser usado para parar e iniciar o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="c6979-104">Net.exe can be used to stop and start the IPv6 protocol.</span></span> <span data-ttu-id="c6979-105">Reiniciar o IPv6 reinicializa o protocolo como se o computador estivesse reiniciando, o que pode alterar os números de interface.</span><span class="sxs-lookup"><span data-stu-id="c6979-105">Restarting IPv6 reinitializes the protocol as if the computer were restarting, which may change interface numbers.</span></span> <span data-ttu-id="c6979-106">Net.exe tem muitos subcomandos.</span><span class="sxs-lookup"><span data-stu-id="c6979-106">Net.exe has many subcommands.</span></span> <span data-ttu-id="c6979-107">Os comandos a seguir são relevantes para o IPv6:</span><span class="sxs-lookup"><span data-stu-id="c6979-107">The following commands are relevant to IPv6:</span></span>

<dl> <dt>

<span data-ttu-id="c6979-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**tcpip6 net stop**</span><span class="sxs-lookup"><span data-stu-id="c6979-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="c6979-109">Interrompe o protocolo IPv6 e o descarrega da memória.</span><span class="sxs-lookup"><span data-stu-id="c6979-109">Stops the IPv6 protocol and unloads it from memory.</span></span> <span data-ttu-id="c6979-110">Esse comando falhará se algum soquete IPv6 estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="c6979-110">This command fails if any IPv6 sockets are open.</span></span>

</dd> <dt>

<span data-ttu-id="c6979-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span><span class="sxs-lookup"><span data-stu-id="c6979-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="c6979-112">Inicia o protocolo IPv6 se ele foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="c6979-112">Starts the IPv6 protocol if it was stopped.</span></span> <span data-ttu-id="c6979-113">Se um novo arquivo de driver de Tcpip6.sys estiver presente no diretório% systemroot% \\ System32 \\ drivers, esse arquivo de driver será carregado.</span><span class="sxs-lookup"><span data-stu-id="c6979-113">If a new Tcpip6.sys driver file is present in the %systemroot%\\System32\\Drivers directory, that driver file is loaded.</span></span>

</dd> </dl>

 

 



