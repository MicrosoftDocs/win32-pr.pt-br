---
description: Durante uma instalação simultânea, o instalador define a propriedade ParentProductCode na sessão da instalação simultânea com o mesmo valor que a propriedade ProductCode na sessão da instalação pai.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: Propriedade ParentProductCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82385a4df94d3a044f0ee6a77461d69e63cc6d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748147"
---
# <a name="parentproductcode-property"></a><span data-ttu-id="fc212-103">Propriedade ParentProductCode</span><span class="sxs-lookup"><span data-stu-id="fc212-103">ParentProductCode property</span></span>

<span data-ttu-id="fc212-104">Durante uma instalação simultânea, o instalador define a propriedade **ParentProductCode** na sessão da instalação simultânea com o mesmo valor que a propriedade [**ProductCode**](productcode.md) na sessão da instalação pai.</span><span class="sxs-lookup"><span data-stu-id="fc212-104">During a concurrent installation, the installer sets the **ParentProductCode** property in the concurrent installation's session to the same value as the [**ProductCode**](productcode.md) property in the parent installation's session.</span></span> <span data-ttu-id="fc212-105">As instalações pai executam as ações de instalação simultânea para executar uma instalação simultânea.</span><span class="sxs-lookup"><span data-stu-id="fc212-105">Parent installations run the concurrent installation actions to perform a concurrent installation.</span></span> <span data-ttu-id="fc212-106">Um pacote de instalação pode determinar se ele está sendo instalado por uma ação de instalação simultânea verificando o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="fc212-106">An installation package can determine whether it is being installed by a concurrent installation action by checking the value of this property.</span></span>

> [!Note]  
> <span data-ttu-id="fc212-107">As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público.</span><span class="sxs-lookup"><span data-stu-id="fc212-107">Concurrent Installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="fc212-108">Para obter informações sobre instalações simultâneas, consulte [instalações simultâneas](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="fc212-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="fc212-109">Essa propriedade não será definida se a instalação simultânea estiver sendo executada pela ação [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="fc212-109">This property is not set if the concurrent installation is being run by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="fc212-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc212-110">Remarks</span></span>

<span data-ttu-id="fc212-111">Para impedir que um pacote nunca seja instalado como uma instalação simultânea, adicione uma das instruções condicionais a seguir à tabela [LaunchCondition](launchcondition-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fc212-111">To prevent a package from ever being installed as a concurrent installation, add either of the following conditional statements to the [LaunchCondition](launchcondition-table.md) table.</span></span> <span data-ttu-id="fc212-112">Isso impede que o pacote nunca seja instalado por uma ação de instalação simultânea executada por outra instalação.</span><span class="sxs-lookup"><span data-stu-id="fc212-112">This prevents the package from ever being installed by a concurrent installation action run by another installation.</span></span> <span data-ttu-id="fc212-113">Isso não impede que o pacote seja instalado pela ação [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="fc212-113">This does not prevent the package from being installed by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a><span data-ttu-id="fc212-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc212-114">Requirements</span></span>



| <span data-ttu-id="fc212-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc212-115">Requirement</span></span> | <span data-ttu-id="fc212-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fc212-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc212-117">Versão</span><span class="sxs-lookup"><span data-stu-id="fc212-117">Version</span></span><br/> | <span data-ttu-id="fc212-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc212-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc212-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc212-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc212-120">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc212-120">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fc212-121">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fc212-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc212-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc212-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc212-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc212-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="fc212-124">**ParentOriginalDatabase**</span><span class="sxs-lookup"><span data-stu-id="fc212-124">**ParentOriginalDatabase**</span></span>](parentoriginaldatabase.md)
</dt> </dl>

 

 




