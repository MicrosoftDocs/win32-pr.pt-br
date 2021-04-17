---
description: As Adminproperties devem ser criadas na tabela de propriedades.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Propriedade adminproperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757132"
---
# <a name="adminproperties-property"></a><span data-ttu-id="62dfa-103">Propriedade adminproperties</span><span class="sxs-lookup"><span data-stu-id="62dfa-103">AdminProperties property</span></span>

<span data-ttu-id="62dfa-104">As **adminproperties** devem ser criadas na tabela de [Propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="62dfa-104">The **AdminProperties** should be authored into the [Property Table](property-table.md).</span></span> <span data-ttu-id="62dfa-105">O valor de **adminproperties** é uma lista de nomes de propriedade separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="62dfa-105">The value of **AdminProperties** is a list of property names separated by semicolons.</span></span> <span data-ttu-id="62dfa-106">O instalador salva os valores dessas propriedades listadas no momento de uma [instalação administrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="62dfa-106">The installer saves the values of these listed properties at the time of an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="62dfa-107">Quando os usuários instalam a partir da imagem administrativa, a instalação usa os valores salvos das propriedades, em vez dos valores no arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="62dfa-107">When users install from the administrative image, the installation uses the saved values of the properties, rather than the values in the .msi file.</span></span>

## <a name="remarks"></a><span data-ttu-id="62dfa-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="62dfa-108">Remarks</span></span>

<span data-ttu-id="62dfa-109">Os nomes de propriedade na lista podem ser letras maiúsculas e minúsculas (propriedades particulares) ou todas as letras maiúsculas (propriedades públicas).</span><span class="sxs-lookup"><span data-stu-id="62dfa-109">The property names in the list can be uppercase and lowercase letters (private properties), or all uppercase (public properties).</span></span>

<span data-ttu-id="62dfa-110">Essa propriedade nunca deve terminar com um ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="62dfa-110">This property must never end with a semicolon.</span></span>

## <a name="requirements"></a><span data-ttu-id="62dfa-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62dfa-111">Requirements</span></span>



| <span data-ttu-id="62dfa-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="62dfa-112">Requirement</span></span> | <span data-ttu-id="62dfa-113">Valor</span><span class="sxs-lookup"><span data-stu-id="62dfa-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62dfa-114">Versão</span><span class="sxs-lookup"><span data-stu-id="62dfa-114">Version</span></span><br/> | <span data-ttu-id="62dfa-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62dfa-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62dfa-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62dfa-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62dfa-117">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="62dfa-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="62dfa-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="62dfa-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62dfa-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="62dfa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62dfa-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62dfa-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




