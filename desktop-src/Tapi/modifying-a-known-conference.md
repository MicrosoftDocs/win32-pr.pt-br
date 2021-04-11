---
description: O fragmento de código a seguir ilustra a modificação de um intervalo de tempo de conferências. O período de tempo padrão é de trinta minutos. Nesse fragmento, o período de tempo é definido como um ano.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modificando uma conferência conhecida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164244"
---
# <a name="modifying-a-known-conference"></a><span data-ttu-id="a4afa-105">Modificando uma conferência conhecida</span><span class="sxs-lookup"><span data-stu-id="a4afa-105">Modifying a Known Conference</span></span>

<span data-ttu-id="a4afa-106">\[Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a4afa-106">\[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a4afa-107">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a4afa-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a4afa-108">O fragmento de código a seguir ilustra a modificação do período de tempo de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="a4afa-108">The following code fragment illustrates modification of a conference's time span.</span></span> <span data-ttu-id="a4afa-109">O período de tempo padrão é de trinta minutos.</span><span class="sxs-lookup"><span data-stu-id="a4afa-109">The default time span is thirty minutes.</span></span> <span data-ttu-id="a4afa-110">Nesse fragmento, o período de tempo é definido como um ano.</span><span class="sxs-lookup"><span data-stu-id="a4afa-110">In this fragment, the time span is set to one year.</span></span>

<span data-ttu-id="a4afa-111">Este fragmento pressupõe que [a conexão com um servidor ILS](connecting-to-an-ils-server.md) já foi executada e que uma [enumeração de diretório de conferência](enumerating-conference-directories.md) foi executada para obter a entrada de diretório que será modificada.</span><span class="sxs-lookup"><span data-stu-id="a4afa-111">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed and that a [conference directory enumeration](enumerating-conference-directories.md) has been performed to obtain the directory entry that will be modified.</span></span>

<span data-ttu-id="a4afa-112">Esse fragmento também pressupõe que essa não é uma conferência multicast.</span><span class="sxs-lookup"><span data-stu-id="a4afa-112">This fragment also assumes this is not a multicast conference.</span></span> <span data-ttu-id="a4afa-113">Alterar os horários em uma conferência multicast requer a notificação do servidor de alocação de endereços multicast.</span><span class="sxs-lookup"><span data-stu-id="a4afa-113">Changing the times on a multicast conference requires notification of the multicast address allocation server.</span></span> <span data-ttu-id="a4afa-114">Consulte [adquirindo um endereço de multicast](acquiring-a-multicast-address.md) para obter um exemplo de como trabalhar com endereçamento multicast.</span><span class="sxs-lookup"><span data-stu-id="a4afa-114">See [Acquiring a Multicast Address](acquiring-a-multicast-address.md) for an example of working with multicast addressing.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="a4afa-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4afa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4afa-116">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="a4afa-116">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



