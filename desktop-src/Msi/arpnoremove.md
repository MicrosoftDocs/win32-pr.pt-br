---
description: A configuração da propriedade ARPNOREMOVE desabilita a funcionalidade adicionar ou remover programas no painel de controle que remove o produto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Propriedade ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770386"
---
# <a name="arpnoremove-property"></a><span data-ttu-id="48a7d-103">Propriedade ARPNOREMOVE</span><span class="sxs-lookup"><span data-stu-id="48a7d-103">ARPNOREMOVE property</span></span>

<span data-ttu-id="48a7d-104">A configuração da propriedade **ARPNOREMOVE** desabilita a funcionalidade **Adicionar ou remover programas** no **painel de controle** que remove o produto.</span><span class="sxs-lookup"><span data-stu-id="48a7d-104">Setting the **ARPNOREMOVE** property disables the **Add or Remove Programs** functionality in **Control Panel** that removes the product.</span></span> <span data-ttu-id="48a7d-105">Para o Windows 2000, isso desabilita o botão **remover** do produto em **Adicionar ou remover programas** no **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="48a7d-105">For Windows 2000, this disables the **Remove** button for the product from the **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="48a7d-106">Para sistemas operacionais anteriores, isso tem o efeito de remover o produto da lista de produtos instalados em **Adicionar ou remover programas** no painel de **controle**.</span><span class="sxs-lookup"><span data-stu-id="48a7d-106">For earlier operating systems, this has the effect of removing the product from the list of installed products on the **Add or Remove Programs** in **Control Panel**.</span></span>

<span data-ttu-id="48a7d-107">Se a propriedade **ARPNOREMOVE** for definida, a [ação RegisterProduct](registerproduct-action.md) gravará o valor "NoRemove" na chave do registro:</span><span class="sxs-lookup"><span data-stu-id="48a7d-107">If the **ARPNOREMOVE** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoRemove" under the registry key:</span></span>

<span data-ttu-id="48a7d-108">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ o **{*chave do produto*}**</span><span class="sxs-lookup"><span data-stu-id="48a7d-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="48a7d-109">A definição da propriedade **ARPNOREMOVE** impede que o valor desinstallstring seja gravado nessa chave.</span><span class="sxs-lookup"><span data-stu-id="48a7d-109">Setting the **ARPNOREMOVE** property prevents the UninstallString value from being written under this key.</span></span> <span data-ttu-id="48a7d-110">O valor de Desinstalastring é uma linha de comando para remover o produto, em vez de reconfigurar o produto.</span><span class="sxs-lookup"><span data-stu-id="48a7d-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="48a7d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="48a7d-111">Remarks</span></span>

<span data-ttu-id="48a7d-112">Por exemplo, essa propriedade pode ser definida durante uma transformação de personalização para impedir que os usuários removam uma personalização do administrador.</span><span class="sxs-lookup"><span data-stu-id="48a7d-112">For example, this property can be set during a customization transform to prevent users from removing an administrator customization.</span></span>

## <a name="requirements"></a><span data-ttu-id="48a7d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48a7d-113">Requirements</span></span>



| <span data-ttu-id="48a7d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a7d-114">Requirement</span></span> | <span data-ttu-id="48a7d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="48a7d-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a7d-116">Versão</span><span class="sxs-lookup"><span data-stu-id="48a7d-116">Version</span></span><br/> | <span data-ttu-id="48a7d-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="48a7d-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="48a7d-118">Windows Installer 4,0 ou Windows Installer 4,5 ou posterior no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="48a7d-118">Windows Installer 4.0 or Windows Installer 4.5 or later on Windows Vista.</span></span> <span data-ttu-id="48a7d-119">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="48a7d-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="48a7d-120">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48a7d-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48a7d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="48a7d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a7d-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48a7d-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




