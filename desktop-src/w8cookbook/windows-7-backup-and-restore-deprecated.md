---
title: Backup e restauração do Windows 7 preteridos
description: Backup e restauração do Windows 7 preteridos
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105782277"
---
# <a name="windows-7-backup-and-restore-deprecated"></a><span data-ttu-id="6683f-103">Backup e restauração do Windows 7 preteridos</span><span class="sxs-lookup"><span data-stu-id="6683f-103">Windows 7 Backup and Restore deprecated</span></span>

## <a name="platform"></a><span data-ttu-id="6683f-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="6683f-104">Platform</span></span>

<span data-ttu-id="6683f-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="6683f-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="6683f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6683f-106">Description</span></span>

<span data-ttu-id="6683f-107">Embora não haja nenhuma alteração comportamental para backup e restauração, essa função está sendo preterida e não será atualizada.</span><span class="sxs-lookup"><span data-stu-id="6683f-107">While there is no behavioral change to Backup and Restore, this function is being deprecated and will not be updated.</span></span> <span data-ttu-id="6683f-108">Ele raramente era usado e sua funcionalidade foi substituída pelo novo recurso de histórico de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6683f-108">It was rarely used and its functionality has been replaced by the new File History feature.</span></span> <span data-ttu-id="6683f-109">Ele será fornecido no Windows 8 e entusiastas que fizeram a atualização do Windows 7 para o Windows 8 ou que dependem do backup e restauração ou do backup de imagem de disco ainda poderão usá-lo.</span><span class="sxs-lookup"><span data-stu-id="6683f-109">It will ship in Windows 8 and enthusiasts who upgraded from Windows 7 to Windows 8 or depend on Backup and Restore or disk image backup will be still able to use it.</span></span> <span data-ttu-id="6683f-110">No entanto, todos os pontos de acesso para backup e restauração, com exceção do painel de controle, foram removidos.</span><span class="sxs-lookup"><span data-stu-id="6683f-110">However, all access points to Backup and Restore, with the exception of the Control Panel, have been removed.</span></span> <span data-ttu-id="6683f-111">O miniaplicativo do painel de controle usado pelo backup e restauração foi renomeado para recuperação de arquivo do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6683f-111">The Control Panel applet used by Backup and Restore was renamed to Windows 7 File Recovery.</span></span>

<span data-ttu-id="6683f-112">Os OEMs que estavam definindo a chave do registro para desabilitar a notificação de backup em suas imagens não precisarão mais fazer isso.</span><span class="sxs-lookup"><span data-stu-id="6683f-112">OEMs that were setting the registry key to disable backup notification in their images will no longer need to do that.</span></span>

<span data-ttu-id="6683f-113">Não recomendamos o uso de ambos os recursos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6683f-113">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="6683f-114">O histórico de arquivos verifica se o agendamento de backup existe e se está ativo e se encontra um, ele não permitirá que os usuários o ativem.</span><span class="sxs-lookup"><span data-stu-id="6683f-114">File History checks if Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="6683f-115">Nesse caso, os usuários que desejarem usar o histórico de arquivos precisarão excluir o agendamento de backup do Windows.</span><span class="sxs-lookup"><span data-stu-id="6683f-115">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="6683f-116">Manifestação</span><span class="sxs-lookup"><span data-stu-id="6683f-116">Manifestation</span></span>

<span data-ttu-id="6683f-117">Os fluxos de trabalho podem ser interrompidos e a documentação que se refere ao método anterior para acessar o recurso de backup e restauração do Windows precisará ser atualizada para refletir essas alterações.</span><span class="sxs-lookup"><span data-stu-id="6683f-117">Workflows may be interrupted and documentation that refers to the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="mitigation"></a><span data-ttu-id="6683f-118">Atenuação</span><span class="sxs-lookup"><span data-stu-id="6683f-118">Mitigation</span></span>

<span data-ttu-id="6683f-119">Os aplicativos que podem disparar backup e restauração devem ser regravados para verificar se o histórico de arquivos está ativado e permitir que os usuários escolham seu método preferido.</span><span class="sxs-lookup"><span data-stu-id="6683f-119">Apps that might trigger Backup and Restore should be rewritten to check if File History is on and let users choose their preferred method.</span></span>

 

 




