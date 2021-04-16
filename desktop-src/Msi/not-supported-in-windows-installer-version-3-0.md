---
description: O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer&\# 160; 3.0 e versões anteriores.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Sem suporte no Windows Installer 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787074"
---
# <a name="not-supported-in-windows-installer-30"></a><span data-ttu-id="fb2ae-103">Sem suporte no Windows Installer 3,0</span><span class="sxs-lookup"><span data-stu-id="fb2ae-103">Not Supported in Windows Installer 3.0</span></span>

<span data-ttu-id="fb2ae-104">O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer 3,0 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-104">The Windows Installer functions, tables, and properties listed on this page are not supported by Windows Installer 3.0 and earlier versions.</span></span> <span data-ttu-id="fb2ae-105">A ausência de um recurso dessa lista não garante que o recurso tenha suporte.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-105">The absence of a feature from this list does not guarantee that the feature is supported.</span></span> <span data-ttu-id="fb2ae-106">Consulte a documentação principal para determinar qual versão de Windows Installer é necessária para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-106">See the main documentation to determine which Windows Installer version is required for a particular feature.</span></span> <span data-ttu-id="fb2ae-107">Para obter informações sobre outras versões do Windows Installer, consulte [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="fb2ae-107">For information about other Windows Installer versions see [What's New in Windows Installer](what-s-new-in-windows-installer.md).</span></span>

<span data-ttu-id="fb2ae-108">Windows Installer 3,0 está disponível para o Windows Server 2003, Windows XP ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-108">Windows Installer 3.0 is available for Windows Server 2003, Windows XP, or Windows 2000.</span></span> <span data-ttu-id="fb2ae-109">Para obter uma lista de todas as versões e redistribuíveis do Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="fb2ae-109">For a list of all Windows Installer versions and redistributables, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

<span data-ttu-id="fb2ae-110">Os recursos a seguir não têm suporte no Windows Installer 3,0 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-110">The following features are not supported in Windows Installer 3.0 and earlier versions.</span></span>

[<span data-ttu-id="fb2ae-111">Funções do instalador</span><span class="sxs-lookup"><span data-stu-id="fb2ae-111">Installer Functions</span></span>](installer-functions.md)

-   [<span data-ttu-id="fb2ae-112">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="fb2ae-112">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="fb2ae-113">**MsiNotifySidChange**</span><span class="sxs-lookup"><span data-stu-id="fb2ae-113">**MsiNotifySidChange**</span></span>](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

<span data-ttu-id="fb2ae-114">Protótipo de função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="fb2ae-114">Callback Function Prototype</span></span>

-   [<span data-ttu-id="fb2ae-115">**\_registro do manipulador INSTALLUI \_**</span><span class="sxs-lookup"><span data-stu-id="fb2ae-115">**INSTALLUI\_HANDLER\_RECORD**</span></span>](/windows/win32/api/msi/nc-msi-installui_handler_record)

[<span data-ttu-id="fb2ae-116">Tabelas de banco de dados</span><span class="sxs-lookup"><span data-stu-id="fb2ae-116">Database Tables</span></span>](database-tables.md)

-   <span data-ttu-id="fb2ae-117">A coluna Value da [tabela MsiPatchMetadata](msipatchmetadata-table.md) aceita **OptimizedInstallMode** e **MinorUpdateTargetRTM**.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-117">The Value column of the [MsiPatchMetadata Table](msipatchmetadata-table.md) accepts **OptimizedInstallMode** and **MinorUpdateTargetRTM**.</span></span>

[<span data-ttu-id="fb2ae-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb2ae-118">Properties</span></span>](properties.md)

-   [<span data-ttu-id="fb2ae-119">**Propriedade Msix64**</span><span class="sxs-lookup"><span data-stu-id="fb2ae-119">**Msix64 Property**</span></span>](msix64.md)

[<span data-ttu-id="fb2ae-120">Windows Installer em sistemas operacionais de 64 bits</span><span class="sxs-lookup"><span data-stu-id="fb2ae-120">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)

-   <span data-ttu-id="fb2ae-121">A [**Propriedade Summary do modelo**](template-summary.md) aceita o valor x64.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-121">The [**Template Summary Property**](template-summary.md) accepts the value x64.</span></span>

[<span data-ttu-id="fb2ae-122">Avaliadores de consistência internos-ICEs</span><span class="sxs-lookup"><span data-stu-id="fb2ae-122">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

-   [<span data-ttu-id="fb2ae-123">ICE99</span><span class="sxs-lookup"><span data-stu-id="fb2ae-123">ICE99</span></span>](ice99.md)

 

 
