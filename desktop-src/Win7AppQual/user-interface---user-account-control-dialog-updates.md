---
description: .
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Interface do usuário – atualizações da caixa de diálogo controle de conta de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5711f8bbed029102bea81e0f4cfcbd4649b5a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785260"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="3d287-103">Interface do usuário – atualizações da caixa de diálogo controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="3d287-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="3d287-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="3d287-104">Affected Platforms</span></span>

<span data-ttu-id="3d287-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d287-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="3d287-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d287-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="3d287-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="3d287-107">Feature Impact</span></span>

<span data-ttu-id="3d287-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="3d287-108">**Severity** - Low</span></span>  
<span data-ttu-id="3d287-109">**Frequência** -média</span><span class="sxs-lookup"><span data-stu-id="3d287-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="3d287-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d287-110">Description</span></span>

<span data-ttu-id="3d287-111">No Windows 7, nós padronizamos as opções da caixa de diálogo UAC.</span><span class="sxs-lookup"><span data-stu-id="3d287-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="3d287-112">Anteriormente, os usuários tinham que selecionar entre várias opções, por exemplo, "continuar", "Cancelar" e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3d287-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="3d287-113">Agora, todas as caixas de diálogo fornecem aos usuários um simples "Sim" ou "não".</span><span class="sxs-lookup"><span data-stu-id="3d287-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="3d287-114">O layout da caixa de diálogo agora também mostra claramente o nome do programa, o editor e a origem.</span><span class="sxs-lookup"><span data-stu-id="3d287-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="3d287-115">Aproveitando os recursos do recurso</span><span class="sxs-lookup"><span data-stu-id="3d287-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="3d287-116">Os requisitos de desenvolvimento de aplicativos no Windows 7 para compatibilidade com o UAC são os mesmos do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3d287-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="3d287-117">Os aplicativos compatíveis com o Windows Vista irão interagir com o UAC no Windows 7 sem nenhuma modificação.</span><span class="sxs-lookup"><span data-stu-id="3d287-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="3d287-118">Consulte os tópicos de controle de conta de usuário no guia de *compatibilidade de aplicativos do Windows Vista* para obter informações sobre como fazer com que os aplicativos do Windows XP funcionem corretamente no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d287-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="3d287-119">Embora as melhorias do UAC para o Windows 7 tenham impacto sobre a experiência do usuário, elas não afetarão a interface do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3d287-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="3d287-120">No entanto, se houver qualquer conteúdo de ajuda vinculado às caixas de diálogo do UAC, talvez seja necessário atualizar as capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="3d287-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="3d287-121">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="3d287-121">Links to Other Resources</span></span>

-   <span data-ttu-id="3d287-122">[Manual de compatibilidade de aplicativos do Windows Vista](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3d287-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="3d287-123">Download do kit de ferramentas de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="3d287-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="3d287-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="3d287-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="3d287-125">Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.</span><span class="sxs-lookup"><span data-stu-id="3d287-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
