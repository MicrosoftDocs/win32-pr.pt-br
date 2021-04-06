---
description: O Windows Installer fornece muitas ações internas para executar o processo de instalação. Para obter uma lista dessas ações, consulte a referência de ações padrão.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011156"
---
# <a name="custom-actions"></a><span data-ttu-id="1eaf4-104">Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="1eaf4-104">Custom Actions</span></span>

<span data-ttu-id="1eaf4-105">O Windows Installer fornece muitas ações internas para executar o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-105">The Windows Installer provides many built-in actions for performing the installation process.</span></span> <span data-ttu-id="1eaf4-106">Para obter uma lista dessas ações, consulte a [referência de ações padrão](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1eaf4-106">For a list of these actions, see the [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="1eaf4-107">As ações padrão são suficientes para executar uma instalação na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-107">Standard actions are sufficient to execute an installation in most cases.</span></span> <span data-ttu-id="1eaf4-108">No entanto, há situações em que o desenvolvedor de um pacote de instalação descobre que é necessário gravar uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-108">However, there are situations where the developer of an installation package finds it necessary to write a custom action.</span></span> <span data-ttu-id="1eaf4-109">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1eaf4-109">For example:</span></span>

-   <span data-ttu-id="1eaf4-110">Você deseja iniciar um executável durante a instalação que está instalado no computador do usuário ou que está sendo instalado com o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-110">You want to launch an executable during installation that is installed on the user's machine or that is being installed with the application.</span></span>
-   <span data-ttu-id="1eaf4-111">Você deseja chamar funções especiais durante uma instalação que são definidas em uma DLL (biblioteca de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="1eaf4-111">You want to call special functions during an installation that are defined in a dynamic-link library (DLL).</span></span>
-   <span data-ttu-id="1eaf4-112">Você deseja usar funções escritas no texto linguagens de desenvolvimento Microsoft Visual Basic Scripting Edition ou script literal do Microsoft JScript, durante uma instalação.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-112">You want to use functions written in the development languages Microsoft Visual Basic Scripting Edition or Microsoft JScript literal script text during an installation.</span></span>
-   <span data-ttu-id="1eaf4-113">Você deseja adiar a execução de algumas ações até a hora em que o script de instalação está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-113">You want to defer the execution of some actions until the time when the installation script is being executed.</span></span>
-   <span data-ttu-id="1eaf4-114">Você deseja adicionar informações de hora e progresso a um controle ProgressBar e a um controle de texto de tempo restante.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-114">You want to add time and progress information to a ProgressBar control and a TimeRemaining Text control.</span></span>

<span data-ttu-id="1eaf4-115">As seções a seguir descrevem as ações personalizadas e como incorporá-las a um pacote de instalação:</span><span class="sxs-lookup"><span data-stu-id="1eaf4-115">The following sections describe custom actions and how to incorporate them into an installation package:</span></span>

-   [<span data-ttu-id="1eaf4-116">Sobre ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="1eaf4-116">About Custom Actions</span></span>](about-custom-actions.md)
-   [<span data-ttu-id="1eaf4-117">Usando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="1eaf4-117">Using Custom Actions</span></span>](using-custom-actions.md)
-   [<span data-ttu-id="1eaf4-118">Referência de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="1eaf4-118">Custom Action Reference</span></span>](custom-action-reference.md)
-   [<span data-ttu-id="1eaf4-119">Lista de Resumo de todos os tipos de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="1eaf4-119">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)

 

 



