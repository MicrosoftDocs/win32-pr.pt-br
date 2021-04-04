---
title: Estrutura de var
description: Representa a organização de dados em um recurso de versão de arquivo. Normalmente, ele contém uma lista de pares de identificadores de página de código e de idioma para os quais a versão do aplicativo ou DLL dá suporte.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menus de estrutura de var e outros recursos
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824771"
---
# <a name="var-structure"></a><span data-ttu-id="44cff-105">Estrutura de var</span><span class="sxs-lookup"><span data-stu-id="44cff-105">Var structure</span></span>

<span data-ttu-id="44cff-106">Representa a organização de dados em um recurso de versão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="44cff-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="44cff-107">Normalmente, ele contém uma lista de pares de identificadores de página de código e de idioma para os quais a versão do aplicativo ou DLL dá suporte.</span><span class="sxs-lookup"><span data-stu-id="44cff-107">It typically contains a list of language and code page identifier pairs that the version of the application or DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="44cff-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44cff-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a><span data-ttu-id="44cff-109">Membros</span><span class="sxs-lookup"><span data-stu-id="44cff-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="44cff-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="44cff-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="44cff-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="44cff-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="44cff-112">O comprimento, em bytes, da estrutura **var** .</span><span class="sxs-lookup"><span data-stu-id="44cff-112">The length, in bytes, of the **Var** structure.</span></span>

</dd> <dt>

<span data-ttu-id="44cff-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="44cff-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="44cff-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="44cff-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="44cff-115">O comprimento, em bytes, do membro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="44cff-115">The length, in bytes, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="44cff-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="44cff-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="44cff-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="44cff-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="44cff-118">O tipo de dados no recurso de versão.</span><span class="sxs-lookup"><span data-stu-id="44cff-118">The type of data in the version resource.</span></span> <span data-ttu-id="44cff-119">Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.</span><span class="sxs-lookup"><span data-stu-id="44cff-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="44cff-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="44cff-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="44cff-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="44cff-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="44cff-122">A cadeia de caracteres Unicode L "translation".</span><span class="sxs-lookup"><span data-stu-id="44cff-122">The Unicode string L"Translation".</span></span>

</dd> <dt>

<span data-ttu-id="44cff-123">**Preenchimento**</span><span class="sxs-lookup"><span data-stu-id="44cff-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="44cff-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="44cff-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="44cff-125">Tantas palavras zero quantas forem necessárias para alinhar o membro de **valor** em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="44cff-125">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="44cff-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="44cff-126">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="44cff-127">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="44cff-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="44cff-128">Uma matriz de um ou mais valores que são pares de identificador de página de código e idioma.</span><span class="sxs-lookup"><span data-stu-id="44cff-128">An array of one or more values that are language and code page identifier pairs.</span></span> <span data-ttu-id="44cff-129">Para obter informações adicionais, consulte a seção de comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="44cff-129">For additional information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44cff-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="44cff-130">Remarks</span></span>

<span data-ttu-id="44cff-131">Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="44cff-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="44cff-132">Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="44cff-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="44cff-133">Se você usar a estrutura **var** para listar os idiomas aos quais seu aplicativo ou DLL dá suporte em vez de usar vários recursos de versão, use o membro **Value** para conter uma matriz de valores **DWORD** indicando as combinações de idioma e página de código com suporte neste arquivo.</span><span class="sxs-lookup"><span data-stu-id="44cff-133">If you use the **Var** structure to list the languages your application or DLL supports instead of using multiple version resources, use the **Value** member to contain an array of **DWORD** values indicating the language and code page combinations supported by this file.</span></span> <span data-ttu-id="44cff-134">A palavra de ordem inferior de cada **DWORD** deve conter um identificador de idioma da Microsoft e a palavra de ordem superior deve conter o número da página de código IBM.</span><span class="sxs-lookup"><span data-stu-id="44cff-134">The low-order word of each **DWORD** must contain a Microsoft language identifier, and the high-order word must contain the IBM code page number.</span></span> <span data-ttu-id="44cff-135">A palavra de ordem superior ou de ordem inferior pode ser zero, indicando que o arquivo é independente da linguagem ou da página de código.</span><span class="sxs-lookup"><span data-stu-id="44cff-135">Either high-order or low-order word can be zero, indicating that the file is language or code page independent.</span></span> <span data-ttu-id="44cff-136">Se a estrutura de **var** for omitida, o arquivo será interpretado como independente da linguagem e da página de código.</span><span class="sxs-lookup"><span data-stu-id="44cff-136">If the **Var** structure is omitted, the file will be interpreted as both language and code page independent.</span></span>

## <a name="requirements"></a><span data-ttu-id="44cff-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44cff-137">Requirements</span></span>



| <span data-ttu-id="44cff-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="44cff-138">Requirement</span></span> | <span data-ttu-id="44cff-139">Valor</span><span class="sxs-lookup"><span data-stu-id="44cff-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="44cff-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44cff-140">Minimum supported client</span></span><br/> | <span data-ttu-id="44cff-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44cff-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="44cff-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44cff-142">Minimum supported server</span></span><br/> | <span data-ttu-id="44cff-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44cff-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="44cff-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="44cff-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="44cff-145">**Referência**</span><span class="sxs-lookup"><span data-stu-id="44cff-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="44cff-146">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="44cff-146">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="44cff-147">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="44cff-147">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="44cff-148">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="44cff-148">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="44cff-149">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="44cff-149">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="44cff-150">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="44cff-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="44cff-151">Informações sobre versão</span><span class="sxs-lookup"><span data-stu-id="44cff-151">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





