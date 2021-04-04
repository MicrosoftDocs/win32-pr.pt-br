---
title: Apêndice D notas para desenvolvedores de Visual Basic
description: Esta seção fornece informações sobre o Microsoft Acessibilidade Ativa para desenvolvedores do Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916216"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a><span data-ttu-id="595c0-103">Apêndice D: notas para desenvolvedores de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="595c0-103">Appendix D: Notes for Visual Basic Developers</span></span>

<span data-ttu-id="595c0-104">Esta seção fornece informações sobre o Microsoft Acessibilidade Ativa para desenvolvedores do Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="595c0-104">This section provides information about Microsoft Active Accessibility for Microsoft Visual Basic developers.</span></span>

<span data-ttu-id="595c0-105">Os aplicativos escritos em Visual Basic são clientes do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="595c0-105">Applications written in Visual Basic are Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="595c0-106">Eles não fornecem informações sobre seus elementos personalizados da interface do usuário porque não implementam o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou qualquer outra interface COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="595c0-106">They do not provide information about their custom user interface elements because they do not implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or any other Component Object Model (COM) interface.</span></span>

<span data-ttu-id="595c0-107">Esta documentação usa os nomes de C/C++ para as propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ; no entanto, os nomes de Visual Basic são semelhantes.</span><span class="sxs-lookup"><span data-stu-id="595c0-107">This documentation uses the C/C++ names for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties; however, the Visual Basic names are similar.</span></span> <span data-ttu-id="595c0-108">Por exemplo, a propriedade [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) seria chamada de **accName** em um aplicativo Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="595c0-108">For example, the [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) property would be called **accName** in a Visual Basic application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="595c0-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="595c0-109">In this section</span></span>

-   [<span data-ttu-id="595c0-110">Visual Basic observações do método: accName</span><span class="sxs-lookup"><span data-stu-id="595c0-110">Visual Basic Method Notes: accName</span></span>](visual-basic-method-notes--accname.md)
-   [<span data-ttu-id="595c0-111">Visual Basic observações do método: accValue</span><span class="sxs-lookup"><span data-stu-id="595c0-111">Visual Basic Method Notes: accValue</span></span>](visual-basic-method-notes--accvalue.md)
-   [<span data-ttu-id="595c0-112">Visual Basic programas de exemplo</span><span class="sxs-lookup"><span data-stu-id="595c0-112">Visual Basic Sample Programs</span></span>](visual-basic-sample-programs.md)

 

 




