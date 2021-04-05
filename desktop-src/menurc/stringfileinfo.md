---
title: Estrutura StringFileInfo
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão que podem ser exibidas para uma determinada linguagem e página de código.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menus de estrutura StringFileInfo e outros recursos
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918122"
---
# <a name="stringfileinfo-structure"></a><span data-ttu-id="19eb2-105">Estrutura StringFileInfo</span><span class="sxs-lookup"><span data-stu-id="19eb2-105">StringFileInfo structure</span></span>

<span data-ttu-id="19eb2-106">Representa a organização de dados em um recurso de versão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="19eb2-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="19eb2-107">Ele contém informações de versão que podem ser exibidas para uma determinada linguagem e página de código.</span><span class="sxs-lookup"><span data-stu-id="19eb2-107">It contains version information that can be displayed for a particular language and code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="19eb2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19eb2-108">Syntax</span></span>


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a><span data-ttu-id="19eb2-109">Membros</span><span class="sxs-lookup"><span data-stu-id="19eb2-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="19eb2-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="19eb2-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="19eb2-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="19eb2-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="19eb2-112">O comprimento, em bytes, do bloco **StringFileInfo** inteiro, incluindo todas as estruturas indicadas pelo membro **filho** .</span><span class="sxs-lookup"><span data-stu-id="19eb2-112">The length, in bytes, of the entire **StringFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="19eb2-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="19eb2-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="19eb2-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="19eb2-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="19eb2-115">Esse membro é sempre igual a zero.</span><span class="sxs-lookup"><span data-stu-id="19eb2-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="19eb2-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="19eb2-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="19eb2-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="19eb2-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="19eb2-118">O tipo de dados no recurso de versão.</span><span class="sxs-lookup"><span data-stu-id="19eb2-118">The type of data in the version resource.</span></span> <span data-ttu-id="19eb2-119">Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.</span><span class="sxs-lookup"><span data-stu-id="19eb2-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="19eb2-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="19eb2-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="19eb2-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="19eb2-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="19eb2-122">A cadeia de caracteres Unicode L "StringFileInfo".</span><span class="sxs-lookup"><span data-stu-id="19eb2-122">The Unicode string L"StringFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="19eb2-123">**Preenchimento**</span><span class="sxs-lookup"><span data-stu-id="19eb2-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="19eb2-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="19eb2-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="19eb2-125">Tantas palavras zero quantas forem necessárias para alinhar o membro **filho** em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="19eb2-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="19eb2-126">**Filhos**</span><span class="sxs-lookup"><span data-stu-id="19eb2-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="19eb2-127">Tipo: **[ **STRINGTABLE**](stringtable.md)**</span><span class="sxs-lookup"><span data-stu-id="19eb2-127">Type: **[**StringTable**](stringtable.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19eb2-128">Uma matriz de uma ou mais estruturas [**STRINGTABLE**](stringtable.md) .</span><span class="sxs-lookup"><span data-stu-id="19eb2-128">An array of one or more [**StringTable**](stringtable.md) structures.</span></span> <span data-ttu-id="19eb2-129">Cada membro **szKey** da estrutura **STRINGTABLE** indica o idioma e a página de código apropriados para exibir o texto nessa estrutura **STRINGTABLE** .</span><span class="sxs-lookup"><span data-stu-id="19eb2-129">Each **StringTable** structure's **szKey** member indicates the appropriate language and code page for displaying the text in that **StringTable** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19eb2-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="19eb2-130">Remarks</span></span>

<span data-ttu-id="19eb2-131">Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="19eb2-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="19eb2-132">Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="19eb2-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="19eb2-133">O membro **filho** da estrutura do [**vs \_ VERSIONINFO**](vs-versioninfo.md) pode conter zero ou mais estruturas **StringFileInfo** .</span><span class="sxs-lookup"><span data-stu-id="19eb2-133">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or more **StringFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="19eb2-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19eb2-134">Requirements</span></span>



| <span data-ttu-id="19eb2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="19eb2-135">Requirement</span></span> | <span data-ttu-id="19eb2-136">Valor</span><span class="sxs-lookup"><span data-stu-id="19eb2-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="19eb2-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19eb2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="19eb2-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="19eb2-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="19eb2-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19eb2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="19eb2-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="19eb2-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="19eb2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="19eb2-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="19eb2-142">**Referência**</span><span class="sxs-lookup"><span data-stu-id="19eb2-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19eb2-143">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="19eb2-143">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="19eb2-144">**Strings**</span><span class="sxs-lookup"><span data-stu-id="19eb2-144">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="19eb2-145">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="19eb2-145">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="19eb2-146">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="19eb2-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="19eb2-147">Informações sobre versão</span><span class="sxs-lookup"><span data-stu-id="19eb2-147">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





