---
title: Propriedade Page
description: Propriedade Page
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363982"
---
# <a name="page-property"></a><span data-ttu-id="f7bbf-103">Propriedade Page</span><span class="sxs-lookup"><span data-stu-id="f7bbf-103">Page Property</span></span>

<span data-ttu-id="f7bbf-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f7bbf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f7bbf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="f7bbf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f7bbf-106">Retorna ou define a página exibida na janela da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f7bbf-106">Returns or sets the page displayed in the Microsoft Agent property sheet window.</span></span>

</dd> <dt>

<span data-ttu-id="f7bbf-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="f7bbf-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="f7bbf-108">\*Agent \* \* *.* \*  \[  =  *Cadeia de caracteres* PropertySheet.Page\]</span><span class="sxs-lookup"><span data-stu-id="f7bbf-108">*agent\*\*\*.PropertySheet.Page*\* \[ = *string*\]</span></span>



| <span data-ttu-id="f7bbf-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f7bbf-109">Part</span></span>     | <span data-ttu-id="f7bbf-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7bbf-110">Description</span></span>                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7bbf-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="f7bbf-111">*string*</span></span> | <span data-ttu-id="f7bbf-112">Uma expressão de cadeia de caracteres com um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f7bbf-112">A string expression with one of the following values.</span></span> <span data-ttu-id="f7bbf-113">**"Fala"** Exibe a página de entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="f7bbf-113">**"Speech"** Displays the Speech Input page.</span></span><br/> <span data-ttu-id="f7bbf-114">**"Saída"** Exibe a página saída.</span><span class="sxs-lookup"><span data-stu-id="f7bbf-114">**"Output"** Displays the Output page.</span></span><br/> <span data-ttu-id="f7bbf-115">**"Direitos autorais"** Exibe a página de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="f7bbf-115">**"Copyright"** Displays the Copyright page.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7bbf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7bbf-116">Remarks</span></span>

<span data-ttu-id="f7bbf-117">Se nenhum mecanismo de fala estiver instalado, a configuração **da página** como **"fala"** não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="f7bbf-117">If no speech engine is installed, setting **Page** to **"Speech"** has no effect.</span></span> <span data-ttu-id="f7bbf-118">Além disso, a propriedade **Visible** da janela deve ser definida como **true** para que o usuário veja a página.</span><span class="sxs-lookup"><span data-stu-id="f7bbf-118">Also, the window's **Visible** property must be set to **True** for the user to see the page.</span></span>

> [!Note]  
> <span data-ttu-id="f7bbf-119">O usuário pode substituir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f7bbf-119">The user can override this property.</span></span>

 

 

 





