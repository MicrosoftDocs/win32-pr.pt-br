---
description: A ação InstallInitialize e a ação InstallFinalize marcam o início e o final de uma sequência de ações que alteram o sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Ação InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647325"
---
# <a name="installinitialize-action"></a><span data-ttu-id="ef78b-103">Ação InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="ef78b-103">InstallInitialize Action</span></span>

<span data-ttu-id="ef78b-104">A ação InstallInitialize e a ação [InstallFinalize](installfinalize-action.md) marcam o início e o final de uma sequência de ações que alteram o sistema.</span><span class="sxs-lookup"><span data-stu-id="ef78b-104">The InstallInitialize action and [InstallFinalize](installfinalize-action.md) action mark the beginning and end of a sequence of actions that change the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ef78b-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="ef78b-105">Sequence Restrictions</span></span>

<span data-ttu-id="ef78b-106">A ação InstallInitialize deve ser sequenciada antes de qualquer ação que altere o sistema, como a ação [InstallFiles](installfiles-action.md) , a ação [WriteRegistryValues](writeregistryvalues-action.md) , a ação [SelfRegModules](selfregmodules-action.md) e a ação [ProcessComponents](processcomponents-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ef78b-106">The InstallInitialize action must be sequenced before any actions that change the system, such as the [InstallFiles](installfiles-action.md) action, the [WriteRegistryValues](writeregistryvalues-action.md) action, the [SelfRegModules](selfregmodules-action.md) action, and the [ProcessComponents](processcomponents-action.md) action.</span></span> <span data-ttu-id="ef78b-107">A ação InstallInitialize deve, portanto, ser sequenciada antes da ação [InstallFinalize](installfinalize-action.md) e da ação [InstallExecute](installexecute-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ef78b-107">The InstallInitialize action must therefore be sequenced before the [InstallFinalize](installfinalize-action.md) action and the [InstallExecute](installexecute-action.md) action.</span></span>

<span data-ttu-id="ef78b-108">As [ações personalizadas](custom-actions.md) que modificam o pacote de Windows Installer, por exemplo, adicionando linhas a uma tabela que manipula recursos instaláveis, como a tabela de [registro](registry-table.md) ou a tabela [duplicatafile](duplicatefile-table.md) , devem ser sequenciadas antes da ação InstallInitialize.</span><span class="sxs-lookup"><span data-stu-id="ef78b-108">[Custom actions](custom-actions.md) that modify the Windows Installer package, for example by adding rows to a table that handles installable resources, such as the [Registry](registry-table.md) table or [DuplicateFile](duplicatefile-table.md) table, must be sequenced before InstallInitialize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ef78b-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="ef78b-109">ActionData Messages</span></span>

<span data-ttu-id="ef78b-110">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="ef78b-110">There are no ActionData messages.</span></span>

 

 



