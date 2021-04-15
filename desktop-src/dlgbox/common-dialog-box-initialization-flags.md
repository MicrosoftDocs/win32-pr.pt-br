---
title: Sinalizadores de inicialização de caixa de diálogo comum
description: Os sinalizadores são usados para modificar o comportamento e a aparência de uma caixa de diálogo comum.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Biblioteca de caixa de diálogo comum, inicializando
- caixas de diálogo comuns, inicializando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/19/2020
ms.locfileid: "104454484"
---
# <a name="common-dialog-box-initialization-flags"></a><span data-ttu-id="e4fda-105">Sinalizadores de inicialização de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="e4fda-105">Common Dialog Box Initialization Flags</span></span>

<span data-ttu-id="e4fda-106">Os sinalizadores são usados para modificar o comportamento e a aparência de uma caixa de diálogo comum.</span><span class="sxs-lookup"><span data-stu-id="e4fda-106">Flags are used to modify the behavior and appearance of a common dialog box.</span></span> <span data-ttu-id="e4fda-107">Os sinalizadores de inicialização são os valores que você define no membro **flags** da estrutura que é usada para criar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e4fda-107">Initialization flags are the values that you set in the **Flags** member of the structure that is used to create the dialog box.</span></span> <span data-ttu-id="e4fda-108">Você usa os sinalizadores para especificar quais controles em uma caixa de diálogo recebem valores iniciais, para desabilitar os controles selecionados e para modificar o intervalo de valores que o usuário pode definir com os controles.</span><span class="sxs-lookup"><span data-stu-id="e4fda-108">You use the flags to specify which controls in a dialog box receive initial values, to disable selected controls, and to modify the range of values that the user can set with the controls.</span></span> <span data-ttu-id="e4fda-109">Você também usa os sinalizadores para habilitar os procedimentos de conexão e modelos personalizados para as caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e4fda-109">You also use the flags to enable hook procedures and custom templates for the dialog boxes.</span></span>

<span data-ttu-id="e4fda-110">Por exemplo, você pode definir o valor de **\_ efeitos do CF** no membro **flags** da estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para direcionar a caixa de diálogo **fonte** para exibir os controles de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e4fda-110">For example, you can set the **CF\_EFFECTS** value in the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to direct the **Font** dialog box to display the effects controls.</span></span> <span data-ttu-id="e4fda-111">Esses controles permitem que o usuário escolha uma cor de fonte, bem como efeitos de tachado e sublinhado.</span><span class="sxs-lookup"><span data-stu-id="e4fda-111">These controls let the user choose a font color as well as strikethrough and underline effects.</span></span>

<span data-ttu-id="e4fda-112">Os valores do sinalizador de inicialização são exclusivos de cada caixa de diálogo comum e são descritos detalhadamente pelos membros dos **sinalizadores** das seguintes estruturas que correspondem a eles:</span><span class="sxs-lookup"><span data-stu-id="e4fda-112">The initialization flag values are unique to each common dialog box and are described in detail by the **Flags** members of the following structures that correspond to them:</span></span>

-   [<span data-ttu-id="e4fda-113">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="e4fda-113">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [<span data-ttu-id="e4fda-114">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="e4fda-114">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="e4fda-115">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="e4fda-115">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [<span data-ttu-id="e4fda-116">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="e4fda-116">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [<span data-ttu-id="e4fda-117">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="e4fda-117">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [<span data-ttu-id="e4fda-118">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="e4fda-118">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [<span data-ttu-id="e4fda-119">**PRINTDLGEX**</span><span class="sxs-lookup"><span data-stu-id="e4fda-119">**PRINTDLGEX**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




