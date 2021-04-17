---
description: O valor da propriedade ProductVersion é a versão do produto no formato de cadeia de caracteres.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propriedade ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748970"
---
# <a name="productversion-property"></a><span data-ttu-id="0fe32-103">Propriedade ProductVersion</span><span class="sxs-lookup"><span data-stu-id="0fe32-103">ProductVersion property</span></span>

<span data-ttu-id="0fe32-104">O valor da propriedade **ProductVersion** é a versão do produto no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0fe32-104">The value of the **ProductVersion** property is the version of the product in string format.</span></span> <span data-ttu-id="0fe32-105">Essa propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="0fe32-105">This property is REQUIRED.</span></span>

<span data-ttu-id="0fe32-106">O formato da cadeia de caracteres é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0fe32-106">The format of the string is as follows:</span></span>

<dl> <span data-ttu-id="0fe32-107">major.minor.build</span><span class="sxs-lookup"><span data-stu-id="0fe32-107">major.minor.build</span></span>  
</dl>

<span data-ttu-id="0fe32-108">O primeiro campo é a versão principal e tem um valor máximo de 255.</span><span class="sxs-lookup"><span data-stu-id="0fe32-108">The first field is the major version and has a maximum value of 255.</span></span> <span data-ttu-id="0fe32-109">O segundo campo é a versão secundária e tem um valor máximo de 255.</span><span class="sxs-lookup"><span data-stu-id="0fe32-109">The second field is the minor version and has a maximum value of 255.</span></span> <span data-ttu-id="0fe32-110">O terceiro campo é chamado de versão de compilação ou versão de atualização e tem um valor máximo de 65.535.</span><span class="sxs-lookup"><span data-stu-id="0fe32-110">The third field is called the build version or the update version and has a maximum value of 65,535.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fe32-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fe32-111">Remarks</span></span>

<span data-ttu-id="0fe32-112">Pelo menos um dos três campos de **ProductVersion** deve ser alterado para uma atualização usando a [tabela de atualização](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="0fe32-112">At least one of the three fields of **ProductVersion** must change for an upgrade using the [Upgrade table](upgrade-table.md).</span></span> <span data-ttu-id="0fe32-113">Qualquer atualização que altere apenas o código do pacote, mas deixa o **ProductVersion** e o [**ProductCode**](productcode.md) inalterados é chamado de uma [pequena atualização](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="0fe32-113">Any update that changes only the package code, but leaves **ProductVersion** and [**ProductCode**](productcode.md) unchanged is called a [small update](small-updates.md).</span></span> <span data-ttu-id="0fe32-114">Os campos de três versões são fornecidos principalmente por conveniência.</span><span class="sxs-lookup"><span data-stu-id="0fe32-114">The three versions fields are provided primarily for convenience.</span></span> <span data-ttu-id="0fe32-115">Por exemplo, se você quiser alterar o **ProductVersion**, mas não quiser alterar as versões principal ou secundária, poderá alterar a versão da compilação.</span><span class="sxs-lookup"><span data-stu-id="0fe32-115">For example, if you want to change **ProductVersion**, but do not want to change either the major or minor versions, you can change the build version.</span></span>

<span data-ttu-id="0fe32-116">Observe que Windows Installer usa apenas os três primeiros campos da versão do produto.</span><span class="sxs-lookup"><span data-stu-id="0fe32-116">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="0fe32-117">Se você incluir um quarto campo em sua versão do produto, o instalador ignorará o quarto campo.</span><span class="sxs-lookup"><span data-stu-id="0fe32-117">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe32-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fe32-118">Requirements</span></span>



| <span data-ttu-id="0fe32-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fe32-119">Requirement</span></span> | <span data-ttu-id="0fe32-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0fe32-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe32-121">Versão</span><span class="sxs-lookup"><span data-stu-id="0fe32-121">Version</span></span><br/> | <span data-ttu-id="0fe32-122">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0fe32-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0fe32-123">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0fe32-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0fe32-124">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0fe32-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0fe32-125">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0fe32-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fe32-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fe32-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe32-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0fe32-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="0fe32-128">Aplicação de patch e atualizações</span><span class="sxs-lookup"><span data-stu-id="0fe32-128">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="0fe32-129">pequena atualização</span><span class="sxs-lookup"><span data-stu-id="0fe32-129">small update</span></span>](small-updates.md)
</dt> </dl>

 

 




