---
title: Estrutura da cadeia de caracteres
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém uma cadeia de caracteres que descreve um aspecto específico de um arquivo, por exemplo, a versão de um arquivo, seus avisos de direitos autorais ou suas marcas registradas.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menus de estrutura de cadeia de caracteres e outros recursos
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796140"
---
# <a name="string-structure"></a><span data-ttu-id="c2246-105">Estrutura da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="c2246-105">String structure</span></span>

<span data-ttu-id="c2246-106">Representa a organização de dados em um recurso de versão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2246-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="c2246-107">Ele contém uma cadeia de caracteres que descreve um aspecto específico de um arquivo, por exemplo, a versão de um arquivo, seus avisos de direitos autorais ou suas marcas registradas.</span><span class="sxs-lookup"><span data-stu-id="c2246-107">It contains a string that describes a specific aspect of a file, for example, a file's version, its copyright notices, or its trademarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2246-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2246-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a><span data-ttu-id="c2246-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c2246-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2246-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="c2246-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="c2246-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c2246-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c2246-112">O comprimento, em bytes, dessa estrutura de **cadeia de caracteres** .</span><span class="sxs-lookup"><span data-stu-id="c2246-112">The length, in bytes, of this **String** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c2246-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="c2246-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="c2246-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c2246-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c2246-115">O tamanho, em palavras, do membro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="c2246-115">The size, in words, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="c2246-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="c2246-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="c2246-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c2246-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c2246-118">O tipo de dados no recurso de versão.</span><span class="sxs-lookup"><span data-stu-id="c2246-118">The type of data in the version resource.</span></span> <span data-ttu-id="c2246-119">Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.</span><span class="sxs-lookup"><span data-stu-id="c2246-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="c2246-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="c2246-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="c2246-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="c2246-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="c2246-122">Uma cadeia de caracteres Unicode arbitrária.</span><span class="sxs-lookup"><span data-stu-id="c2246-122">An arbitrary Unicode string.</span></span> <span data-ttu-id="c2246-123">O membro **szKey** pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2246-123">The **szKey** member can be one or more of the following values.</span></span> <span data-ttu-id="c2246-124">Esses valores são apenas diretrizes.</span><span class="sxs-lookup"><span data-stu-id="c2246-124">These values are guidelines only.</span></span>

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span data-ttu-id="c2246-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Feitos**</span><span class="sxs-lookup"><span data-stu-id="c2246-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comments**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-126">O membro de **valor** contém qualquer informação adicional que deve ser exibida para fins de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c2246-126">The **Value** member contains any additional information that should be displayed for diagnostic purposes.</span></span> <span data-ttu-id="c2246-127">Essa cadeia de caracteres pode ter um comprimento arbitrário.</span><span class="sxs-lookup"><span data-stu-id="c2246-127">This string can be an arbitrary length.</span></span>

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span data-ttu-id="c2246-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span><span class="sxs-lookup"><span data-stu-id="c2246-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-129">O membro de **valor** identifica a empresa que produziu o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2246-129">The **Value** member identifies the company that produced the file.</span></span> <span data-ttu-id="c2246-130">Por exemplo, "Microsoft Corporation" ou "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="c2246-130">For example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span>

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span data-ttu-id="c2246-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="c2246-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-132">O membro de **valor** descreve o arquivo de forma que ele possa ser apresentado aos usuários.</span><span class="sxs-lookup"><span data-stu-id="c2246-132">The **Value** member describes the file in such a way that it can be presented to users.</span></span> <span data-ttu-id="c2246-133">Essa cadeia de caracteres pode ser apresentada em uma caixa de listagem quando o usuário estiver escolhendo os arquivos a serem instalados.</span><span class="sxs-lookup"><span data-stu-id="c2246-133">This string may be presented in a list box when the user is choosing files to install.</span></span> <span data-ttu-id="c2246-134">Por exemplo, "driver de teclado para os teclados no estilo" ou "Microsoft Word para Windows".</span><span class="sxs-lookup"><span data-stu-id="c2246-134">For example, "Keyboard driver for AT-style keyboards" or "Microsoft Word for Windows".</span></span>

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span data-ttu-id="c2246-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="c2246-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-136">O membro de **valor** identifica a versão deste arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2246-136">The **Value** member identifies the version of this file.</span></span> <span data-ttu-id="c2246-137">Por exemplo, o **valor** poderia ser "3,00 a" ou "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="c2246-137">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span data-ttu-id="c2246-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**Internoname**</span><span class="sxs-lookup"><span data-stu-id="c2246-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-139">O membro de **valor** identifica o nome interno do arquivo, se houver.</span><span class="sxs-lookup"><span data-stu-id="c2246-139">The **Value** member identifies the file's internal name, if one exists.</span></span> <span data-ttu-id="c2246-140">Por exemplo, essa cadeia de caracteres pode conter o nome do módulo para uma DLL, um nome de dispositivo virtual para um dispositivo virtual do Windows ou um nome de dispositivo para um driver de dispositivo MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="c2246-140">For example, this string could contain the module name for a DLL, a virtual device name for a Windows virtual device, or a device name for a MS-DOS device driver.</span></span>

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span data-ttu-id="c2246-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="c2246-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-142">O membro de **valor** descreve todos os avisos de direitos autorais, marcas registradas e marcas registradas que se aplicam ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2246-142">The **Value** member describes all copyright notices, trademarks, and registered trademarks that apply to the file.</span></span> <span data-ttu-id="c2246-143">Isso deve incluir o texto completo de todos os avisos, símbolos legais, datas de direitos autorais, números de marca e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c2246-143">This should include the full text of all notices, legal symbols, copyright dates, trademark numbers, and so on.</span></span> <span data-ttu-id="c2246-144">Em inglês, essa cadeia de caracteres deve estar no formato "Copyright Microsoft Corp. 1990 1994".</span><span class="sxs-lookup"><span data-stu-id="c2246-144">In English, this string should be in the format "Copyright Microsoft Corp. 1990  1994".</span></span>

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span data-ttu-id="c2246-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="c2246-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-146">O membro de **valor** descreve todas as marcas registradas e marcas registradas que se aplicam ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2246-146">The **Value** member describes all trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="c2246-147">Isso deve incluir o texto completo de todos os avisos, símbolos legais, números de marca e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c2246-147">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="c2246-148">Em inglês, essa cadeia de caracteres deve estar no formato "Windows is a trademark of Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="c2246-148">In English, this string should be in the format "Windows is a trademark of Microsoft Corporation".</span></span>

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span data-ttu-id="c2246-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="c2246-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-150">O membro de **valor** identifica o nome original do arquivo, sem incluir um caminho.</span><span class="sxs-lookup"><span data-stu-id="c2246-150">The **Value** member identifies the original name of the file, not including a path.</span></span> <span data-ttu-id="c2246-151">Isso permite que um aplicativo determine se um arquivo foi renomeado por um usuário.</span><span class="sxs-lookup"><span data-stu-id="c2246-151">This enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="c2246-152">Esse nome não pode ser MS-DOS 8,3 se o arquivo for específico para um sistema de arquivos não FAT.</span><span class="sxs-lookup"><span data-stu-id="c2246-152">This name may not be MS-DOS 8.3-format if the file is specific to a non-FAT file system.</span></span>

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span data-ttu-id="c2246-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="c2246-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-154">O membro de **valor** descreve por quem, onde e por que esta versão particular do arquivo foi criada.</span><span class="sxs-lookup"><span data-stu-id="c2246-154">The **Value** member describes by whom, where, and why this private version of the file was built.</span></span> <span data-ttu-id="c2246-155">Essa cadeia de caracteres só deverá estar presente se o sinalizador do **vs \_ FF \_ PRIVATEBUILD** estiver definido no membro **dwFileFlags** da estrutura do [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="c2246-155">This string should only be present if the **VS\_FF\_PRIVATEBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="c2246-156">Por exemplo, o **valor** poderia ser "criado pela interface Oscar on \\ OSCAR2".</span><span class="sxs-lookup"><span data-stu-id="c2246-156">For example, **Value** could be "Built by OSCAR on \\OSCAR2".</span></span>

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span data-ttu-id="c2246-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**NomeDoProduto**</span><span class="sxs-lookup"><span data-stu-id="c2246-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-158">O membro de **valor** identifica o nome do produto com o qual esse arquivo é distribuído.</span><span class="sxs-lookup"><span data-stu-id="c2246-158">The **Value** member identifies the name of the product with which this file is distributed.</span></span> <span data-ttu-id="c2246-159">Por exemplo, essa cadeia de caracteres pode ser "Microsoft Windows".</span><span class="sxs-lookup"><span data-stu-id="c2246-159">For example, this string could be "Microsoft Windows".</span></span>

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span data-ttu-id="c2246-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="c2246-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-161">O membro de **valor** identifica a versão do produto com a qual esse arquivo é distribuído.</span><span class="sxs-lookup"><span data-stu-id="c2246-161">The **Value** member identifies the version of the product with which this file is distributed.</span></span> <span data-ttu-id="c2246-162">Por exemplo, o **valor** poderia ser "3,00 a" ou "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="c2246-162">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span data-ttu-id="c2246-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="c2246-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span></span>


