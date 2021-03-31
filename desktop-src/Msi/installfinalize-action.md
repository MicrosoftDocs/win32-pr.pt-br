---
description: A ação InstallFinalize executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a execução das ações InstallExecute ou InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Ação InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647654"
---
# <a name="installfinalize-action"></a><span data-ttu-id="d66f0-103">Ação InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="d66f0-103">InstallFinalize Action</span></span>

<span data-ttu-id="d66f0-104">A ação InstallFinalize executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a execução das ações [InstallExecute](installexecute-action.md) ou [InstallExecuteAgain](installexecuteagain-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d66f0-104">The InstallFinalize action runs a script that contains all operations in the action sequence since either the start of the installation or the execution of the [InstallExecute](installexecute-action.md) or [InstallExecuteAgain](installexecuteagain-action.md) actions.</span></span> <span data-ttu-id="d66f0-105">Esta ação marca o final de uma transação que começa com a ação [InstallInitialize](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d66f0-105">This action marks the end of a transaction that begins with the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d66f0-106">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="d66f0-106">Sequence Restrictions</span></span>

<span data-ttu-id="d66f0-107">A ação [InstallInitialize](installinitialize-action.md) deve vir antes da ação InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="d66f0-107">The [InstallInitialize](installinitialize-action.md) action must come before the InstallFinalize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d66f0-108">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="d66f0-108">ActionData Messages</span></span>

<span data-ttu-id="d66f0-109">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="d66f0-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66f0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d66f0-110">Remarks</span></span>

<span data-ttu-id="d66f0-111">Se for detectado que o produto está marcado para remoção completa, as operações serão adicionadas automaticamente ao script para remover a **adição/remoção de programas** nas informações do **painel de controle** do produto, para cancelar o registro e cancelar a publicação do produto e remover o banco de dados local armazenado em cache de% Windows%, se existir.</span><span class="sxs-lookup"><span data-stu-id="d66f0-111">If it is detected that the product is marked for complete removal, operations are automatically added to the script to remove the **Add/Remove Programs** in the **Control Panel** information for the product, to unregister and unpublish the product, and to remove the cached local database from %WINDOWS%, if it exists.</span></span>

<span data-ttu-id="d66f0-112">As alterações do sistema feitas antes da ação não podem ser restauradas depois que a ação InstallFinalize é executada.</span><span class="sxs-lookup"><span data-stu-id="d66f0-112">System changes made before the action may not be restored after the InstallFinalize action is executed.</span></span> <span data-ttu-id="d66f0-113">A ação InstallFinalize atualiza o sistema com todas as operações determinadas para esse ponto e, em seguida, encerra a transação.</span><span class="sxs-lookup"><span data-stu-id="d66f0-113">The InstallFinalize action updates the system with all operations determined to that point and then ends the transaction.</span></span>

 

 



