---
title: Estrutura StringTable
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de formatação de página de código e idioma para as cadeias de caracteres especificadas pelo membro filho. Uma página de código é um conjunto de caracteres ordenados.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menus de estrutura StringTable e outros recursos
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369357"
---
# <a name="stringtable-structure"></a><span data-ttu-id="1a9ba-106">Estrutura StringTable</span><span class="sxs-lookup"><span data-stu-id="1a9ba-106">StringTable structure</span></span>

<span data-ttu-id="1a9ba-107">Representa a organização de dados em um recurso de versão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-107">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="1a9ba-108">Ele contém informações de formatação de página de código e idioma para as cadeias de caracteres especificadas pelo membro **filho** .</span><span class="sxs-lookup"><span data-stu-id="1a9ba-108">It contains language and code page formatting information for the strings specified by the **Children** member.</span></span> <span data-ttu-id="1a9ba-109">Uma página de código é um conjunto de caracteres ordenados.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-109">A code page is an ordered character set.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a9ba-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a9ba-110">Syntax</span></span>


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a><span data-ttu-id="1a9ba-111">Membros</span><span class="sxs-lookup"><span data-stu-id="1a9ba-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="1a9ba-112">**wLength**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-112">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="1a9ba-113">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-113">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1a9ba-114">O comprimento, em bytes, dessa estrutura **STRINGTABLE** , incluindo todas as estruturas indicadas pelo membro **filho** .</span><span class="sxs-lookup"><span data-stu-id="1a9ba-114">The length, in bytes, of this **StringTable** structure, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="1a9ba-115">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-115">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="1a9ba-116">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1a9ba-117">Esse membro é sempre igual a zero.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-117">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a9ba-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="1a9ba-119">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1a9ba-120">O tipo de dados no recurso de versão.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-120">The type of data in the version resource.</span></span> <span data-ttu-id="1a9ba-121">Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="1a9ba-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="1a9ba-123">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="1a9ba-124">Um número hexadecimal de 8 dígitos armazenado como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-124">An 8-digit hexadecimal number stored as a Unicode string.</span></span> <span data-ttu-id="1a9ba-125">Os quatro dígitos mais significativos representam o identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-125">The four most significant digits represent the language identifier.</span></span> <span data-ttu-id="1a9ba-126">Os quatro dígitos menos significativos representam a página de código para a qual os dados são formatados.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-126">The four least significant digits represent the code page for which the data is formatted.</span></span> <span data-ttu-id="1a9ba-127">Cada identificador de idioma padrão da Microsoft contém duas partes: os 10 bits de ordem inferior especificam o idioma principal e os 6 bits de ordem superior especificam o subidioma.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-127">Each Microsoft Standard Language identifier contains two parts: the low-order 10 bits specify the major language, and the high-order 6 bits specify the sublanguage.</span></span> <span data-ttu-id="1a9ba-128">Para obter uma tabela de identificadores válidos, consulte.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-128">For a table of valid identifiers see .</span></span>

</dd> <dt>

<span data-ttu-id="1a9ba-129">**Preenchimento**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-129">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="1a9ba-130">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-130">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1a9ba-131">Tantas palavras zero quantas forem necessárias para alinhar o membro **filho** em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-131">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="1a9ba-132">**Filhos**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-132">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="1a9ba-133">Tipo: **[ **cadeia de caracteres**](string-str.md)**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-133">Type: **[**String**](string-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1a9ba-134">Uma matriz de uma ou mais estruturas de [**cadeia de caracteres**](string-str.md) .</span><span class="sxs-lookup"><span data-stu-id="1a9ba-134">An array of one or more [**String**](string-str.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a9ba-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a9ba-135">Remarks</span></span>

<span data-ttu-id="1a9ba-136">Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-136">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="1a9ba-137">Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-137">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="1a9ba-138">O membro **filho** da estrutura [**StringFileInfo**](stringfileinfo.md) contém pelo menos uma estrutura **STRINGTABLE** .</span><span class="sxs-lookup"><span data-stu-id="1a9ba-138">The **Children** member of the [**StringFileInfo**](stringfileinfo.md) structure contains at least one **StringTable** structure.</span></span>

<span data-ttu-id="1a9ba-139">Defina a parte da página de código do membro **szKey** como o valor hexadecimal 0x04b0 para indicar a página de código Unicode ou para o valor hexadecimal da página de código apropriada para o componente de linguagem.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-139">Set the code page portion of the **szKey** member to the hexadecimal value 0x04b0 to indicate the Unicode code page, or to the hexadecimal value of the code page that is appropriate for the language component.</span></span> <span data-ttu-id="1a9ba-140">Depois de escolher o valor para a página de código, você deve continuar a usar o mesmo valor em revisões posteriores para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-140">After you choose the value for the code page you should continue to use the same value in later revisions to the file.</span></span>

<span data-ttu-id="1a9ba-141">Um arquivo executável ou DLL que dá suporte a vários idiomas deve ter um recurso de versão para cada idioma, em vez de um único recurso de versão que contém cadeias de caracteres em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="1a9ba-141">An executable file or DLL that supports multiple languages should have a version resource for each language, rather than a single version resource that contains strings in several languages.</span></span> <span data-ttu-id="1a9ba-142">No entanto, se você usar a estrutura [**var**](var-str.md) para listar os idiomas aos quais seu aplicativo dá suporte, o número de estruturas **STRINGTABLE** no recurso de versão estará diretamente relacionado ao número de pares de identificador de página de código/idioma no membro de **valor** da estrutura **var** .</span><span class="sxs-lookup"><span data-stu-id="1a9ba-142">However, if you use the [**Var**](var-str.md) structure to list the languages that your application supports, the number of **StringTable** structures in the version resource is directly related to the number of language/code page identifier pairs in the **Value** member of the **Var** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a9ba-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a9ba-143">Requirements</span></span>



| <span data-ttu-id="1a9ba-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a9ba-144">Requirement</span></span> | <span data-ttu-id="1a9ba-145">Valor</span><span class="sxs-lookup"><span data-stu-id="1a9ba-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1a9ba-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a9ba-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1a9ba-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a9ba-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1a9ba-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a9ba-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1a9ba-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a9ba-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1a9ba-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a9ba-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a9ba-151">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a9ba-152">**Strings**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-152">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="1a9ba-153">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-153">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="1a9ba-154">**Var**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-154">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="1a9ba-155">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-155">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="1a9ba-156">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-156">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="1a9ba-157">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="1a9ba-157">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1a9ba-158">Informações sobre versão</span><span class="sxs-lookup"><span data-stu-id="1a9ba-158">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





