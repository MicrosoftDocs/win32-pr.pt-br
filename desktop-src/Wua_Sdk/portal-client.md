---
description: A API do WUA (agente de Windows Update) é um conjunto de interfaces COM que permitem que os administradores de sistema e os programadores acessem o Windows Update e o Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API do agente de Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646774"
---
# <a name="windows-update-agent-api"></a><span data-ttu-id="ae31f-103">API do agente de Windows Update</span><span class="sxs-lookup"><span data-stu-id="ae31f-103">Windows Update Agent API</span></span>

## <a name="purpose"></a><span data-ttu-id="ae31f-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="ae31f-104">Purpose</span></span>

<span data-ttu-id="ae31f-105">A API do WUA (agente de Windows Update) é um conjunto de interfaces COM que permitem que os administradores de sistema e os programadores acessem o Windows Update e o [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae31f-105">The Windows Update Agent (WUA) API is a set of COM interfaces that enable system administrators and programmers to access Windows Update and [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span></span> <span data-ttu-id="ae31f-106">Scripts e programas podem ser escritos para examinar quais atualizações estão disponíveis no momento para um computador e, em seguida, você pode instalar ou desinstalar atualizações.</span><span class="sxs-lookup"><span data-stu-id="ae31f-106">Scripts and programs can be written to examine which updates are currently available for a computer, and then you can install or uninstall updates.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="ae31f-107">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="ae31f-107">Where applicable</span></span>

<span data-ttu-id="ae31f-108">Os administradores do sistema podem usar o WUA para determinar programaticamente quais atualizações devem ser aplicadas a um computador, baixar essas atualizações e instalá-las com pouca ou nenhuma intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="ae31f-108">System administrators can use WUA to programmatically determine which updates should be applied to a computer, download those updates, and then install them with little or no user intervention.</span></span>

<span data-ttu-id="ae31f-109">ISVs (fornecedores independentes de software) e desenvolvedores de usuários finais podem integrar recursos do WUA ao gerenciamento do computador ou ao software de gerenciamento de atualizações para fornecer um ambiente operacional perfeitamente integrado.</span><span class="sxs-lookup"><span data-stu-id="ae31f-109">Independent software vendors (ISV) and end-user developers can integrate WUA features into computer management or update management software to provide a seamless operating environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ae31f-110">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="ae31f-110">Developer audience</span></span>

<span data-ttu-id="ae31f-111">Você pode escrever aplicativos WUA em várias linguagens de programação.</span><span class="sxs-lookup"><span data-stu-id="ae31f-111">You can write WUA applications in several programming languages.</span></span> <span data-ttu-id="ae31f-112">O WUA define interfaces e objetos que são acessíveis de Visual Basic, Visual Basic Scripting Edition (VBScript), JScript e de C e C++.</span><span class="sxs-lookup"><span data-stu-id="ae31f-112">WUA defines interfaces and objects that are accessible from Visual Basic, Visual Basic Scripting Edition (VBScript), JScript, and from C and C++.</span></span> <span data-ttu-id="ae31f-113">Uma familiaridade com a programação COM é útil para o programador do WUA.</span><span class="sxs-lookup"><span data-stu-id="ae31f-113">A familiarity with COM programming is useful to the WUA programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ae31f-114">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="ae31f-114">Run-time requirements</span></span>

<span data-ttu-id="ae31f-115">O WUA tem suporte a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae31f-115">WUA is supported starting with Windows XP.</span></span> <span data-ttu-id="ae31f-116">O WUA tem suporte no servidor a partir do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ae31f-116">WUA is supported on the server starting with Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ae31f-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ae31f-117">In this section</span></span>

-   [<span data-ttu-id="ae31f-118">Usando a API do agente de Windows Update</span><span class="sxs-lookup"><span data-stu-id="ae31f-118">Using the Windows Update Agent API</span></span>](using-the-windows-update-agent-api.md)
-   [<span data-ttu-id="ae31f-119">Referência da API do WUA</span><span class="sxs-lookup"><span data-stu-id="ae31f-119">WUA API Reference</span></span>](windows-update-agent--wua--api-reference.md)

 

 
