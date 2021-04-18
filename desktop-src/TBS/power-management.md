---
title: Gerenciamento de energia (serviços base do TPM)
description: O TBS recebe eventos de gerenciamento de energia.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "105756343"
---
# <a name="power-management-tpm-base-services"></a><span data-ttu-id="e7f31-103">Gerenciamento de energia (serviços base do TPM)</span><span class="sxs-lookup"><span data-stu-id="e7f31-103">Power Management (TPM Base Services)</span></span>

<span data-ttu-id="e7f31-104">O TBS recebe eventos de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="e7f31-104">The TBS receives power management events.</span></span> <span data-ttu-id="e7f31-105">Quando é recebida uma indicação de que o TPM ou outras partes da plataforma estão prestes a entrar em um estado de energia no qual a execução será interrompida ou o estado do TPM será perdido, o TBS verificará se o comando em execução no momento provavelmente será concluído antes de o sistema ser desligado.</span><span class="sxs-lookup"><span data-stu-id="e7f31-105">When an indication is received that the TPM or other parts of the platform are about to enter a power state in which execution will be interrupted or TPM state will be lost, the TBS checks to determine whether the currently executing command is likely to finish before the system powers down.</span></span> <span data-ttu-id="e7f31-106">Em geral, o TBS permite que os comandos de duração curta e média sejam concluídos, mas cancela comandos de duração longa.</span><span class="sxs-lookup"><span data-stu-id="e7f31-106">In general, the TBS allows short and medium duration commands to finish, but cancels long duration commands.</span></span> <span data-ttu-id="e7f31-107">Depois que o comando for retornado, o TBS interromperá o envio de novos comandos para o TPM e se preparará para hibernação.</span><span class="sxs-lookup"><span data-stu-id="e7f31-107">After the command has returned, the TBS stops sending new commands to the TPM and prepares itself for hibernation.</span></span> <span data-ttu-id="e7f31-108">Quando a energia é restaurada, o TBS retorna o resultado do comando para o chamador e, em seguida, prossegue com o processamento de comandos TBS pendentes.</span><span class="sxs-lookup"><span data-stu-id="e7f31-108">When power is restored, the TBS returns the result of the command to the caller, and then proceeds with processing pending TBS commands.</span></span> <span data-ttu-id="e7f31-109">O código de gerenciamento de energia TBS é executado de forma assíncrona, portanto, ele pode lidar com solicitações de gerenciamento de energia, mesmo que o TPM esteja processando um comando longo.</span><span class="sxs-lookup"><span data-stu-id="e7f31-109">The TBS power management code runs asynchronously, so it can handle power management requests even if the TPM is processing a long command.</span></span>

<span data-ttu-id="e7f31-110">Quando um computador entra nos Estados de suspensão, incluindo S3 (suspensão) e S4 (hibernação), o TPM é desligado.</span><span class="sxs-lookup"><span data-stu-id="e7f31-110">When a computer enters sleep states, including S3 (sleep) and S4 (hibernation), the TPM is powered off.</span></span> <span data-ttu-id="e7f31-111">Assim, todos os Estados de TPM não persistentes são perdidos.</span><span class="sxs-lookup"><span data-stu-id="e7f31-111">Thus, all nonpersistent TPM states are lost.</span></span> <span data-ttu-id="e7f31-112">Antes de entrar nesses Estados, espera-se que o software de aplicativo se prepare para a perda de Estados do TPM volátil.</span><span class="sxs-lookup"><span data-stu-id="e7f31-112">Before entering these states, application software is expected to prepare for the loss of volatile TPM states.</span></span> <span data-ttu-id="e7f31-113">Quando o sistema retorna de um estado de suspensão, o TBS sincroniza com o TPM para que o estado TBS seja consistente com o estado do TPM.</span><span class="sxs-lookup"><span data-stu-id="e7f31-113">When the system returns from a sleep state, the TBS synchronizes with the TPM so that the TBS state is consistent with the TPM state.</span></span> <span data-ttu-id="e7f31-114">O software de aplicativo pode precisar emitir comandos que foram interrompidos.</span><span class="sxs-lookup"><span data-stu-id="e7f31-114">Application software may need to reissue commands that were interrupted.</span></span>

 

 




