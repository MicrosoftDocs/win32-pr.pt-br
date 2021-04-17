---
description: O instalador define a propriedade PATCH para uma lista de patches que estão sendo aplicados chamando MsiApplyPatch, MsiApplyMultiplePatches ou a opção de linha de comando/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: Propriedade PATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747746"
---
# <a name="patch-property"></a><span data-ttu-id="9f0cb-103">Propriedade PATCH</span><span class="sxs-lookup"><span data-stu-id="9f0cb-103">PATCH property</span></span>

<span data-ttu-id="9f0cb-104">O instalador define a propriedade **patch** para uma lista de patches que estão sendo aplicados chamando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) ou a opção de [linha de comando](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-104">The installer sets the **PATCH** property to a list of patches being applied by calling [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) or the /p [Command Line Option](command-line-options.md).</span></span> <span data-ttu-id="9f0cb-105">Você também pode definir a propriedade **patch** na linha de comando ao instalar um pacote usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou a opção de linha de comando/i.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-105">You can also set the **PATCH** property on the command line while installing a package using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or the /i Command Line Option.</span></span>

<span data-ttu-id="9f0cb-106">O valor da propriedade **patch** é uma lista dos patches que estão sendo instalados.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-106">The value of the **PATCH** property is a list of the patches that are being installed.</span></span> <span data-ttu-id="9f0cb-107">Cada patch na lista é representado pelo caminho completo para o pacote do patch (arquivo. msp). Os caminhos completos na lista são separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-107">Each patch in the list is represented by the full path to the patch's package (.msp file.) The full paths in the list are separated by semicolons.</span></span>

<span data-ttu-id="9f0cb-108">**Windows Installer 2,0:** Não há suporte para vários patches.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-108">**Windows Installer 2.0:** Multiple patches are not supported.</span></span> <span data-ttu-id="9f0cb-109">Windows Installer 3,0 é necessário para aplicar vários patches.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-109">Windows Installer 3.0 is required to apply multiple patches.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f0cb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f0cb-110">Remarks</span></span>

<span data-ttu-id="9f0cb-111">Se você criar um pacote de patch usando [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) você poderá especificar que uma ação ou uma caixa de diálogo seja executada somente quando um patch específico estiver sendo aplicado.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-111">If you create a patch package using [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) you can specify that an action or a dialog box only run when a particular patch is being applied.</span></span> <span data-ttu-id="9f0cb-112">Ao criar o pacote de patch, por exemplo test. msp, você cria uma imagem atualizada do produto e um arquivo de propriedades de criação de patch.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-112">When you create the patch package, for example test.msp, you author an upgraded image of the product and a patch creation properties file.</span></span> <span data-ttu-id="9f0cb-113">Ao criar o arquivo de propriedades de criação de patch, você pode inserir um nome de propriedade, por exemplo, PATCHFORTEST, no campo MediaSrcPropName da tabela [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="9f0cb-113">When authoring the patch creation properties file you can enter a property name, for example PATCHFORTEST, in the MediaSrcPropName field of the [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) table.</span></span> <span data-ttu-id="9f0cb-114">Ao criar as tabelas de sequência da imagem atualizada do produto, você pode incluir na coluna condição da tabela de sequência uma instrução condicional para a ação ou caixa de diálogo que você deseja tornar condicional.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-114">When you author the sequence tables of the upgraded image of the product, you can include in the Condition column of the sequence table a conditional statement for the action or dialog box you want to make conditional.</span></span>

<span data-ttu-id="9f0cb-115">Por exemplo, você pode usar a seguinte instrução condicional para executar uma ação ou caixa de diálogo somente quando Test. msp estiver sendo aplicado.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-115">For example, you can use the following conditional statement to run an action or dialog box only when test.msp is being applied.</span></span>

<dl> <span data-ttu-id="9f0cb-116">PATCH E PATCHFORTEST E PATCH >< PATCHFORTEST</span><span class="sxs-lookup"><span data-stu-id="9f0cb-116">PATCH AND PATCHFORTEST AND PATCH >< PATCHFORTEST</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="9f0cb-117">Como a propriedade **patch** pode conter vários patches, use o operador de subcadeia de caracteres "><" para testar a presença de um patch específico em vez do operador Equals "=".</span><span class="sxs-lookup"><span data-stu-id="9f0cb-117">Because the **PATCH** property can contain multiple patches, use the substring operator "><" to test for the presence of a particular patch rather than the equals operator "=".</span></span> <span data-ttu-id="9f0cb-118">Para obter mais informações sobre instruções condicionais, consulte a seção [sintaxe de instrução condicional](conditional-statement-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="9f0cb-118">For more information about conditional statements see the [Conditional Statement Syntax](conditional-statement-syntax.md) section.</span></span>

 

<span data-ttu-id="9f0cb-119">O instalador definirá as duas propriedades se você aplicar uma lista de patches que inclui o Test. msp.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-119">The installer sets both properties if you apply a list of patches that includes test.msp.</span></span> <span data-ttu-id="9f0cb-120">Por exemplo, você pode usar a [opção de linha de comando](command-line-options.md) /p para aplicar uma lista de dois patches.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-120">For example, you can use the /p [Command Line Option](command-line-options.md) to apply a list of two patches.</span></span>

<span data-ttu-id="9f0cb-121">**msiexec/QB/p \\ \\ temporário \\ \\ \\ patches XYZ \\ Tests. msp; \\ \\ rascunho do rascunho da \\ \\ \\ barra XYZ. msp**</span><span class="sxs-lookup"><span data-stu-id="9f0cb-121">**msiexec /qb /p \\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp**</span></span>

<span data-ttu-id="9f0cb-122">O instalador define as propriedades **patch** e PATCHFORTEST da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-122">The installer sets the **PATCH** and PATCHFORTEST properties as follows.</span></span>

<dl> <span data-ttu-id="9f0cb-123">PATCH = \\ \\ rascunho \\ temporário \\ \\ patches de XYZ \\ Test. msp; \\ \\ rascunho do rascunho da \\ \\ \\ barra XYZ. msp</span><span class="sxs-lookup"><span data-stu-id="9f0cb-123">PATCH=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp</span></span>  
<span data-ttu-id="9f0cb-124">PATCHFORTEST = rascunho \\ \\ \\ temporário \\ \\ patches do XYZ \\ Test. msp</span><span class="sxs-lookup"><span data-stu-id="9f0cb-124">PATCHFORTEST=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp</span></span>  
</dl>

<span data-ttu-id="9f0cb-125">Nesse caso, a condição é verdadeira e a caixa de diálogo ou ação condicional acima pode ser executada para cada patch que está sendo instalado, Test. msp e bar. msp.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-125">In this case, the condition is TRUE and the above conditional action or dialog box can run for each patch being installed, test.msp and bar.msp.</span></span>

<span data-ttu-id="9f0cb-126">Se Test. msp não estiver sendo aplicado, o instalador não o incluirá na propriedade **patch** e não definirá PATCHFORTEST.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-126">If test.msp is not being applied, the installer does not include it in the **PATCH** property and does not set PATCHFORTEST.</span></span> <span data-ttu-id="9f0cb-127">Nesse caso, a condição acima é falsa e a ação condicional ou a caixa de diálogo não é executada.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-127">In this case, the condition above is FALSE and the conditional action or dialog box does not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f0cb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f0cb-128">Requirements</span></span>



| <span data-ttu-id="9f0cb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f0cb-129">Requirement</span></span> | <span data-ttu-id="9f0cb-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0cb-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f0cb-131">Versão</span><span class="sxs-lookup"><span data-stu-id="9f0cb-131">Version</span></span><br/> | <span data-ttu-id="9f0cb-132">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9f0cb-133">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9f0cb-134">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9f0cb-135">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f0cb-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f0cb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f0cb-137">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f0cb-137">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9f0cb-138">Sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="9f0cb-138">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="9f0cb-139">Exemplos de sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="9f0cb-139">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




