---
description: A definição da propriedade ARPNOMODIFY desabilita a funcionalidade adicionar ou remover programas no painel de controle que modifica o produto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propriedade ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749595"
---
# <a name="arpnomodify-property"></a><span data-ttu-id="82bff-103">Propriedade ARPNOMODIFY</span><span class="sxs-lookup"><span data-stu-id="82bff-103">ARPNOMODIFY property</span></span>

<span data-ttu-id="82bff-104">A definição da propriedade **ARPNOMODIFY** desabilita a funcionalidade adicionar ou remover programas no painel de controle que modifica o produto.</span><span class="sxs-lookup"><span data-stu-id="82bff-104">Setting the **ARPNOMODIFY** property disables Add or Remove Programs functionality in Control Panel that modifies the product.</span></span> <span data-ttu-id="82bff-105">Para o Windows 2000, isso desabilita o botão **Modificar** do produto em **Adicionar ou remover programas** no painel de **controle**.</span><span class="sxs-lookup"><span data-stu-id="82bff-105">For Windows 2000, this disables the **Modify** button for the product in **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="82bff-106">Em sistemas operacionais anteriores, clicar no botão **Adicionar ou remover programas** desinstala o produto em vez de entrar no assistente de modo de manutenção.</span><span class="sxs-lookup"><span data-stu-id="82bff-106">On earlier operating systems, clicking the **Add or Remove Programs** button uninstalls the product rather than entering the maintenance mode wizard.</span></span>

<span data-ttu-id="82bff-107">Se a propriedade **ARPNOMODIFY** for definida, a [ação RegisterProduct](registerproduct-action.md) gravará o valor "NoModify" na chave do registro:</span><span class="sxs-lookup"><span data-stu-id="82bff-107">If the **ARPNOMODIFY** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoModify" under the registry key:</span></span>

<span data-ttu-id="82bff-108">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ o **{*chave do produto*}**</span><span class="sxs-lookup"><span data-stu-id="82bff-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="82bff-109">Se a propriedade **ARPNOMODIFY** for definida e a propriedade [**ARPNOREMOVE**](arpnoremove.md) não estiver definida, a ação RegisterProduct também gravará o valor de UninstallString nessa chave.</span><span class="sxs-lookup"><span data-stu-id="82bff-109">If the **ARPNOMODIFY** property is set and the [**ARPNOREMOVE**](arpnoremove.md) property is not set, the RegisterProduct action also writes the UninstallString value under this key.</span></span> <span data-ttu-id="82bff-110">O valor de Desinstalastring é uma linha de comando para remover o produto, em vez de reconfigurar o produto.</span><span class="sxs-lookup"><span data-stu-id="82bff-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="82bff-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="82bff-111">Remarks</span></span>

<span data-ttu-id="82bff-112">No Windows 2000, isso desabilita o botão **alterar** do produto em **Adicionar ou remover programas** do **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="82bff-112">On Windows 2000, this disables the **Change** button for the product in the **Add or Remove Programs** of the **Control Panel**.</span></span>

<span data-ttu-id="82bff-113">Essa propriedade pode ser definida por uma transformação de personalização para impedir que os usuários alterem a personalização de um administrador por meio de **Adicionar ou remover programas**.</span><span class="sxs-lookup"><span data-stu-id="82bff-113">This property can be set by a customization transform to prevent users from changing an administrator's customization through **Add or Remove Programs**.</span></span> <span data-ttu-id="82bff-114">Essa propriedade só afeta **Adicionar ou remover programas**.</span><span class="sxs-lookup"><span data-stu-id="82bff-114">This property only affects **Add or Remove Programs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="82bff-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82bff-115">Requirements</span></span>



| <span data-ttu-id="82bff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="82bff-116">Requirement</span></span> | <span data-ttu-id="82bff-117">Valor</span><span class="sxs-lookup"><span data-stu-id="82bff-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82bff-118">Versão</span><span class="sxs-lookup"><span data-stu-id="82bff-118">Version</span></span><br/> | <span data-ttu-id="82bff-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82bff-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="82bff-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="82bff-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="82bff-121">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="82bff-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="82bff-122">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="82bff-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82bff-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="82bff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bff-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82bff-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="82bff-125">Um exemplo de transformação de personalização</span><span class="sxs-lookup"><span data-stu-id="82bff-125">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> </dl>

 

 




