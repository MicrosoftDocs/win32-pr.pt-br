---
description: A propriedade UPGRADINGPRODUCTCODE é definida por Windows Installer quando uma atualização remove um aplicativo.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propriedade UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751832"
---
# <a name="upgradingproductcode-property"></a><span data-ttu-id="ff9ee-103">Propriedade UPGRADINGPRODUCTCODE</span><span class="sxs-lookup"><span data-stu-id="ff9ee-103">UPGRADINGPRODUCTCODE property</span></span>

<span data-ttu-id="ff9ee-104">A propriedade **UPGRADINGPRODUCTCODE** é definida por Windows Installer quando uma atualização remove um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-104">The **UPGRADINGPRODUCTCODE** property is set by Windows Installer when an upgrade removes an application.</span></span> <span data-ttu-id="ff9ee-105">O instalador define essa propriedade quando executa a [ação RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ee-105">The installer sets this property when it runs the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="ff9ee-106">Essa propriedade não é definida removendo um aplicativo usando Adicionar ou remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-106">This property is not set by removing an application using the Add or Remove Programs in Control Panel.</span></span> <span data-ttu-id="ff9ee-107">Um aplicativo determina se ele está sendo removido por uma atualização ou adicionar ou remover programas, verificando **UPGRADINGPRODUCTCODE**.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-107">An application determines whether it is being removed by an upgrade or the Add or Remove Programs by checking **UPGRADINGPRODUCTCODE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff9ee-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff9ee-108">Requirements</span></span>



| <span data-ttu-id="ff9ee-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff9ee-109">Requirement</span></span> | <span data-ttu-id="ff9ee-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9ee-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9ee-111">Versão</span><span class="sxs-lookup"><span data-stu-id="ff9ee-111">Version</span></span><br/> | <span data-ttu-id="ff9ee-112">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ff9ee-113">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ff9ee-114">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ff9ee-115">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff9ee-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff9ee-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9ee-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ff9ee-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




