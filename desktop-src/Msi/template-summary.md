---
description: Para um pacote de instalação, a propriedade de resumo do modelo indica as versões de plataforma e idioma que são compatíveis com esse banco de dados de instalação.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Propriedade de resumo do modelo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775698"
---
# <a name="template-summary-property"></a><span data-ttu-id="587a7-103">Propriedade de resumo do modelo</span><span class="sxs-lookup"><span data-stu-id="587a7-103">Template Summary property</span></span>

<span data-ttu-id="587a7-104">Para um pacote de instalação, a propriedade de **Resumo do modelo** indica as versões de plataforma e idioma que são compatíveis com esse banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="587a7-104">For an installation package, the **Template Summary** property indicates the platform and language versions that are compatible with this installation database.</span></span> <span data-ttu-id="587a7-105">A sintaxe das informações de propriedade de **Resumo do modelo** para um banco de dados de instalação é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="587a7-105">The syntax of the **Template Summary** property information for an installation database is the following:</span></span>

<span data-ttu-id="587a7-106">\[*propriedade de plataforma* \] ; \[ *ID do idioma* \] \[ ,*ID de idioma* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="587a7-106">\[*platform property*\];\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="587a7-107">Os exemplos a seguir são valores válidos para a propriedade de **Resumo do modelo** :</span><span class="sxs-lookup"><span data-stu-id="587a7-107">The following examples are valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="587a7-108">x64; 1033</span><span class="sxs-lookup"><span data-stu-id="587a7-108">x64;1033</span></span>
-   <span data-ttu-id="587a7-109">Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="587a7-109">Intel;1033</span></span>
-   <span data-ttu-id="587a7-110">Intel64; 1033</span><span class="sxs-lookup"><span data-stu-id="587a7-110">Intel64;1033</span></span>
-   <span data-ttu-id="587a7-111">; 1033</span><span class="sxs-lookup"><span data-stu-id="587a7-111">;1033</span></span>
-   <span data-ttu-id="587a7-112">Intel; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="587a7-112">Intel ;1033,2046</span></span>
-   <span data-ttu-id="587a7-113">Intel64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="587a7-113">Intel64;1033,2046</span></span>
-   <span data-ttu-id="587a7-114">Intel; 0</span><span class="sxs-lookup"><span data-stu-id="587a7-114">Intel;0</span></span>
-   <span data-ttu-id="587a7-115">ARM; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="587a7-115">Arm;1033,2046</span></span>
-   <span data-ttu-id="587a7-116">ARM; 0</span><span class="sxs-lookup"><span data-stu-id="587a7-116">Arm;0</span></span>
-   <span data-ttu-id="587a7-117">Arm64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="587a7-117">Arm64;1033,2046</span></span>
-   <span data-ttu-id="587a7-118">Arm64; 0</span><span class="sxs-lookup"><span data-stu-id="587a7-118">Arm64;0</span></span>

<span data-ttu-id="587a7-119">A propriedade **Summary do modelo** de uma transformação indica as versões de plataforma e idioma compatíveis com a transformação.</span><span class="sxs-lookup"><span data-stu-id="587a7-119">The **Template Summary** property of a transform indicates the platform and language versions compatible with the transform.</span></span> <span data-ttu-id="587a7-120">Em um arquivo de transformação, apenas um idioma pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="587a7-120">In a transform file, only one language may be specified.</span></span> <span data-ttu-id="587a7-121">A plataforma e o idioma especificados determinam se uma transformação pode ser aplicada a um determinado banco de dados.</span><span class="sxs-lookup"><span data-stu-id="587a7-121">The specified platform and language determine whether a transform can be applied to a particular database.</span></span> <span data-ttu-id="587a7-122">A propriedade Platform e a propriedade Language poderão ser deixadas em branco se nenhuma restrição de transformação depender delas para validar a transformação.</span><span class="sxs-lookup"><span data-stu-id="587a7-122">The platform property and the language property can be left blank if no transform restriction relies on them to validate the transform.</span></span>

<span data-ttu-id="587a7-123">A propriedade de **Resumo do modelo** de um pacote de patch é uma lista delimitada por ponto-e-vírgula dos códigos de produto que podem aceitar o patch.</span><span class="sxs-lookup"><span data-stu-id="587a7-123">The **Template Summary** property of a patch package is a semicolon-delimited list of the product codes that can accept the patch.</span></span> <span data-ttu-id="587a7-124">Se você usar [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) para gerar o pacote de patch, essa lista será obtida da [tabela TargetImages](targetimages-table-patchwiz-dll-.md) do arquivo de criação de patch.</span><span class="sxs-lookup"><span data-stu-id="587a7-124">If you use [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate the patch package, this list is obtained from the [TargetImages table](targetimages-table-patchwiz-dll-.md) of the patch creation file.</span></span>

<span data-ttu-id="587a7-125">Essa propriedade de resumo é necessária.</span><span class="sxs-lookup"><span data-stu-id="587a7-125">This summary property is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="587a7-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="587a7-126">Remarks</span></span>

<span data-ttu-id="587a7-127">Se a plataforma atual não corresponder a uma das plataformas especificadas na propriedade de **Resumo do modelo** , o instalador não processará o pacote.</span><span class="sxs-lookup"><span data-stu-id="587a7-127">If the current platform does not match one of the platforms specified in the **Template Summary** property then the installer does not process the package.</span></span>

<span data-ttu-id="587a7-128">Se a especificação da plataforma estiver ausente no valor da propriedade de **Resumo do modelo** , o instalador assumirá a arquitetura Intel.</span><span class="sxs-lookup"><span data-stu-id="587a7-128">If the platform specification is missing in the **Template Summary** property value, the installer assumes the Intel architecture.</span></span>

<span data-ttu-id="587a7-129">Se esse for um pacote de Windows Installer de 64 bits sendo executado em uma plataforma Intel64 (Itanium), digite Intel64 na propriedade **Resumo do modelo** .</span><span class="sxs-lookup"><span data-stu-id="587a7-129">If this is a 64-bit Windows Installer package being run on an Intel64 (Itanium) platform, enter Intel64 in the **Template Summary** property.</span></span>

<span data-ttu-id="587a7-130">Se esse for um pacote de Windows Installer de 64 bits sendo executado em uma plataforma x64, digite x64 na propriedade de **Resumo do modelo** .</span><span class="sxs-lookup"><span data-stu-id="587a7-130">If this is a 64-bit Windows Installer package being run on a x64 platform, enter x64 in the **Template Summary** property.</span></span>

<span data-ttu-id="587a7-131">Se esse for um pacote de Windows Installer de 64 bits sendo executado em uma plataforma Arm64, digite Arm64 na propriedade **Resumo do modelo** .</span><span class="sxs-lookup"><span data-stu-id="587a7-131">If this is a 64-bit Windows Installer package being run on an Arm64 platform, enter Arm64 in the **Template Summary** property.</span></span>

<span data-ttu-id="587a7-132">Um pacote Windows Installer não pode ser marcado como compatível com Intel64 e x64; por exemplo, o valor da propriedade de **Resumo do modelo** de Intel64, x64 é inválido.</span><span class="sxs-lookup"><span data-stu-id="587a7-132">A Windows Installer package cannot be marked as supporting both Intel64 and x64; for example, the **Template Summary** property value of Intel64,x64 is invalid.</span></span>

<span data-ttu-id="587a7-133">Um pacote Windows Installer não pode ser marcado como compatível com plataformas de 32 bits e 64 bits; por exemplo, os valores de propriedade de **Resumo do modelo** , como Intel, x64 ou Intel, Intel64 são inválidos.</span><span class="sxs-lookup"><span data-stu-id="587a7-133">A Windows Installer package cannot be marked as supporting both 32-bit and 64-bit platforms; for example, **Template Summary** property values such as Intel,x64 or Intel,Intel64 are invalid.</span></span>

<span data-ttu-id="587a7-134">Inserir 0 (zero) no campo ID de idioma da propriedade **Resumo do modelo** ou deixar esse campo vazio, indica que o pacote é neutro de idioma.</span><span class="sxs-lookup"><span data-stu-id="587a7-134">Entering 0 (zero) in the language ID field of the **Template Summary** property, or leaving this field empty, indicates that the package is language neutral.</span></span>

<span data-ttu-id="587a7-135">Se esse for um pacote Windows Installer sendo executado no Windows RT, insira o ARM de valor na propriedade de **Resumo do modelo** .</span><span class="sxs-lookup"><span data-stu-id="587a7-135">If this is a Windows Installer package being run on Windows RT, enter the value Arm in the **Template Summary** property.</span></span>

<span data-ttu-id="587a7-136">Os módulos de mesclagem são os únicos pacotes que podem ter vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="587a7-136">Merge Modules are the only packages that may have multiple languages.</span></span> <span data-ttu-id="587a7-137">Somente um idioma pode ser especificado em um banco de dados do instalador de origem.</span><span class="sxs-lookup"><span data-stu-id="587a7-137">Only one language can be specified in a source installer database.</span></span> <span data-ttu-id="587a7-138">Para obter mais informações, consulte [vários módulos de mesclagem de idiomas](multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="587a7-138">For more information, see [Multiple Language Merge Modules](multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="587a7-139">A plataforma Alpha não tem suporte pelo Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="587a7-139">The Alpha platform is not supported by Windows Installer.</span></span>

<span data-ttu-id="587a7-140">**Windows Installer:** Não há suporte para a sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="587a7-140">**Windows Installer:** The following syntax is not supported:</span></span>

<span data-ttu-id="587a7-141">\[*Propriedade* \] \[ de plataforma,*propriedade de plataforma* \] \[ ,... \] \[ *ID do idioma* \] \[ ,*ID de idioma* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="587a7-141">\[*platform property*\]\[,*platform property*\]\[,...\]\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="587a7-142">Os exemplos a seguir não são valores válidos para a propriedade de **Resumo do modelo** :</span><span class="sxs-lookup"><span data-stu-id="587a7-142">The following examples are not valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="587a7-143">Alpha, Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="587a7-143">Alpha,Intel;1033</span></span>
-   <span data-ttu-id="587a7-144">Intel, Alpha; 1033</span><span class="sxs-lookup"><span data-stu-id="587a7-144">Intel,Alpha;1033</span></span>
-   <span data-ttu-id="587a7-145">Alfa; 1033</span><span class="sxs-lookup"><span data-stu-id="587a7-145">Alpha;1033</span></span>
-   <span data-ttu-id="587a7-146">Alpha; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="587a7-146">Alpha;1033,2046</span></span>

## <a name="requirements"></a><span data-ttu-id="587a7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="587a7-147">Requirements</span></span>



| <span data-ttu-id="587a7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="587a7-148">Requirement</span></span> | <span data-ttu-id="587a7-149">Valor</span><span class="sxs-lookup"><span data-stu-id="587a7-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="587a7-150">Versão</span><span class="sxs-lookup"><span data-stu-id="587a7-150">Version</span></span><br/> | <span data-ttu-id="587a7-151">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="587a7-151">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="587a7-152">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="587a7-152">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="587a7-153">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="587a7-153">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="587a7-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="587a7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587a7-155">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="587a7-155">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




