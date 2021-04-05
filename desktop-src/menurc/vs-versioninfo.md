---
title: Estrutura de VS_VERSIONINFO
description: Representa a organização de dados em um recurso de versão de arquivo. É a estrutura raiz que contém todas as outras estruturas de informações de versão de arquivo.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO de menus de estrutura e outros recursos
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086383"
---
# <a name="vs_versioninfo-structure"></a><span data-ttu-id="3e28b-105">Estrutura do VS \_ VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="3e28b-105">VS\_VERSIONINFO structure</span></span>

<span data-ttu-id="3e28b-106">Representa a organização de dados em um recurso de versão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3e28b-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="3e28b-107">É a estrutura raiz que contém todas as outras estruturas de informações de versão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3e28b-107">It is the root structure that contains all other file-version information structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e28b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e28b-108">Syntax</span></span>


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="3e28b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="3e28b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e28b-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="3e28b-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="3e28b-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="3e28b-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e28b-112">O comprimento, em bytes, da estrutura do **vs \_ VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="3e28b-112">The length, in bytes, of the **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="3e28b-113">Esse comprimento não inclui nenhum preenchimento que alinhe quaisquer dados de recursos de versão subsequentes em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e28b-113">This length does not include any padding that aligns any subsequent version resource data on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="3e28b-114">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="3e28b-114">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="3e28b-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="3e28b-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e28b-116">O comprimento, em bytes, do membro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="3e28b-116">The length, in bytes, of the **Value** member.</span></span> <span data-ttu-id="3e28b-117">Esse valor será zero se não houver nenhum membro de **valor** associado à estrutura de versão atual.</span><span class="sxs-lookup"><span data-stu-id="3e28b-117">This value is zero if there is no **Value** member associated with the current version structure.</span></span>

</dd> <dt>

<span data-ttu-id="3e28b-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="3e28b-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="3e28b-119">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="3e28b-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e28b-120">O tipo de dados no recurso de versão.</span><span class="sxs-lookup"><span data-stu-id="3e28b-120">The type of data in the version resource.</span></span> <span data-ttu-id="3e28b-121">Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.</span><span class="sxs-lookup"><span data-stu-id="3e28b-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="3e28b-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="3e28b-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="3e28b-123">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="3e28b-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="3e28b-124">A cadeia de caracteres Unicode L " \_ informações de versão vs \_ ".</span><span class="sxs-lookup"><span data-stu-id="3e28b-124">The Unicode string L"VS\_VERSION\_INFO".</span></span>

</dd> <dt>

<span data-ttu-id="3e28b-125">**Padding1**</span><span class="sxs-lookup"><span data-stu-id="3e28b-125">**Padding1**</span></span>
</dt> <dd>

<span data-ttu-id="3e28b-126">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="3e28b-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e28b-127">Contém tantas palavras zero quantas forem necessárias para alinhar o membro de **valor** em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e28b-127">Contains as many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="3e28b-128">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3e28b-128">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="3e28b-129">Tipo: **[ **vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span><span class="sxs-lookup"><span data-stu-id="3e28b-129">Type: **[**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span></span>

</dd> <dd>

<span data-ttu-id="3e28b-130">Dados arbitrários associados a esta estrutura do **vs \_ VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="3e28b-130">Arbitrary data associated with this **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="3e28b-131">O membro **wValueLength** especifica o comprimento deste membro; Se **wValueLength** for zero, esse membro não existirá.</span><span class="sxs-lookup"><span data-stu-id="3e28b-131">The **wValueLength** member specifies the length of this member; if **wValueLength** is zero, this member does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="3e28b-132">**Padding2**</span><span class="sxs-lookup"><span data-stu-id="3e28b-132">**Padding2**</span></span>
</dt> <dd>

<span data-ttu-id="3e28b-133">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="3e28b-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e28b-134">Tantas palavras zero quantas forem necessárias para alinhar o membro **filho** em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e28b-134">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span> <span data-ttu-id="3e28b-135">Esses bytes não estão incluídos no **wValueLength**.</span><span class="sxs-lookup"><span data-stu-id="3e28b-135">These bytes are not included in **wValueLength**.</span></span> <span data-ttu-id="3e28b-136">Esse membro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3e28b-136">This member is optional.</span></span>

</dd> <dt>

<span data-ttu-id="3e28b-137">**Filhos**</span><span class="sxs-lookup"><span data-stu-id="3e28b-137">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="3e28b-138">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="3e28b-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e28b-139">Uma matriz de zero ou uma estrutura [**StringFileInfo**](stringfileinfo.md) e nenhuma ou uma estrutura [**VarFileInfo**](varfileinfo.md) que são filhos da estrutura atual do **vs \_ VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="3e28b-139">An array of zero or one [**StringFileInfo**](stringfileinfo.md) structures, and zero or one [**VarFileInfo**](varfileinfo.md) structures that are children of the current **VS\_VERSIONINFO** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e28b-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e28b-140">Remarks</span></span>

<span data-ttu-id="3e28b-141">Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="3e28b-141">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="3e28b-142">Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="3e28b-142">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e28b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e28b-143">Requirements</span></span>



| <span data-ttu-id="3e28b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e28b-144">Requirement</span></span> | <span data-ttu-id="3e28b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="3e28b-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3e28b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e28b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3e28b-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3e28b-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3e28b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e28b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3e28b-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3e28b-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3e28b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e28b-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e28b-151">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3e28b-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e28b-152">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="3e28b-152">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="3e28b-153">**VerQueryValue**</span><span class="sxs-lookup"><span data-stu-id="3e28b-153">**VerQueryValue**</span></span>](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[<span data-ttu-id="3e28b-154">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="3e28b-154">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="3e28b-155">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="3e28b-155">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

<span data-ttu-id="3e28b-156">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="3e28b-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e28b-157">Informações sobre versão</span><span class="sxs-lookup"><span data-stu-id="3e28b-157">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





