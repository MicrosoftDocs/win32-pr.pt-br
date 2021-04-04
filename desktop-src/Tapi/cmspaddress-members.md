---
description: A lista a seguir contém os membros do endereço CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Membros do CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837480"
---
# <a name="cmspaddress-members"></a><span data-ttu-id="07315-103">Membros do CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="07315-103">CMSPAddress Members</span></span>



| <span data-ttu-id="07315-104">Tipos de membro</span><span class="sxs-lookup"><span data-stu-id="07315-104">Member types</span></span>                    | <span data-ttu-id="07315-105">Nome</span><span class="sxs-lookup"><span data-stu-id="07315-105">Name</span></span>                    | <span data-ttu-id="07315-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="07315-106">Description</span></span>                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07315-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="07315-107">Iunknown</span></span>                        | <span data-ttu-id="07315-108">\*\_pFTM m</span><span class="sxs-lookup"><span data-stu-id="07315-108">\*m\_pFTM</span></span>               | <span data-ttu-id="07315-109">Ponteiro para o Marshaller com thread livre.</span><span class="sxs-lookup"><span data-stu-id="07315-109">Pointer to the free threaded marshaller.</span></span>                                                         |
| <span data-ttu-id="07315-110">PROCESSAMENTO</span><span class="sxs-lookup"><span data-stu-id="07315-110">HANDLE</span></span>                          | <span data-ttu-id="07315-111">\_htEvent m</span><span class="sxs-lookup"><span data-stu-id="07315-111">m\_htEvent</span></span>              | <span data-ttu-id="07315-112">Manipule o evento de Tapi3.dll, que é usado para notificar a TAPI que o MSP deseja enviar dados para ele.</span><span class="sxs-lookup"><span data-stu-id="07315-112">Handle to Tapi3.dll's event, which is used to notify TAPI that the MSP wants to send data to it.</span></span> |
| <span data-ttu-id="07315-113">entrada de lista \_</span><span class="sxs-lookup"><span data-stu-id="07315-113">LIST\_ENTRY</span></span>                     | <span data-ttu-id="07315-114">de \_ eventos m</span><span class="sxs-lookup"><span data-stu-id="07315-114">m\_EventList</span></span>            | <span data-ttu-id="07315-115">Lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="07315-115">List of events.</span></span>                                                                                  |
| <span data-ttu-id="07315-116">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="07315-116">CMSPCritSection</span></span>                 | <span data-ttu-id="07315-117">\_EventDataLock m</span><span class="sxs-lookup"><span data-stu-id="07315-117">m\_EventDataLock</span></span>        | <span data-ttu-id="07315-118">O bloqueio que protege os dados relacionados à manipulação de eventos com a TAPI.</span><span class="sxs-lookup"><span data-stu-id="07315-118">The lock that protects the data related to event handling with TAPI.</span></span>                             |
| <span data-ttu-id="07315-119">ITTerminalManager</span><span class="sxs-lookup"><span data-stu-id="07315-119">ITTerminalManager</span></span>               | <span data-ttu-id="07315-120">\*\_pITTerminalManager m</span><span class="sxs-lookup"><span data-stu-id="07315-120">\*m\_pITTerminalManager</span></span> | <span data-ttu-id="07315-121">O ponteiro para o objeto do Gerenciador de terminal.</span><span class="sxs-lookup"><span data-stu-id="07315-121">The pointer to the Terminal Manager object.</span></span>                                                      |
| <span data-ttu-id="07315-122">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="07315-122">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="07315-123">\_terminais m</span><span class="sxs-lookup"><span data-stu-id="07315-123">m\_Terminals</span></span>            | <span data-ttu-id="07315-124">A lista de terminais estáticos que podem ser usados no endereço.</span><span class="sxs-lookup"><span data-stu-id="07315-124">The list of static terminals that can be used on the address.</span></span>                                    |
| <span data-ttu-id="07315-125">BOOL</span><span class="sxs-lookup"><span data-stu-id="07315-125">BOOL</span></span>                            | <span data-ttu-id="07315-126">\_fTerminalsUpToDate m</span><span class="sxs-lookup"><span data-stu-id="07315-126">m\_fTerminalsUpToDate</span></span>   | <span data-ttu-id="07315-127">Esse sinalizador será **verdadeiro** se a lista de terminais estiver atualizada.</span><span class="sxs-lookup"><span data-stu-id="07315-127">This flag is **TRUE** if the terminal list is up to date.</span></span>                                        |
| <span data-ttu-id="07315-128">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="07315-128">CMSPCritSection</span></span>                 | <span data-ttu-id="07315-129">\_TerminalDataLock m</span><span class="sxs-lookup"><span data-stu-id="07315-129">m\_TerminalDataLock</span></span>     | <span data-ttu-id="07315-130">O bloqueio que protege os membros de dados relacionados ao terminal.</span><span class="sxs-lookup"><span data-stu-id="07315-130">The lock that protects the terminal-related data members.</span></span>                                        |



 

 

 



