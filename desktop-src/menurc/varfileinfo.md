---
title: Estrutura VarFileInfo
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão não dependentes de uma combinação de linguagem de código e de idioma específico.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menus de estrutura VarFileInfo e outros recursos
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790309"
---
# <a name="varfileinfo-structure"></a><span data-ttu-id="cdb57-105">Estrutura VarFileInfo</span><span class="sxs-lookup"><span data-stu-id="cdb57-105">VarFileInfo structure</span></span>

<span data-ttu-id="cdb57-106">Representa a organização de dados em um recurso de versão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="cdb57-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="cdb57-107">Ele contém informações de versão não dependentes de uma combinação de linguagem de código e de idioma específico.</span><span class="sxs-lookup"><span data-stu-id="cdb57-107">It contains version information not dependent on a particular language and code page combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb57-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdb57-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a><span data-ttu-id="cdb57-109">Membros</span><span class="sxs-lookup"><span data-stu-id="cdb57-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="cdb57-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="cdb57-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="cdb57-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="cdb57-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdb57-112">O comprimento, em bytes, do bloco **VarFileInfo** inteiro, incluindo todas as estruturas indicadas pelo membro **filho** .</span><span class="sxs-lookup"><span data-stu-id="cdb57-112">The length, in bytes, of the entire **VarFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="cdb57-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="cdb57-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="cdb57-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="cdb57-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdb57-115">Esse membro é sempre igual a zero.</span><span class="sxs-lookup"><span data-stu-id="cdb57-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cdb57-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="cdb57-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="cdb57-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="cdb57-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdb57-118">O tipo de dados no recurso de versão.</span><span class="sxs-lookup"><span data-stu-id="cdb57-118">The type of data in the version resource.</span></span> <span data-ttu-id="cdb57-119">Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.</span><span class="sxs-lookup"><span data-stu-id="cdb57-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="cdb57-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="cdb57-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="cdb57-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="cdb57-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="cdb57-122">A cadeia de caracteres Unicode L "VarFileInfo".</span><span class="sxs-lookup"><span data-stu-id="cdb57-122">The Unicode string L"VarFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="cdb57-123">**Preenchimento**</span><span class="sxs-lookup"><span data-stu-id="cdb57-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="cdb57-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="cdb57-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cdb57-125">Tantas palavras zero quantas forem necessárias para alinhar o membro **filho** em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cdb57-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="cdb57-126">**Filhos**</span><span class="sxs-lookup"><span data-stu-id="cdb57-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="cdb57-127">Tipo: **[ **var**](var-str.md)**</span><span class="sxs-lookup"><span data-stu-id="cdb57-127">Type: **[**Var**](var-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cdb57-128">Normalmente contém uma lista de idiomas aos quais o aplicativo ou DLL dá suporte.</span><span class="sxs-lookup"><span data-stu-id="cdb57-128">Typically contains a list of languages that the application or DLL supports.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdb57-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdb57-129">Remarks</span></span>

<span data-ttu-id="cdb57-130">Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="cdb57-130">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="cdb57-131">Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="cdb57-131">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="cdb57-132">O membro **filho** da estrutura do [**vs \_ VERSIONINFO**](vs-versioninfo.md) pode conter zero ou um **VarFileInfo** estruturas.</span><span class="sxs-lookup"><span data-stu-id="cdb57-132">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or one **VarFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb57-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdb57-133">Requirements</span></span>



| <span data-ttu-id="cdb57-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdb57-134">Requirement</span></span> | <span data-ttu-id="cdb57-135">Valor</span><span class="sxs-lookup"><span data-stu-id="cdb57-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="cdb57-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdb57-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb57-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdb57-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cdb57-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdb57-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb57-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdb57-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cdb57-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdb57-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="cdb57-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cdb57-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cdb57-142">**Var**</span><span class="sxs-lookup"><span data-stu-id="cdb57-142">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="cdb57-143">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="cdb57-143">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="cdb57-144">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="cdb57-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cdb57-145">Informações sobre versão</span><span class="sxs-lookup"><span data-stu-id="cdb57-145">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





