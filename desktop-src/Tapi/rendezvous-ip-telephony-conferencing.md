---
description: Os controles de reunião TAPI 3 permitem que um programador crie aplicativos que podem criar e descobrir conferências de IP de multicast de multimídia.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conferência de telefonia IP de reunião
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169477"
---
# <a name="rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="91e79-103">Conferência de telefonia IP de reunião</span><span class="sxs-lookup"><span data-stu-id="91e79-103">Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="91e79-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="91e79-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="91e79-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="91e79-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="91e79-106">Os controles de reunião TAPI 3 permitem que um programador crie aplicativos que podem criar e descobrir conferências de IP de multicast de multimídia.</span><span class="sxs-lookup"><span data-stu-id="91e79-106">The TAPI 3 Rendezvous controls enable a programmer to create applications that can create and discover multimedia multicast IP conferences.</span></span>

<span data-ttu-id="91e79-107">Os principais componentes da reunião:</span><span class="sxs-lookup"><span data-stu-id="91e79-107">The key components of Rendezvous:</span></span>

<span data-ttu-id="91e79-108">Os [controles de diretório](directory-controls.md) são uma abstração de listagens de conferências em um servidor ILS ou NTDS.</span><span class="sxs-lookup"><span data-stu-id="91e79-108">[Directory Controls](directory-controls.md) are an abstraction of conference listings on an ILS or NTDS server.</span></span>

<span data-ttu-id="91e79-109">Os [controles de blob de conferência](conference-blob-controls.md) representam informações específicas da conferência, como hora de início e de parada.</span><span class="sxs-lookup"><span data-stu-id="91e79-109">[Conference Blob Controls](conference-blob-controls.md) represent conference-specific information such as start and stop time.</span></span> <span data-ttu-id="91e79-110">Interfaces especiais são fornecidas para BLOBs de protocolo SDP.</span><span class="sxs-lookup"><span data-stu-id="91e79-110">Special interfaces are provided for SDP protocol blobs.</span></span> <span data-ttu-id="91e79-111">Para obter informações detalhadas, consulte RFC 2327 intitulado "SDP: Session description protocol".</span><span class="sxs-lookup"><span data-stu-id="91e79-111">For detailed information, see RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="91e79-112">Uma cópia atual desse RFC pode ser localizada usando um mecanismo de pesquisa da Internet.</span><span class="sxs-lookup"><span data-stu-id="91e79-112">A current copy of this RFC can be located using an Internet search engine.</span></span>

<span data-ttu-id="91e79-113">As [interfaces com multicast](multicast-com-interfaces.md) são wrappers com para as funções do MADCAP, anteriormente conhecidos como MDHCP.</span><span class="sxs-lookup"><span data-stu-id="91e79-113">[Multicast COM Interfaces](multicast-com-interfaces.md) are COM wrappers for the MADCAP functions, formerly know as MDHCP.</span></span> <span data-ttu-id="91e79-114">Essas interfaces permitem que um aplicativo obtenha endereços multicast de um servidor de alocação de endereços multicast.</span><span class="sxs-lookup"><span data-stu-id="91e79-114">These interfaces allow an application to get multicast addresses from a multicast address allocation server.</span></span>

<span data-ttu-id="91e79-115">O material a seguir fornece uma visão geral e alguns exemplos de uso dos controles de reunião para a telefonia e a conferência por IP.</span><span class="sxs-lookup"><span data-stu-id="91e79-115">The following material provides a general overview and some usage examples of the Rendezvous controls for IP telephony and conferencing.</span></span>

 

 



