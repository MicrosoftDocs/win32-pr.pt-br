---
title: Função MrmCreateResourceFileInMemory (MrmResourceIndexer. h)
description: Cria informações de PRI como um blob na memória, não como um arquivo no disco.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menus de função MrmCreateResourceFileInMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455791"
---
# <a name="mrmcreateresourcefileinmemory-function"></a><span data-ttu-id="2edbd-104">Função MrmCreateResourceFileInMemory</span><span class="sxs-lookup"><span data-stu-id="2edbd-104">MrmCreateResourceFileInMemory function</span></span>

<span data-ttu-id="2edbd-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2edbd-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2edbd-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2edbd-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2edbd-107">Cria informações de PRI como um blob na memória, não como um arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="2edbd-107">Creates PRI info as a blob in memory, not as a file on disk.</span></span> <span data-ttu-id="2edbd-108">A função aloca memória e retorna um ponteiro para essa memória em *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="2edbd-108">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="2edbd-109">Chame [**MrmFreeMemory**](mrmfreememory.md) com o mesmo ponteiro para liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="2edbd-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="2edbd-110">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="2edbd-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="2edbd-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2edbd-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a><span data-ttu-id="2edbd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2edbd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2edbd-113">*indexador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2edbd-113">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edbd-114">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="2edbd-114">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="2edbd-115">Um identificador que identifica o indexador de recursos do qual criar as informações de PRI.</span><span class="sxs-lookup"><span data-stu-id="2edbd-115">A handle identifying the resource indexer from which to create the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="2edbd-116">*packagmode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2edbd-116">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edbd-117">Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="2edbd-117">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="2edbd-118">Especifica se as informações de PRI devem ser autônomas ou ser um pacote de recursos.</span><span class="sxs-lookup"><span data-stu-id="2edbd-118">Specifies whether the PRI info should be standalone, or be a resource pack.</span></span> <span data-ttu-id="2edbd-119">Não há suporte para **MrmPackagingModeAutoSplit** .</span><span class="sxs-lookup"><span data-stu-id="2edbd-119">**MrmPackagingModeAutoSplit** is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2edbd-120">*packagoptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2edbd-120">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edbd-121">Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="2edbd-121">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="2edbd-122">Especifica opções adicionais sobre as informações de PRI.</span><span class="sxs-lookup"><span data-stu-id="2edbd-122">Specifies additional options about the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="2edbd-123">*outputPriData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2edbd-123">*outputPriData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2edbd-124">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="2edbd-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="2edbd-125">O endereço de um ponteiro para BYTE.</span><span class="sxs-lookup"><span data-stu-id="2edbd-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="2edbd-126">A função aloca memória e retorna um ponteiro para essa memória em *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="2edbd-126">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="2edbd-127">Chame [**MrmFreeMemory**](mrmfreememory.md) com o ponteiro para byte para liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="2edbd-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="2edbd-128">*outputPriSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2edbd-128">*outputPriSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2edbd-129">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="2edbd-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="2edbd-130">O endereço de um ULONG.</span><span class="sxs-lookup"><span data-stu-id="2edbd-130">The address of a ULONG.</span></span> <span data-ttu-id="2edbd-131">No _outputPriSize \*, a função retorna o tamanho da memória alocada apontada por *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="2edbd-131">In _outputPriSize\*, the function returns the size of the allocated memory pointed to by *outputPriData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2edbd-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2edbd-132">Return value</span></span>

<span data-ttu-id="2edbd-133">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2edbd-133">Type: **HRESULT**</span></span>

<span data-ttu-id="2edbd-134">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="2edbd-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="2edbd-135">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="2edbd-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2edbd-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="2edbd-136">Remarks</span></span>

<span data-ttu-id="2edbd-137">Se você passar *outputPriData* para [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), não libere a memória até depois de concluir o uso do indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="2edbd-137">If you pass *outputPriData* to [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), then don't free the memory until after you've finished using the resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2edbd-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2edbd-138">Requirements</span></span>



| <span data-ttu-id="2edbd-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2edbd-139">Requirement</span></span> | <span data-ttu-id="2edbd-140">Valor</span><span class="sxs-lookup"><span data-stu-id="2edbd-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2edbd-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2edbd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2edbd-142">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="2edbd-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2edbd-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2edbd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2edbd-144">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="2edbd-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2edbd-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2edbd-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2edbd-146"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2edbd-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="2edbd-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2edbd-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="2edbd-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2edbd-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="2edbd-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2edbd-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2edbd-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2edbd-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="2edbd-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="2edbd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2edbd-152">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="2edbd-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

