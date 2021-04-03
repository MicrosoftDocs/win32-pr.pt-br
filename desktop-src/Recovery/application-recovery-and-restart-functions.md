---
title: Recuperação de aplicativo e funções de reinicialização
description: Recuperação e reinicialização do aplicativo define as funções a seguir
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084741"
---
# <a name="application-recovery-and-restart-functions"></a><span data-ttu-id="b2618-103">Recuperação de aplicativo e funções de reinicialização</span><span class="sxs-lookup"><span data-stu-id="b2618-103">Application Recovery and Restart Functions</span></span>

<span data-ttu-id="b2618-104">A recuperação e a reinicialização do aplicativo define as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="b2618-104">Application Recovery and Restart defines the following functions:</span></span>



| <span data-ttu-id="b2618-105">Função</span><span class="sxs-lookup"><span data-stu-id="b2618-105">Function</span></span>                                                                               | <span data-ttu-id="b2618-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2618-106">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2618-107">**ApplicationRecoveryFinished**</span><span class="sxs-lookup"><span data-stu-id="b2618-107">**ApplicationRecoveryFinished**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | <span data-ttu-id="b2618-108">Indica que o aplicativo de chamada concluiu sua recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="b2618-108">Indicates that the calling application has completed its data recovery.</span></span>                    |
| [<span data-ttu-id="b2618-109">**ApplicationRecoveryInProgress**</span><span class="sxs-lookup"><span data-stu-id="b2618-109">**ApplicationRecoveryInProgress**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | <span data-ttu-id="b2618-110">Indica que o aplicativo de chamada está continuando a recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="b2618-110">Indicates that the calling application is continuing to recover data.</span></span>                      |
| [<span data-ttu-id="b2618-111">**GetApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="b2618-111">**GetApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | <span data-ttu-id="b2618-112">Recupera um ponteiro para a rotina de retorno de chamada de recuperação registrada para o processo especificado.</span><span class="sxs-lookup"><span data-stu-id="b2618-112">Retrieves a pointer to the recovery callback routine registered for the specified process.</span></span> |
| [<span data-ttu-id="b2618-113">**GetApplicationRestartSettings**</span><span class="sxs-lookup"><span data-stu-id="b2618-113">**GetApplicationRestartSettings**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | <span data-ttu-id="b2618-114">Recupera as informações de reinicialização registradas para o processo especificado.</span><span class="sxs-lookup"><span data-stu-id="b2618-114">Retrieves the restart information registered for the specified process.</span></span>                    |
| [<span data-ttu-id="b2618-115">**RegisterApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="b2618-115">**RegisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | <span data-ttu-id="b2618-116">Registra a instância ativa de um aplicativo para recuperação.</span><span class="sxs-lookup"><span data-stu-id="b2618-116">Registers the active instance of an application for recovery.</span></span>                              |
| [<span data-ttu-id="b2618-117">**RegisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="b2618-117">**RegisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | <span data-ttu-id="b2618-118">Registra a instância ativa de um aplicativo para reinicializar.</span><span class="sxs-lookup"><span data-stu-id="b2618-118">Registers the active instance of an application for restart.</span></span>                               |
| [<span data-ttu-id="b2618-119">**UnregisterApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="b2618-119">**UnregisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | <span data-ttu-id="b2618-120">Remove a instância ativa de um aplicativo da lista de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b2618-120">Removes the active instance of an application from the recovery list.</span></span>                      |
| [<span data-ttu-id="b2618-121">**UnregisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="b2618-121">**UnregisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | <span data-ttu-id="b2618-122">Remove a instância ativa de um aplicativo da lista de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="b2618-122">Removes the active instance of an application from the restart list.</span></span>                       |



 

 

 