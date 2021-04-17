---
description: O diagrama a seguir ilustra os principais objetos envolvidos nos controles de diretório de reunião TAPI 3. As interfaces mostradas são vinculadas às páginas de referência relevantes.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Controles de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789872"
---
# <a name="directory-controls"></a><span data-ttu-id="7e1d8-104">Controles de diretório</span><span class="sxs-lookup"><span data-stu-id="7e1d8-104">Directory Controls</span></span>

<span data-ttu-id="7e1d8-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7e1d8-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="7e1d8-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7e1d8-107">O diagrama a seguir ilustra os principais objetos envolvidos nos controles de diretório de reunião TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-107">The following diagram illustrates the main objects involved in TAPI 3 Rendezvous directory controls.</span></span> <span data-ttu-id="7e1d8-108">As interfaces mostradas são vinculadas às páginas de referência relevantes.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![interfaces e objetos de controle do diretório de reunião](images/renddir.png)

<span data-ttu-id="7e1d8-110">A interface de controle de diretório principal é [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), que deve ser criada chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-110">The main directory control interface is [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), which must be created by calling **CoCreateInstance**.</span></span> <span data-ttu-id="7e1d8-111">O objeto de reunião expõe métodos para obter listas de diretórios disponíveis e criar novos diretórios ou objetos de diretório.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-111">The Rendezvous object exposes methods to get lists of available directories and to create new directories or directory objects.</span></span>

<span data-ttu-id="7e1d8-112">Um diretório reside em um servidor e é uma lista de objetos de diretório, juntamente com informações descritivas.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-112">A directory resides on a server and is a list of directory objects along with descriptive information.</span></span> <span data-ttu-id="7e1d8-113">Os métodos associados ao [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) podem obter informações associadas ao diretório como um todo, como se ele é um diretório ILS.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-113">Methods associated with [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) can get information associated with the directory as a whole, such as whether it is an ILS directory.</span></span>

<span data-ttu-id="7e1d8-114">Um objeto de diretório pode representar uma conferência ou um usuário.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-114">A directory object can represent a conference or a user.</span></span> <span data-ttu-id="7e1d8-115">A interface [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) fornece métodos que podem recuperar ou modificar informações genéricas para um objeto de diretório, como o endereço de discagem.</span><span class="sxs-lookup"><span data-stu-id="7e1d8-115">The [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) interface supplies methods that can retrieve or modify information generic to a directory object, such as the dialable address.</span></span>

<span data-ttu-id="7e1d8-116">As informações de conferência e de usuário, como a URL de uma conferência ou o telefone IP primário de um usuário, são manipuladas por métodos fornecidos nas interfaces [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) e [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .</span><span class="sxs-lookup"><span data-stu-id="7e1d8-116">Conference and user information, such as the URL of a conference or the primary IP phone of a user, is manipulated by methods provided in the [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) and [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) interfaces.</span></span>

 

 



