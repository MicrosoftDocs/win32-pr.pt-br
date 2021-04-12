---
title: Recurso VERSIONINFO
description: Define um recurso de informações de versão. O recurso contém informações sobre o arquivo como seu número de versão, seu sistema operacional pretendido e seu nome de arquivo original. O recurso destina-se a ser usado com as funções de informações de versão.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menus de recursos do VERSIONINFO e outros recursos
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "104294587"
---
# <a name="versioninfo-resource"></a><span data-ttu-id="d2a7a-106">Recurso VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="d2a7a-106">VERSIONINFO resource</span></span>

<span data-ttu-id="d2a7a-107">Define um recurso de informações de versão.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-107">Defines a version-information resource.</span></span> <span data-ttu-id="d2a7a-108">O recurso contém informações sobre o arquivo como seu número de versão, seu sistema operacional pretendido e seu nome de arquivo original.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-108">The resource contains such information about the file as its version number, its intended operating system, and its original filename.</span></span> <span data-ttu-id="d2a7a-109">O recurso destina-se a ser usado com as funções de [informações de versão](./version-information.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a7a-109">The resource is intended to be used with the [Version Information](./version-information.md) functions.</span></span>

<span data-ttu-id="d2a7a-110">Há duas maneiras de Formatar uma instrução **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="d2a7a-110">There are two ways to format a **VERSIONINFO** statement:</span></span>

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

<span data-ttu-id="d2a7a-111">\- ou –</span><span class="sxs-lookup"><span data-stu-id="d2a7a-111">\- or -</span></span>

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="d2a7a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2a7a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a7a-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-114">Versão – identificador de recurso de informações.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-114">Version-information resource identifier.</span></span> <span data-ttu-id="d2a7a-115">Esse valor deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="d2a7a-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*informações fixas*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-117">Informações de versão, como a versão do arquivo e o sistema operacional pretendido.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-117">Version information, such as the file version and the intended operating system.</span></span> <span data-ttu-id="d2a7a-118">Esse parâmetro consiste nas instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-118">This parameter consists of the following statements.</span></span>



| <span data-ttu-id="d2a7a-119">Instrução</span><span class="sxs-lookup"><span data-stu-id="d2a7a-119">Statement</span></span>                         | <span data-ttu-id="d2a7a-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a7a-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a7a-121"> *Versão* da versão</span><span class="sxs-lookup"><span data-stu-id="d2a7a-121">**FILEVERSION** *version*</span></span>         | <span data-ttu-id="d2a7a-122">Número de versão binária do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-122">Binary version number for the file.</span></span> <span data-ttu-id="d2a7a-123">A *versão* consiste em inteiros de 2 32 bits, definidos por inteiros de 4 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-123">The *version* consists of two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="d2a7a-124">Por exemplo, "FileVersion 3, 10, 0, 61" é traduzido em dois doublewords: 0x0003000a e 0x0000003d, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-124">For example, "FILEVERSION 3,10,0,61" is translated into two doublewords: 0x0003000a and 0x0000003d, in that order.</span></span> <span data-ttu-id="d2a7a-125">Portanto, se a *versão* for definida pelos valores **DWORD** *dw1* e *DW2*, eles precisarão aparecer na instrução **FileVersion** da seguinte maneira: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` .</span><span class="sxs-lookup"><span data-stu-id="d2a7a-125">Therefore, if *version* is defined by the **DWORD** values *dw1* and *dw2*, they need to appear in the **FILEVERSION** statement as follows: `HIWORD(dw1)`, `LOWORD(dw1)`, `HIWORD(dw2)`, `LOWORD(dw2)`.</span></span> |
| <span data-ttu-id="d2a7a-126"> *Versão* do PRODUCTVERSION</span><span class="sxs-lookup"><span data-stu-id="d2a7a-126">**PRODUCTVERSION** *version*</span></span>      | <span data-ttu-id="d2a7a-127">Número de versão binária do produto com o qual o arquivo é distribuído.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-127">Binary version number for the product with which the file is distributed.</span></span> <span data-ttu-id="d2a7a-128">O parâmetro *version* é um número inteiro de 2 32 bits, definido por inteiros de 4 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-128">The *version* parameter is two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="d2a7a-129">Para obter mais informações sobre a *versão*, consulte a descrição de **FileVersion** .</span><span class="sxs-lookup"><span data-stu-id="d2a7a-129">For more information about *version*, see the **FILEVERSION** description.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="d2a7a-130">**FILEFLAGSMASK** *FILEFLAGSMASK*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-130">**FILEFLAGSMASK** *fileflagsmask*</span></span> | <span data-ttu-id="d2a7a-131">Indica quais bits na instrução **FILEFLAGS** são válidos.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-131">Indicates which bits in the **FILEFLAGS** statement are valid.</span></span> <span data-ttu-id="d2a7a-132">Para o Windows de 16 bits, esse valor é 0x3F.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-132">For 16-bit Windows, this value is 0x3f.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d2a7a-133">*Sinalizadors* de **FILEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-133">**FILEFLAGS** *fileflags*</span></span>         | <span data-ttu-id="d2a7a-134">Atributos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-134">Attributes of the file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d2a7a-135">**FILEOS** *FILEOS*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-135">**FILEOS** *fileos*</span></span>               | <span data-ttu-id="d2a7a-136">Sistema operacional para o qual este arquivo foi projetado.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-136">Operating system for which this file was designed.</span></span> <span data-ttu-id="d2a7a-137">O parâmetro *fileos* pode ser um dos valores do sistema operacional fornecidos na seção comentários.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-137">The *fileos* parameter can be one of the operating system values given in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d2a7a-138"> *Filetype* de filetype</span><span class="sxs-lookup"><span data-stu-id="d2a7a-138">**FILETYPE** *filetype*</span></span>           | <span data-ttu-id="d2a7a-139">Tipo geral de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-139">General type of file.</span></span> <span data-ttu-id="d2a7a-140">O parâmetro *filetype* pode ser um dos valores de tipo de arquivo listados na seção comentários.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-140">The *filetype* parameter can be one of the file type values listed in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d2a7a-141">Subtipo **FILESUBTYPE** </span><span class="sxs-lookup"><span data-stu-id="d2a7a-141">**FILESUBTYPE** *subtype*</span></span>         | <span data-ttu-id="d2a7a-142">Função do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-142">Function of the file.</span></span> <span data-ttu-id="d2a7a-143">O parâmetro de *subtipo* é zero, a menos que o parâmetro *filetype* na instrução **FILETYPE** seja VFT \_ DRV, VFT \_ Font ou VFT \_ VXD.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-143">The *subtype* parameter is zero unless the *filetype* parameter in the **FILETYPE** statement is VFT\_DRV, VFT\_FONT, or VFT\_VXD.</span></span> <span data-ttu-id="d2a7a-144">Para obter uma lista de valores de subtipo de arquivo, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-144">For a list of file subtype values, see the Remarks section.</span></span>                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="d2a7a-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*instrução Block*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-146">Especifica um ou mais blocos de informações de versão.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-146">Specifies one or more version-information blocks.</span></span> <span data-ttu-id="d2a7a-147">Um bloco pode conter informações de cadeia de caracteres ou informações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-147">A block can contain string information or variable information.</span></span> <span data-ttu-id="d2a7a-148">Para obter mais informações, consulte bloco [**StringFileInfo**](stringfileinfo-block.md) ou [**bloco VarFileInfo**](varfileinfo-block.md).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-148">For more information, see [**StringFileInfo Block**](stringfileinfo-block.md) or [**VarFileInfo Block**](varfileinfo-block.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2a7a-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2a7a-149">Remarks</span></span>

<span data-ttu-id="d2a7a-150">Para usar as constantes especificadas com a instrução **VERSIONINFO** , você deve incluir o arquivo de cabeçalho winver. h ou Windows. h no arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-150">To use the constants specified with the **VERSIONINFO** statement, you must include the Winver.h or Windows.h header file in the resource-definition file.</span></span>

<span data-ttu-id="d2a7a-151">A lista a seguir descreve os parâmetros usados na instrução **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="d2a7a-151">The following list describes the parameters used in the **VERSIONINFO** statement:</span></span>

<dl> <dt>

<span data-ttu-id="d2a7a-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*sinalizadores de*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-153">Uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-153">A combination of the following values.</span></span>



| <span data-ttu-id="d2a7a-154">Valor</span><span class="sxs-lookup"><span data-stu-id="d2a7a-154">Value</span></span>                      | <span data-ttu-id="d2a7a-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a7a-155">Description</span></span>                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a7a-156">**depuração do VS \_ FF \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-156">**VS\_FF\_DEBUG**</span></span>          | <span data-ttu-id="d2a7a-157">O arquivo contém informações de depuração ou é compilado com recursos de depuração habilitados.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-157">File contains debugging information or is compiled with debugging features enabled.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="d2a7a-158">**com \_ patch do vs FF \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-158">**VS\_FF\_PATCHED**</span></span>        | <span data-ttu-id="d2a7a-159">O arquivo foi modificado e não é idêntico ao arquivo de envio original do mesmo número de versão.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-159">File has been modified and is not identical to the original shipping file of the same version number.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="d2a7a-160">**PRÉ-lançamento do VS \_ FF \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-160">**VS\_FF\_PRERELEASE**</span></span>     | <span data-ttu-id="d2a7a-161">O arquivo é uma versão de desenvolvimento, não um produto lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-161">File is a development version, not a commercially released product.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="d2a7a-162">**PRIVATEBUILD do VS \_ FF \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-162">**VS\_FF\_PRIVATEBUILD**</span></span>   | <span data-ttu-id="d2a7a-163">O arquivo não foi compilado usando procedimentos de versão padrão.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-163">File was not built using standard release procedures.</span></span> <span data-ttu-id="d2a7a-164">Se esse valor for fornecido, o [**bloco StringFileInfo**](stringfileinfo-block.md) deverá conter uma cadeia de caracteres **PrivateBuild** .</span><span class="sxs-lookup"><span data-stu-id="d2a7a-164">If this value is given, the [**StringFileInfo block**](stringfileinfo-block.md) must contain a **PrivateBuild** string.</span></span>                                                                                              |
| <span data-ttu-id="d2a7a-165">**SPECIALBUILD do VS \_ FF \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-165">**VS\_FF\_SPECIALBUILD**</span></span>   | <span data-ttu-id="d2a7a-166">O arquivo foi criado pela empresa original usando procedimentos de versão padrão, mas é uma variação do arquivo padrão do mesmo número de versão.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-166">File was built by the original company using standard release procedures but is a variation of the standard file of the same version number.</span></span> <span data-ttu-id="d2a7a-167">Se esse valor for fornecido, o bloco de [bloco **StringFileInfo**](stringfileinfo-block.md) deverá conter uma cadeia de caracteres **SpecialBuild** .</span><span class="sxs-lookup"><span data-stu-id="d2a7a-167">If this value is given, the [**StringFileInfo** block](stringfileinfo-block.md) block must contain a **SpecialBuild** string.</span></span> |
| <span data-ttu-id="d2a7a-168">**VS \_ FFI \_ FILEFLAGSMASK**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-168">**VS\_FFI\_FILEFLAGSMASK**</span></span> | <span data-ttu-id="d2a7a-169">Uma combinação de todos os valores anteriores.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-169">A combination of all the preceding values.</span></span>                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="d2a7a-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-171">Um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-171">One of the following values.</span></span>



| <span data-ttu-id="d2a7a-172">Valor</span><span class="sxs-lookup"><span data-stu-id="d2a7a-172">Value</span></span>                   | <span data-ttu-id="d2a7a-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a7a-173">Description</span></span>                                                      |
|-------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d2a7a-174">**VOS \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-174">**VOS\_UNKNOWN**</span></span>        | <span data-ttu-id="d2a7a-175">O sistema operacional para o qual o arquivo foi projetado é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-175">The operating system for which the file was designed is unknown.</span></span> |
| <span data-ttu-id="d2a7a-176">**VOS \_ dos**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-176">**VOS\_DOS**</span></span>            | <span data-ttu-id="d2a7a-177">O arquivo foi projetado para o MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-177">File was designed for MS-DOS.</span></span>                                    |
| <span data-ttu-id="d2a7a-178">**VOS \_ NT**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-178">**VOS\_NT**</span></span>             | <span data-ttu-id="d2a7a-179">O arquivo foi projetado para o Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-179">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="d2a7a-180">**VOS \_ \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-180">**VOS\_\_WINDOWS16**</span></span>    | <span data-ttu-id="d2a7a-181">O arquivo foi projetado para o Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-181">File was designed for 16-bit Windows.</span></span>                            |
| <span data-ttu-id="d2a7a-182">**VOS \_ \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-182">**VOS\_\_WINDOWS32**</span></span>    | <span data-ttu-id="d2a7a-183">O arquivo foi projetado para o Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-183">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="d2a7a-184">**VOS \_ dos \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-184">**VOS\_DOS\_WINDOWS16**</span></span> | <span data-ttu-id="d2a7a-185">O arquivo foi projetado para o Windows de 16 bits em execução com o MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-185">File was designed for 16-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="d2a7a-186">**VOS \_ dos \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-186">**VOS\_DOS\_WINDOWS32**</span></span> | <span data-ttu-id="d2a7a-187">O arquivo foi projetado para o Windows de 32 bits em execução com o MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-187">File was designed for 32-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="d2a7a-188">**VOS \_ NT \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-188">**VOS\_NT\_WINDOWS32**</span></span>  | <span data-ttu-id="d2a7a-189">O arquivo foi projetado para o Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-189">File was designed for 32-bit Windows.</span></span>                            |



 

<span data-ttu-id="d2a7a-190">Os valores 0x00002L, 0x00003L, 0x20000L e 0x30000L são reservados.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-190">The values 0x00002L, 0x00003L, 0x20000L and 0x30000L are reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d2a7a-191"><span id="filetype"></span><span id="FILETYPE"></span>*Talvez*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-192">Um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-192">One of the following values.</span></span>



| <span data-ttu-id="d2a7a-193">Valor</span><span class="sxs-lookup"><span data-stu-id="d2a7a-193">Value</span></span>                | <span data-ttu-id="d2a7a-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a7a-194">Description</span></span>                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a7a-195">**VFT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-195">**VFT\_UNKNOWN**</span></span>     | <span data-ttu-id="d2a7a-196">O tipo de arquivo é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-196">File type is unknown.</span></span>                                                                                                       |
| <span data-ttu-id="d2a7a-197">**\_aplicativo VFT**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-197">**VFT\_APP**</span></span>         | <span data-ttu-id="d2a7a-198">O arquivo contém um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-198">File contains an application.</span></span>                                                                                               |
| <span data-ttu-id="d2a7a-199">**\_dll VFT**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-199">**VFT\_DLL**</span></span>         | <span data-ttu-id="d2a7a-200">O arquivo contém uma DLL (biblioteca de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-200">File contains a dynamic-link library (DLL).</span></span>                                                                                 |
| <span data-ttu-id="d2a7a-201">**VFT \_ drv**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-201">**VFT\_DRV**</span></span>         | <span data-ttu-id="d2a7a-202">O arquivo contém um driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-202">File contains a device driver.</span></span> <span data-ttu-id="d2a7a-203">Se o *filetype* for **VFT \_ drv**, o *subtipo* conterá uma descrição mais específica do driver.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-203">If *filetype* is **VFT\_DRV**, *subtype* contains a more specific description of the driver.</span></span> |
| <span data-ttu-id="d2a7a-204">**\_fonte VFT**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-204">**VFT\_FONT**</span></span>        | <span data-ttu-id="d2a7a-205">O arquivo contém uma fonte.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-205">File contains a font.</span></span> <span data-ttu-id="d2a7a-206">Se *filetype* for VFT \_ fonte, *subtipo* conterá uma descrição mais específica da fonte.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-206">If *filetype* is VFT\_FONT, *subtype* contains a more specific description of the font.</span></span>               |
| <span data-ttu-id="d2a7a-207">**VFT \_ vxd**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-207">**VFT\_VXD**</span></span>         | <span data-ttu-id="d2a7a-208">O arquivo contém um dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-208">File contains a virtual device.</span></span>                                                                                             |
| <span data-ttu-id="d2a7a-209">**\_lib VFT static \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-209">**VFT\_STATIC\_LIB**</span></span> | <span data-ttu-id="d2a7a-210">O arquivo contém uma biblioteca de vínculo estático.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-210">File contains a static-link library.</span></span>                                                                                        |



 

<span data-ttu-id="d2a7a-211">Todos os outros valores são reservados para uso pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-211">All other values are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="d2a7a-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtipo*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtype*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-213">Informações adicionais sobre o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-213">Additional information about the file type.</span></span>

<span data-ttu-id="d2a7a-214">Se *filetype* especificar **VFT \_ drv**, esse parâmetro poderá ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-214">If *filetype* specifies **VFT\_DRV**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="d2a7a-215">Valor</span><span class="sxs-lookup"><span data-stu-id="d2a7a-215">Value</span></span>                             | <span data-ttu-id="d2a7a-216">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a7a-216">Description</span></span>                               |
|-----------------------------------|-------------------------------------------|
| <span data-ttu-id="d2a7a-217">**VFT2 \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-217">**VFT2\_UNKNOWN**</span></span>                 | <span data-ttu-id="d2a7a-218">O tipo de driver é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-218">Driver type is unknown.</span></span>                   |
| <span data-ttu-id="d2a7a-219">**\_Comm VFT2 drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-219">**VFT2\_DRV\_COMM**</span></span>               | <span data-ttu-id="d2a7a-220">O arquivo contém um driver de comunicação.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-220">File contains a communications driver.</span></span>    |
| <span data-ttu-id="d2a7a-221">**\_Impressora VFT2 drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-221">**VFT2\_DRV\_PRINTER**</span></span>            | <span data-ttu-id="d2a7a-222">O arquivo contém um driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-222">File contains a printer driver.</span></span>           |
| <span data-ttu-id="d2a7a-223">**\_Teclado VFT2 drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-223">**VFT2\_DRV\_KEYBOARD**</span></span>           | <span data-ttu-id="d2a7a-224">O arquivo contém um driver de teclado.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-224">File contains a keyboard driver.</span></span>          |
| <span data-ttu-id="d2a7a-225">**\_Linguagem VFT2 drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-225">**VFT2\_DRV\_LANGUAGE**</span></span>           | <span data-ttu-id="d2a7a-226">O arquivo contém um driver de idioma.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-226">File contains a language driver.</span></span>          |
| <span data-ttu-id="d2a7a-227">**Exibição de VFT2 \_ drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-227">**VFT2\_DRV\_DISPLAY**</span></span>            | <span data-ttu-id="d2a7a-228">O arquivo contém um driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-228">File contains a display driver.</span></span>           |
| <span data-ttu-id="d2a7a-229">**\_Mouse VFT2 drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-229">**VFT2\_DRV\_MOUSE**</span></span>              | <span data-ttu-id="d2a7a-230">O arquivo contém um driver de mouse.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-230">File contains a mouse driver.</span></span>             |
| <span data-ttu-id="d2a7a-231">**\_Rede VFT2 drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-231">**VFT2\_DRV\_NETWORK**</span></span>            | <span data-ttu-id="d2a7a-232">O arquivo contém um driver de rede.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-232">File contains a network driver.</span></span>           |
| <span data-ttu-id="d2a7a-233">**\_Sistema VFT2 drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-233">**VFT2\_DRV\_SYSTEM**</span></span>             | <span data-ttu-id="d2a7a-234">O arquivo contém um driver de sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-234">File contains a system driver.</span></span>            |
| <span data-ttu-id="d2a7a-235">**VFT2 \_ drv \_ instalável**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-235">**VFT2\_DRV\_INSTALLABLE**</span></span>        | <span data-ttu-id="d2a7a-236">O arquivo contém um driver instalável.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-236">File contains an installable driver.</span></span>      |
| <span data-ttu-id="d2a7a-237">**\_Som VFT2 drv \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-237">**VFT2\_DRV\_SOUND**</span></span>              | <span data-ttu-id="d2a7a-238">O arquivo contém um driver de som.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-238">File contains a sound driver.</span></span>             |
| <span data-ttu-id="d2a7a-239">**\_Impressora com \_ versão VFT2 \_ drv**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-239">**VFT2\_DRV\_VERSIONED\_PRINTER**</span></span> | <span data-ttu-id="d2a7a-240">O arquivo contém um driver de impressora com versão.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-240">File contains a versioned printer driver.</span></span> |



 

<span data-ttu-id="d2a7a-241">Se *filetype* especificar **a \_ fonte VFT**, esse parâmetro poderá ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-241">If *filetype* specifies **VFT\_FONT**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="d2a7a-242">Valor</span><span class="sxs-lookup"><span data-stu-id="d2a7a-242">Value</span></span>                    | <span data-ttu-id="d2a7a-243">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a7a-243">Description</span></span>                    |
|--------------------------|--------------------------------|
| <span data-ttu-id="d2a7a-244">**VFT2 \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-244">**VFT2\_UNKNOWN**</span></span>        | <span data-ttu-id="d2a7a-245">O tipo de fonte é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-245">Font type is unknown.</span></span>          |
| <span data-ttu-id="d2a7a-246">**\_Rasterização de fonte VFT2 \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-246">**VFT2\_FONT\_RASTER**</span></span>   | <span data-ttu-id="d2a7a-247">O arquivo contém uma fonte de varredura.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-247">File contains a raster font.</span></span>   |
| <span data-ttu-id="d2a7a-248">**\_Vetor de fonte VFT2 \_**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-248">**VFT2\_FONT\_VECTOR**</span></span>   | <span data-ttu-id="d2a7a-249">O arquivo contém uma fonte de vetor.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-249">File contains a vector font.</span></span>   |
| <span data-ttu-id="d2a7a-250">**Fonte de VFT2 \_ \_ TrueType**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-250">**VFT2\_FONT\_TRUETYPE**</span></span> | <span data-ttu-id="d2a7a-251">O arquivo contém uma fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-251">File contains a TrueType font.</span></span> |



 

<span data-ttu-id="d2a7a-252">Se *filetype* especificar VFT \_ vxd, esse parâmetro deverá ser o identificador de dispositivo virtual incluído no bloco de controle de dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-252">If *filetype* specifies VFT\_VXD, this parameter must be the virtual-device identifier included in the virtual-device control block.</span></span>

<span data-ttu-id="d2a7a-253">Todos os valores de *subtipo* não listados aqui são reservados para uso pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-253">All *subtype* values not listed here are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="d2a7a-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-255">Um dos códigos de idioma a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-255">One of the following language codes.</span></span>



| <span data-ttu-id="d2a7a-256">Código</span><span class="sxs-lookup"><span data-stu-id="d2a7a-256">Code</span></span>   | <span data-ttu-id="d2a7a-257">Idioma</span><span class="sxs-lookup"><span data-stu-id="d2a7a-257">Language</span></span>            | <span data-ttu-id="d2a7a-258">Código</span><span class="sxs-lookup"><span data-stu-id="d2a7a-258">Code</span></span>   | <span data-ttu-id="d2a7a-259">Idioma</span><span class="sxs-lookup"><span data-stu-id="d2a7a-259">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="d2a7a-260">0x0401</span><span class="sxs-lookup"><span data-stu-id="d2a7a-260">0x0401</span></span> | <span data-ttu-id="d2a7a-261">Árabe</span><span class="sxs-lookup"><span data-stu-id="d2a7a-261">Arabic</span></span>              | <span data-ttu-id="d2a7a-262">0x0415</span><span class="sxs-lookup"><span data-stu-id="d2a7a-262">0x0415</span></span> | <span data-ttu-id="d2a7a-263">Polonês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-263">Polish</span></span>                    |
| <span data-ttu-id="d2a7a-264">0x0402</span><span class="sxs-lookup"><span data-stu-id="d2a7a-264">0x0402</span></span> | <span data-ttu-id="d2a7a-265">Búlgaro</span><span class="sxs-lookup"><span data-stu-id="d2a7a-265">Bulgarian</span></span>           | <span data-ttu-id="d2a7a-266">0x0416</span><span class="sxs-lookup"><span data-stu-id="d2a7a-266">0x0416</span></span> | <span data-ttu-id="d2a7a-267">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-267">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="d2a7a-268">0x0403</span><span class="sxs-lookup"><span data-stu-id="d2a7a-268">0x0403</span></span> | <span data-ttu-id="d2a7a-269">Catalão</span><span class="sxs-lookup"><span data-stu-id="d2a7a-269">Catalan</span></span>             | <span data-ttu-id="d2a7a-270">0x0417</span><span class="sxs-lookup"><span data-stu-id="d2a7a-270">0x0417</span></span> | <span data-ttu-id="d2a7a-271">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="d2a7a-271">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="d2a7a-272">0x0404</span><span class="sxs-lookup"><span data-stu-id="d2a7a-272">0x0404</span></span> | <span data-ttu-id="d2a7a-273">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="d2a7a-273">Traditional Chinese</span></span> | <span data-ttu-id="d2a7a-274">0x0418</span><span class="sxs-lookup"><span data-stu-id="d2a7a-274">0x0418</span></span> | <span data-ttu-id="d2a7a-275">Romeno</span><span class="sxs-lookup"><span data-stu-id="d2a7a-275">Romanian</span></span>                  |
| <span data-ttu-id="d2a7a-276">0x0405</span><span class="sxs-lookup"><span data-stu-id="d2a7a-276">0x0405</span></span> | <span data-ttu-id="d2a7a-277">Tcheco</span><span class="sxs-lookup"><span data-stu-id="d2a7a-277">Czech</span></span>               | <span data-ttu-id="d2a7a-278">0x0419</span><span class="sxs-lookup"><span data-stu-id="d2a7a-278">0x0419</span></span> | <span data-ttu-id="d2a7a-279">Russo</span><span class="sxs-lookup"><span data-stu-id="d2a7a-279">Russian</span></span>                   |
| <span data-ttu-id="d2a7a-280">0x0406</span><span class="sxs-lookup"><span data-stu-id="d2a7a-280">0x0406</span></span> | <span data-ttu-id="d2a7a-281">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-281">Danish</span></span>              | <span data-ttu-id="d2a7a-282">0x041A</span><span class="sxs-lookup"><span data-stu-id="d2a7a-282">0x041A</span></span> | <span data-ttu-id="d2a7a-283">Croato-Serbian (latino)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-283">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="d2a7a-284">0x0407</span><span class="sxs-lookup"><span data-stu-id="d2a7a-284">0x0407</span></span> | <span data-ttu-id="d2a7a-285">Alemão</span><span class="sxs-lookup"><span data-stu-id="d2a7a-285">German</span></span>              | <span data-ttu-id="d2a7a-286">0x041B</span><span class="sxs-lookup"><span data-stu-id="d2a7a-286">0x041B</span></span> | <span data-ttu-id="d2a7a-287">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="d2a7a-287">Slovak</span></span>                    |
| <span data-ttu-id="d2a7a-288">0x0408</span><span class="sxs-lookup"><span data-stu-id="d2a7a-288">0x0408</span></span> | <span data-ttu-id="d2a7a-289">Grego</span><span class="sxs-lookup"><span data-stu-id="d2a7a-289">Greek</span></span>               | <span data-ttu-id="d2a7a-290">0x041C</span><span class="sxs-lookup"><span data-stu-id="d2a7a-290">0x041C</span></span> | <span data-ttu-id="d2a7a-291">Albanês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-291">Albanian</span></span>                  |
| <span data-ttu-id="d2a7a-292">0x0409</span><span class="sxs-lookup"><span data-stu-id="d2a7a-292">0x0409</span></span> | <span data-ttu-id="d2a7a-293">Inglês americano</span><span class="sxs-lookup"><span data-stu-id="d2a7a-293">U.S. English</span></span>        | <span data-ttu-id="d2a7a-294">0x041D</span><span class="sxs-lookup"><span data-stu-id="d2a7a-294">0x041D</span></span> | <span data-ttu-id="d2a7a-295">Sueco</span><span class="sxs-lookup"><span data-stu-id="d2a7a-295">Swedish</span></span>                   |
| <span data-ttu-id="d2a7a-296">0x040A</span><span class="sxs-lookup"><span data-stu-id="d2a7a-296">0x040A</span></span> | <span data-ttu-id="d2a7a-297">Castelhano espanhol</span><span class="sxs-lookup"><span data-stu-id="d2a7a-297">Castilian Spanish</span></span>   | <span data-ttu-id="d2a7a-298">0x041E</span><span class="sxs-lookup"><span data-stu-id="d2a7a-298">0x041E</span></span> | <span data-ttu-id="d2a7a-299">Tailandês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-299">Thai</span></span>                      |
| <span data-ttu-id="d2a7a-300">0x040B</span><span class="sxs-lookup"><span data-stu-id="d2a7a-300">0x040B</span></span> | <span data-ttu-id="d2a7a-301">Finlandês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-301">Finnish</span></span>             | <span data-ttu-id="d2a7a-302">0x041F</span><span class="sxs-lookup"><span data-stu-id="d2a7a-302">0x041F</span></span> | <span data-ttu-id="d2a7a-303">Turco</span><span class="sxs-lookup"><span data-stu-id="d2a7a-303">Turkish</span></span>                   |
| <span data-ttu-id="d2a7a-304">0x040C</span><span class="sxs-lookup"><span data-stu-id="d2a7a-304">0x040C</span></span> | <span data-ttu-id="d2a7a-305">Francês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-305">French</span></span>              | <span data-ttu-id="d2a7a-306">0x0420</span><span class="sxs-lookup"><span data-stu-id="d2a7a-306">0x0420</span></span> | <span data-ttu-id="d2a7a-307">Urdu</span><span class="sxs-lookup"><span data-stu-id="d2a7a-307">Urdu</span></span>                      |
| <span data-ttu-id="d2a7a-308">0x040D</span><span class="sxs-lookup"><span data-stu-id="d2a7a-308">0x040D</span></span> | <span data-ttu-id="d2a7a-309">Hebraico</span><span class="sxs-lookup"><span data-stu-id="d2a7a-309">Hebrew</span></span>              | <span data-ttu-id="d2a7a-310">0x0421</span><span class="sxs-lookup"><span data-stu-id="d2a7a-310">0x0421</span></span> | <span data-ttu-id="d2a7a-311">Bahasa</span><span class="sxs-lookup"><span data-stu-id="d2a7a-311">Bahasa</span></span>                    |
| <span data-ttu-id="d2a7a-312">0x040E</span><span class="sxs-lookup"><span data-stu-id="d2a7a-312">0x040E</span></span> | <span data-ttu-id="d2a7a-313">Húngaro</span><span class="sxs-lookup"><span data-stu-id="d2a7a-313">Hungarian</span></span>           | <span data-ttu-id="d2a7a-314">0x0804</span><span class="sxs-lookup"><span data-stu-id="d2a7a-314">0x0804</span></span> | <span data-ttu-id="d2a7a-315">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="d2a7a-315">Simplified Chinese</span></span>        |
| <span data-ttu-id="d2a7a-316">0x040F</span><span class="sxs-lookup"><span data-stu-id="d2a7a-316">0x040F</span></span> | <span data-ttu-id="d2a7a-317">Islandês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-317">Icelandic</span></span>           | <span data-ttu-id="d2a7a-318">0x0807</span><span class="sxs-lookup"><span data-stu-id="d2a7a-318">0x0807</span></span> | <span data-ttu-id="d2a7a-319">Alemão suíço</span><span class="sxs-lookup"><span data-stu-id="d2a7a-319">Swiss German</span></span>              |
| <span data-ttu-id="d2a7a-320">0x0410</span><span class="sxs-lookup"><span data-stu-id="d2a7a-320">0x0410</span></span> | <span data-ttu-id="d2a7a-321">Italiano</span><span class="sxs-lookup"><span data-stu-id="d2a7a-321">Italian</span></span>             | <span data-ttu-id="d2a7a-322">0x0809</span><span class="sxs-lookup"><span data-stu-id="d2a7a-322">0x0809</span></span> | <span data-ttu-id="d2a7a-323">Inglaterra</span><span class="sxs-lookup"><span data-stu-id="d2a7a-323">U.K.</span></span> <span data-ttu-id="d2a7a-324">Inglês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-324">English</span></span>              |
| <span data-ttu-id="d2a7a-325">0x0411</span><span class="sxs-lookup"><span data-stu-id="d2a7a-325">0x0411</span></span> | <span data-ttu-id="d2a7a-326">Japonês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-326">Japanese</span></span>            | <span data-ttu-id="d2a7a-327">0x080A</span><span class="sxs-lookup"><span data-stu-id="d2a7a-327">0x080A</span></span> | <span data-ttu-id="d2a7a-328">Espanhol (México)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-328">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="d2a7a-329">0x0412</span><span class="sxs-lookup"><span data-stu-id="d2a7a-329">0x0412</span></span> | <span data-ttu-id="d2a7a-330">Coreano</span><span class="sxs-lookup"><span data-stu-id="d2a7a-330">Korean</span></span>              | <span data-ttu-id="d2a7a-331">0x080C</span><span class="sxs-lookup"><span data-stu-id="d2a7a-331">0x080C</span></span> | <span data-ttu-id="d2a7a-332">Francês belga</span><span class="sxs-lookup"><span data-stu-id="d2a7a-332">Belgian French</span></span>            |
| <span data-ttu-id="d2a7a-333">0x0413</span><span class="sxs-lookup"><span data-stu-id="d2a7a-333">0x0413</span></span> | <span data-ttu-id="d2a7a-334">Holandês</span><span class="sxs-lookup"><span data-stu-id="d2a7a-334">Dutch</span></span>               | <span data-ttu-id="d2a7a-335">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="d2a7a-335">0x0C0C</span></span> | <span data-ttu-id="d2a7a-336">Francês do Canadá</span><span class="sxs-lookup"><span data-stu-id="d2a7a-336">Canadian French</span></span>           |
| <span data-ttu-id="d2a7a-337">0x0414</span><span class="sxs-lookup"><span data-stu-id="d2a7a-337">0x0414</span></span> | <span data-ttu-id="d2a7a-338">Norueguês?</span><span class="sxs-lookup"><span data-stu-id="d2a7a-338">Norwegian ?</span></span> <span data-ttu-id="d2a7a-339">Bokmal</span><span class="sxs-lookup"><span data-stu-id="d2a7a-339">Bokmal</span></span>  | <span data-ttu-id="d2a7a-340">0x100C</span><span class="sxs-lookup"><span data-stu-id="d2a7a-340">0x100C</span></span> | <span data-ttu-id="d2a7a-341">Francês suíço</span><span class="sxs-lookup"><span data-stu-id="d2a7a-341">Swiss French</span></span>              |
| <span data-ttu-id="d2a7a-342">0x0810</span><span class="sxs-lookup"><span data-stu-id="d2a7a-342">0x0810</span></span> | <span data-ttu-id="d2a7a-343">Italiano suíço</span><span class="sxs-lookup"><span data-stu-id="d2a7a-343">Swiss Italian</span></span>       | <span data-ttu-id="d2a7a-344">0x0816</span><span class="sxs-lookup"><span data-stu-id="d2a7a-344">0x0816</span></span> | <span data-ttu-id="d2a7a-345">Português (Portugal)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-345">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="d2a7a-346">0x0813</span><span class="sxs-lookup"><span data-stu-id="d2a7a-346">0x0813</span></span> | <span data-ttu-id="d2a7a-347">Holandês belga</span><span class="sxs-lookup"><span data-stu-id="d2a7a-347">Belgian Dutch</span></span>       | <span data-ttu-id="d2a7a-348">0x081A</span><span class="sxs-lookup"><span data-stu-id="d2a7a-348">0x081A</span></span> | <span data-ttu-id="d2a7a-349">Serbo-Croatian (cirílico)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-349">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="d2a7a-350">0x0814</span><span class="sxs-lookup"><span data-stu-id="d2a7a-350">0x0814</span></span> | <span data-ttu-id="d2a7a-351">Norueguês?</span><span class="sxs-lookup"><span data-stu-id="d2a7a-351">Norwegian ?</span></span> <span data-ttu-id="d2a7a-352">Nynorsk</span><span class="sxs-lookup"><span data-stu-id="d2a7a-352">Nynorsk</span></span> |        |                           |



 

</dd> <dt>

<span data-ttu-id="d2a7a-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-354">Um dos seguintes identificadores de conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-354">One of the following character-set identifiers.</span></span>



| <span data-ttu-id="d2a7a-355">Decimal</span><span class="sxs-lookup"><span data-stu-id="d2a7a-355">Decimal</span></span> | <span data-ttu-id="d2a7a-356">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="d2a7a-356">Hexadecimal</span></span> | <span data-ttu-id="d2a7a-357">Conjunto de caracteres</span><span class="sxs-lookup"><span data-stu-id="d2a7a-357">Character Set</span></span>              |
|---------|-------------|----------------------------|
| <span data-ttu-id="d2a7a-358">0</span><span class="sxs-lookup"><span data-stu-id="d2a7a-358">0</span></span>       | <span data-ttu-id="d2a7a-359">0000</span><span class="sxs-lookup"><span data-stu-id="d2a7a-359">0000</span></span>        | <span data-ttu-id="d2a7a-360">ASCII de 7 bits</span><span class="sxs-lookup"><span data-stu-id="d2a7a-360">7-bit ASCII</span></span>                |
| <span data-ttu-id="d2a7a-361">932</span><span class="sxs-lookup"><span data-stu-id="d2a7a-361">932</span></span>     | <span data-ttu-id="d2a7a-362">03A4</span><span class="sxs-lookup"><span data-stu-id="d2a7a-362">03A4</span></span>        | <span data-ttu-id="d2a7a-363">Japão (Shift?</span><span class="sxs-lookup"><span data-stu-id="d2a7a-363">Japan (Shift ?</span></span> <span data-ttu-id="d2a7a-364">JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-364">JIS X-0208)</span></span> |
| <span data-ttu-id="d2a7a-365">949</span><span class="sxs-lookup"><span data-stu-id="d2a7a-365">949</span></span>     | <span data-ttu-id="d2a7a-366">03B5</span><span class="sxs-lookup"><span data-stu-id="d2a7a-366">03B5</span></span>        | <span data-ttu-id="d2a7a-367">Coreia (Shift?</span><span class="sxs-lookup"><span data-stu-id="d2a7a-367">Korea (Shift ?</span></span> <span data-ttu-id="d2a7a-368">KS 5601)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-368">KSC 5601)</span></span>   |
| <span data-ttu-id="d2a7a-369">950</span><span class="sxs-lookup"><span data-stu-id="d2a7a-369">950</span></span>     | <span data-ttu-id="d2a7a-370">03B6</span><span class="sxs-lookup"><span data-stu-id="d2a7a-370">03B6</span></span>        | <span data-ttu-id="d2a7a-371">Taiwan (Big5)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-371">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="d2a7a-372">1200</span><span class="sxs-lookup"><span data-stu-id="d2a7a-372">1200</span></span>    | <span data-ttu-id="d2a7a-373">04B0</span><span class="sxs-lookup"><span data-stu-id="d2a7a-373">04B0</span></span>        | <span data-ttu-id="d2a7a-374">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2a7a-374">Unicode</span></span>                    |
| <span data-ttu-id="d2a7a-375">1250</span><span class="sxs-lookup"><span data-stu-id="d2a7a-375">1250</span></span>    | <span data-ttu-id="d2a7a-376">04E2</span><span class="sxs-lookup"><span data-stu-id="d2a7a-376">04E2</span></span>        | <span data-ttu-id="d2a7a-377">Latim-2 (Europa Oriental)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-377">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="d2a7a-378">1251</span><span class="sxs-lookup"><span data-stu-id="d2a7a-378">1251</span></span>    | <span data-ttu-id="d2a7a-379">04E3</span><span class="sxs-lookup"><span data-stu-id="d2a7a-379">04E3</span></span>        | <span data-ttu-id="d2a7a-380">Cirílico</span><span class="sxs-lookup"><span data-stu-id="d2a7a-380">Cyrillic</span></span>                   |
| <span data-ttu-id="d2a7a-381">1252</span><span class="sxs-lookup"><span data-stu-id="d2a7a-381">1252</span></span>    | <span data-ttu-id="d2a7a-382">04E4</span><span class="sxs-lookup"><span data-stu-id="d2a7a-382">04E4</span></span>        | <span data-ttu-id="d2a7a-383">Multilíngüe</span><span class="sxs-lookup"><span data-stu-id="d2a7a-383">Multilingual</span></span>               |
| <span data-ttu-id="d2a7a-384">1253</span><span class="sxs-lookup"><span data-stu-id="d2a7a-384">1253</span></span>    | <span data-ttu-id="d2a7a-385">04E5</span><span class="sxs-lookup"><span data-stu-id="d2a7a-385">04E5</span></span>        | <span data-ttu-id="d2a7a-386">Grego</span><span class="sxs-lookup"><span data-stu-id="d2a7a-386">Greek</span></span>                      |
| <span data-ttu-id="d2a7a-387">1254</span><span class="sxs-lookup"><span data-stu-id="d2a7a-387">1254</span></span>    | <span data-ttu-id="d2a7a-388">04E6</span><span class="sxs-lookup"><span data-stu-id="d2a7a-388">04E6</span></span>        | <span data-ttu-id="d2a7a-389">Turco</span><span class="sxs-lookup"><span data-stu-id="d2a7a-389">Turkish</span></span>                    |
| <span data-ttu-id="d2a7a-390">1255</span><span class="sxs-lookup"><span data-stu-id="d2a7a-390">1255</span></span>    | <span data-ttu-id="d2a7a-391">04E7</span><span class="sxs-lookup"><span data-stu-id="d2a7a-391">04E7</span></span>        | <span data-ttu-id="d2a7a-392">Hebraico</span><span class="sxs-lookup"><span data-stu-id="d2a7a-392">Hebrew</span></span>                     |
| <span data-ttu-id="d2a7a-393">1256</span><span class="sxs-lookup"><span data-stu-id="d2a7a-393">1256</span></span>    | <span data-ttu-id="d2a7a-394">04E8</span><span class="sxs-lookup"><span data-stu-id="d2a7a-394">04E8</span></span>        | <span data-ttu-id="d2a7a-395">Árabe</span><span class="sxs-lookup"><span data-stu-id="d2a7a-395">Arabic</span></span>                     |



 

</dd> <dt>

<span data-ttu-id="d2a7a-396"><span id="string-name"></span><span id="STRING-NAME"></span>*nome da cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="d2a7a-396"><span id="string-name"></span><span id="STRING-NAME"></span>*string-name*</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-397">Um dos nomes predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-397">One of the following predefined names.</span></span>



| <span data-ttu-id="d2a7a-398">Nome</span><span class="sxs-lookup"><span data-stu-id="d2a7a-398">Name</span></span>                 | <span data-ttu-id="d2a7a-399">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a7a-399">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a7a-400">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-400">**Comments**</span></span>         | <span data-ttu-id="d2a7a-401">Informações adicionais que devem ser exibidas para fins de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-401">Additional information that should be displayed for diagnostic purposes.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="d2a7a-402">**CompanyName**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-402">**CompanyName**</span></span>      | <span data-ttu-id="d2a7a-403">Empresa que produziu o arquivo? por exemplo, "Microsoft Corporation" ou "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="d2a7a-403">Company that produced the file?for example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span> <span data-ttu-id="d2a7a-404">Essa cadeia de caracteres é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-404">This string is required.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="d2a7a-405">**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-405">**FileDescription**</span></span>  | <span data-ttu-id="d2a7a-406">Descrição do arquivo a ser apresentado aos usuários.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-406">File description to be presented to users.</span></span> <span data-ttu-id="d2a7a-407">Essa cadeia de caracteres pode ser exibida em uma caixa de listagem quando o usuário estiver escolhendo os arquivos a serem instalados? por exemplo, "driver de teclado para AT-Style teclados".</span><span class="sxs-lookup"><span data-stu-id="d2a7a-407">This string may be displayed in a list box when the user is choosing files to install?for example, "Keyboard Driver for AT-Style Keyboards".</span></span> <span data-ttu-id="d2a7a-408">Essa cadeia de caracteres é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-408">This string is required.</span></span>                                                                                            |
| <span data-ttu-id="d2a7a-409">**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-409">**FileVersion**</span></span>      | <span data-ttu-id="d2a7a-410">Número de versão do arquivo? por exemplo, "3,10" ou "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="d2a7a-410">Version number of the file?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="d2a7a-411">Essa cadeia de caracteres é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-411">This string is required.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="d2a7a-412">**InternalName**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-412">**InternalName**</span></span>     | <span data-ttu-id="d2a7a-413">Nome interno do arquivo, se houver um? por exemplo, um nome de módulo se o arquivo for uma biblioteca de vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-413">Internal name of the file, if one exists?for example, a module name if the file is a dynamic-link library.</span></span> <span data-ttu-id="d2a7a-414">Se o arquivo não tiver um nome interno, essa cadeia de caracteres deverá ser o nome de arquivo original, sem extensão.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-414">If the file has no internal name, this string should be the original filename, without extension.</span></span> <span data-ttu-id="d2a7a-415">Essa cadeia de caracteres é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-415">This string is required.</span></span>                                                                       |
| <span data-ttu-id="d2a7a-416">**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-416">**LegalCopyright**</span></span>   | <span data-ttu-id="d2a7a-417">Avisos de direitos autorais que se aplicam ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-417">Copyright notices that apply to the file.</span></span> <span data-ttu-id="d2a7a-418">Isso deve incluir o texto completo de todos os avisos, símbolos legais, datas de direitos autorais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-418">This should include the full text of all notices, legal symbols, copyright dates, and so on.</span></span> <span data-ttu-id="d2a7a-419">Essa cadeia de caracteres é opcional.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-419">This string is optional.</span></span>                                                                                                                                             |
| <span data-ttu-id="d2a7a-420">**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-420">**LegalTrademarks**</span></span>  | <span data-ttu-id="d2a7a-421">Marcas registradas e marcas registradas que se aplicam ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-421">Trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="d2a7a-422">Isso deve incluir o texto completo de todos os avisos, símbolos legais, números de marca e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-422">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="d2a7a-423">Essa cadeia de caracteres é opcional.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-423">This string is optional.</span></span>                                                                                                                        |
| <span data-ttu-id="d2a7a-424">**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-424">**OriginalFilename**</span></span> | <span data-ttu-id="d2a7a-425">Nome original do arquivo, sem incluir um caminho.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-425">Original name of the file, not including a path.</span></span> <span data-ttu-id="d2a7a-426">Essas informações permitem que um aplicativo determine se um arquivo foi renomeado por um usuário.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-426">This information enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="d2a7a-427">O formato do nome depende do sistema de arquivos para o qual o arquivo foi criado.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-427">The format of the name depends on the file system for which the file was created.</span></span> <span data-ttu-id="d2a7a-428">Essa cadeia de caracteres é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-428">This string is required.</span></span>                                                 |
| <span data-ttu-id="d2a7a-429">**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-429">**PrivateBuild**</span></span>     | <span data-ttu-id="d2a7a-430">Informações sobre uma versão particular do arquivo? por exemplo, "compilado por TESTER1 em \\ TESTBED".</span><span class="sxs-lookup"><span data-stu-id="d2a7a-430">Information about a private version of the file?for example, "Built by TESTER1 on \\TESTBED".</span></span> <span data-ttu-id="d2a7a-431">Essa cadeia de caracteres deve estar presente somente se o **vs \_ FF \_ PRIVATEBUILD** for especificado no parâmetro *FILEFLAGS* do bloco raiz.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-431">This string should be present only if **VS\_FF\_PRIVATEBUILD** is specified in the *fileflags* parameter of the root block.</span></span>                                                                                   |
| <span data-ttu-id="d2a7a-432">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-432">**ProductName**</span></span>      | <span data-ttu-id="d2a7a-433">Nome do produto com o qual o arquivo é distribuído.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-433">Name of the product with which the file is distributed.</span></span> <span data-ttu-id="d2a7a-434">Essa cadeia de caracteres é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-434">This string is required.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="d2a7a-435">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-435">**ProductVersion**</span></span>   | <span data-ttu-id="d2a7a-436">Versão do produto com a qual o arquivo é distribuído? por exemplo, "3,10" ou "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="d2a7a-436">Version of the product with which the file is distributed?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="d2a7a-437">Essa cadeia de caracteres é necessária.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-437">This string is required.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="d2a7a-438">**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-438">**SpecialBuild**</span></span>     | <span data-ttu-id="d2a7a-439">Texto que indica como esta versão do arquivo difere da versão padrão? por exemplo, "compilação particular para resolução de TESTER1 problemas de mouse em M250 e computadores M250E".</span><span class="sxs-lookup"><span data-stu-id="d2a7a-439">Text that indicates how this version of the file differs from the standard version?for example, "Private build for TESTER1 solving mouse problems on M250 and M250E computers".</span></span> <span data-ttu-id="d2a7a-440">Essa cadeia de caracteres deve estar presente somente se o **vs \_ FF \_ SPECIALBUILD** for especificado no parâmetro *FILEFLAGS* do bloco raiz.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-440">This string should be present only if **VS\_FF\_SPECIALBUILD** is specified in the *fileflags* parameter of the root block.</span></span> |



 

</dd> </dl>

<span data-ttu-id="d2a7a-441">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-441">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="d2a7a-442">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-442">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d2a7a-443">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-443">Examples</span></span>

<span data-ttu-id="d2a7a-444">O exemplo a seguir define um recurso **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="d2a7a-444">The following example defines a **VERSIONINFO** resource:</span></span>

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a><span data-ttu-id="d2a7a-445">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2a7a-445">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a7a-446">Usando informações de versão</span><span class="sxs-lookup"><span data-stu-id="d2a7a-446">Using Version Information</span></span>](./using-version-information.md)
</dt> <dt>

[<span data-ttu-id="d2a7a-447">Informações sobre versão</span><span class="sxs-lookup"><span data-stu-id="d2a7a-447">Version Information</span></span>](./version-information.md)
</dt> </dl>

 

 