</dt> <dd>

<span data-ttu-id="c2246-164">O membro de **valor** descreve como essa versão do arquivo difere da versão normal.</span><span class="sxs-lookup"><span data-stu-id="c2246-164">The **Value** member describes how this version of the file differs from the normal version.</span></span> <span data-ttu-id="c2246-165">Essa entrada só deverá estar presente se o sinalizador do **vs \_ FF \_ SPECIALBUILD** estiver definido no membro **dwFileFlags** da estrutura do [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="c2246-165">This entry should only be present if the **VS\_FF\_SPECIALBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="c2246-166">Por exemplo, o **valor** poderia ser "compilação particular para a resolução de problemas de mouse em M250 e M250E Computers".</span><span class="sxs-lookup"><span data-stu-id="c2246-166">For example, **Value** could be "Private build for Olivetti solving mouse problems on M250 and M250E computers".</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c2246-167">**Preenchimento**</span><span class="sxs-lookup"><span data-stu-id="c2246-167">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="c2246-168">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c2246-168">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c2246-169">Tantas palavras zero quantas forem necessárias para alinhar o membro de **valor** em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c2246-169">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="c2246-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c2246-170">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="c2246-171">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c2246-171">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c2246-172">Uma cadeia de caracteres terminada em zero.</span><span class="sxs-lookup"><span data-stu-id="c2246-172">A zero-terminated string.</span></span> <span data-ttu-id="c2246-173">Consulte a descrição do membro **szKey** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c2246-173">See the **szKey** member description for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2246-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2246-174">Remarks</span></span>

<span data-ttu-id="c2246-175">Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="c2246-175">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="c2246-176">Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="c2246-176">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="c2246-177">Uma estrutura de **cadeia de caracteres** pode ter um valor de **szKey** de, por exemplo, "CompanyName" e um **valor** de "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="c2246-177">A **String** structure may have an **szKey** value of, for example, "CompanyName" and a **Value** of "Microsoft Corporation".</span></span> <span data-ttu-id="c2246-178">Outra estrutura de **cadeia de caracteres** com o mesmo valor de **szKey** pode conter um **valor** de "Microsoft GmbH".</span><span class="sxs-lookup"><span data-stu-id="c2246-178">Another **String** structure with the same **szKey** value could contain a **Value** of "Microsoft GmbH".</span></span> <span data-ttu-id="c2246-179">Isso pode ocorrer se a segunda estrutura de **cadeia de caracteres** estivesse associada a uma estrutura [**STRINGTABLE**](stringtable.md) cujo valor **szKey** seja 040704b0, alemão/Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2246-179">This might occur if the second **String** structure were associated with a [**StringTable**](stringtable.md) structure whose **szKey** value is 040704b0   that is, German/Unicode.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2246-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2246-180">Requirements</span></span>



| <span data-ttu-id="c2246-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2246-181">Requirement</span></span> | <span data-ttu-id="c2246-182">Valor</span><span class="sxs-lookup"><span data-stu-id="c2246-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c2246-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2246-183">Minimum supported client</span></span><br/> | <span data-ttu-id="c2246-184">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2246-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2246-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2246-185">Minimum supported server</span></span><br/> | <span data-ttu-id="c2246-186">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2246-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c2246-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2246-187">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2246-188">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c2246-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2246-189">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="c2246-189">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="c2246-190">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="c2246-190">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[<span data-ttu-id="c2246-191">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="c2246-191">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="c2246-192">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="c2246-192">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="c2246-193">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c2246-193">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c2246-194">Informações sobre versão</span><span class="sxs-lookup"><span data-stu-id="c2246-194">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





