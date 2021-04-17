---
description: Para criar aplicativos de Tablet PC em C \# e Visual Basic .net, seu projeto no Microsoft Visual Studio .NET deve incluir uma referência aos assemblies da biblioteca gerenciada do Tablet PC. Isso fornece acesso ao modelo de objeto gerenciado e aos controles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Biblioteca gerenciada e controles (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768303"
---
# <a name="managed-library-and-controls-tablet-pc"></a><span data-ttu-id="e7123-104">Biblioteca gerenciada e controles (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="e7123-104">Managed Library and Controls (Tablet PC)</span></span>

<span data-ttu-id="e7123-105">Para criar aplicativos de Tablet PC em C \# e Visual Basic .net, seu projeto no Microsoft Visual Studio .NET deve incluir uma referência aos assemblies da biblioteca gerenciada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e7123-105">To build Tablet PC applications in C\# and Visual Basic .NET, your project in Microsoft Visual Studio .NET must include a reference to the Tablet PC managed library assemblies.</span></span> <span data-ttu-id="e7123-106">Isso fornece acesso ao modelo de objeto gerenciado e aos controles.</span><span class="sxs-lookup"><span data-stu-id="e7123-106">This provides access to the managed object model and controls.</span></span>

## <a name="microsoft-visual-c-and-visual-basicnet"></a><span data-ttu-id="e7123-107">Microsoft Visual C \# e visual Basic.net</span><span class="sxs-lookup"><span data-stu-id="e7123-107">Microsoft Visual C\# and Visual Basic.NET</span></span>

<span data-ttu-id="e7123-108">No Windows Vista, os assemblies da biblioteca gerenciada do Tablet PC são instalados por padrão em dois diretórios:</span><span class="sxs-lookup"><span data-stu-id="e7123-108">In Windows Vista, the Tablet PC managed library assemblies are installed by default in two directories:</span></span>

-   <span data-ttu-id="e7123-109"><systemdrive>: \\ Arquivos de programas \\ Arquivos comuns \\ diretório de tinta compartilhada da Microsoft \\</span><span class="sxs-lookup"><span data-stu-id="e7123-109"><systemdrive>:\\Program Files\\Common Files\\Microsoft Shared\\Ink directory</span></span>
-   <span data-ttu-id="e7123-110"><systemdrive>: \\ Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="e7123-110"><systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Bin</span></span>

<span data-ttu-id="e7123-111">Para adicionar uma referência às bibliotecas gerenciadas da plataforma do Tablet PC no Microsoft Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="e7123-111">To add a reference to the Tablet PC platform managed libraries in Microsoft Visual Studio .NET:</span></span>

1.  <span data-ttu-id="e7123-112">Abra seu projeto do Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="e7123-112">Open your Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="e7123-113">No menu **Projeto**, clique em **Adicionar Referência**.</span><span class="sxs-lookup"><span data-stu-id="e7123-113">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="e7123-114">Na guia **.net** da caixa de diálogo **Adicionar referência** , na lista componentes, selecione **API do Microsoft Tablet PC**.</span><span class="sxs-lookup"><span data-stu-id="e7123-114">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC API**.</span></span>
4.  <span data-ttu-id="e7123-115">Clique em **selecionar** e em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7123-115">Click **Select**, and then click **OK**.</span></span>

<span data-ttu-id="e7123-116">Para adicionar uma referência às APIs de análise de tinta no Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="e7123-116">To add a reference to the ink analysis APIs in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="e7123-117">Abra seu projeto Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="e7123-117">Open your Microsoft Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="e7123-118">No menu **Projeto**, clique em **Adicionar Referência**.</span><span class="sxs-lookup"><span data-stu-id="e7123-118">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="e7123-119">Na guia **.net** da caixa de diálogo **Adicionar referência** , na lista componentes, selecione **biblioteca gerenciada de análise de tinta do Microsoft Tablet PC**.</span><span class="sxs-lookup"><span data-stu-id="e7123-119">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC Ink Analysis Managed Library**.</span></span>
4.  <span data-ttu-id="e7123-120">Clique em **selecionar** e em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7123-120">Click **Select**, and then click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="e7123-121">Ao compilar aplicativos que usam Microsoft. Ink no Visual Studio 2005, você deve selecionar **projeto**, selecionar **Propriedades**, selecionar **Compilar** e definir destino da plataforma = x86.</span><span class="sxs-lookup"><span data-stu-id="e7123-121">When compiling applications that use Microsoft.Ink on Visual Studio 2005, you must select **Project**, select **Properties**, select **Build** and set Platform target=x86.</span></span> <span data-ttu-id="e7123-122">Essa opção não está disponível em produtos Microsoft Visual Studio Express.</span><span class="sxs-lookup"><span data-stu-id="e7123-122">This option is not available in Microsoft Visual Studio Express products.</span></span>

 

 

 



