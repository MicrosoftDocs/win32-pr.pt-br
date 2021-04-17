---
description: A propriedade instalada será definida somente se o produto estiver instalado por computador ou para o usuário atual.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propriedade instalada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747976"
---
# <a name="installed-property"></a><span data-ttu-id="dcda3-103">Propriedade instalada</span><span class="sxs-lookup"><span data-stu-id="dcda3-103">Installed property</span></span>

<span data-ttu-id="dcda3-104">A propriedade **instalada** será definida somente se o produto estiver instalado por computador ou para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="dcda3-104">The **Installed** property is set only if the product is installed per-machine or for the current user.</span></span> <span data-ttu-id="dcda3-105">Essa propriedade não será definida se o produto for instalado para um usuário diferente.</span><span class="sxs-lookup"><span data-stu-id="dcda3-105">This property is not set if the product is installed for a different user.</span></span>

<span data-ttu-id="dcda3-106">A propriedade **installed** pode ser usada em expressões condicionais para determinar se um produto está instalado por computador ou para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="dcda3-106">The **Installed** property can be used in conditional expressions to determine whether a product is installed per-computer or for the current user.</span></span> <span data-ttu-id="dcda3-107">Por exemplo, a propriedade pode ser usada na coluna condicional de uma tabela de sequência ou para diferenciar entre uma primeira instalação e uma instalação de manutenção.</span><span class="sxs-lookup"><span data-stu-id="dcda3-107">For example, the property can be used in the conditional column of a sequence table or to differentiate between a first installation and a maintenance installation.</span></span>

<span data-ttu-id="dcda3-108">Para determinar se o produto está instalado para um usuário diferente, verifique a propriedade [**productstate**](productstate.md) .</span><span class="sxs-lookup"><span data-stu-id="dcda3-108">To determine whether the product is installed for a different user, check the [**ProductState**](productstate.md) property.</span></span>

<span data-ttu-id="dcda3-109">O valor da propriedade [**ProductVersion**](productversion.md) é a versão do produto no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dcda3-109">The value of the [**ProductVersion**](productversion.md) property is the version of the product in string format.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcda3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcda3-110">Requirements</span></span>



| <span data-ttu-id="dcda3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcda3-111">Requirement</span></span> | <span data-ttu-id="dcda3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="dcda3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcda3-113">Versão</span><span class="sxs-lookup"><span data-stu-id="dcda3-113">Version</span></span><br/> | <span data-ttu-id="dcda3-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dcda3-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dcda3-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dcda3-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dcda3-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dcda3-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="dcda3-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="dcda3-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dcda3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcda3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcda3-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dcda3-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




