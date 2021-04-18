---
title: Função MrmDumpPriDataInMemory (MrmResourceIndexer. h)
description: Despeja informações de PRI (como um blob na memória, criado por uma chamada anterior para MrmCreateResourceFileInMemory) para seu equivalente XML (como dados na memória), para torná-la mais fácil de ler.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menus de função MrmDumpPriDataInMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759015"
---
# <a name="mrmdumppridatainmemory-function"></a><span data-ttu-id="1287d-104">Função MrmDumpPriDataInMemory</span><span class="sxs-lookup"><span data-stu-id="1287d-104">MrmDumpPriDataInMemory function</span></span>

<span data-ttu-id="1287d-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1287d-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1287d-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1287d-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1287d-107">Despeja informações de PRI (como um blob na memória, criado por uma chamada anterior para [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) para seu equivalente XML (como dados na memória), para torná-la mais fácil de ler.</span><span class="sxs-lookup"><span data-stu-id="1287d-107">Dumps PRI info (as a blob in memory, created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="1287d-108">A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="1287d-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="1287d-109">Chame [**MrmFreeMemory**](mrmfreememory.md) com o mesmo ponteiro para liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="1287d-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="1287d-110">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="1287d-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="1287d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1287d-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="1287d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1287d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1287d-113">*inputPriData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1287d-113">*inputPriData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1287d-114">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="1287d-114">Type: \**BYTE\** _</span></span>

<span data-ttu-id="1287d-115">Um ponteiro para dados PRI criados por uma chamada anterior para [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1287d-115">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1287d-116">*inputPriSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1287d-116">*inputPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1287d-117">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="1287d-117">Type: **ULONG**</span></span>

<span data-ttu-id="1287d-118">O tamanho dos dados apontados por *inputPriData*.</span><span class="sxs-lookup"><span data-stu-id="1287d-118">The size of the data pointed to by *inputPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="1287d-119">*schemaPriData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1287d-119">*schemaPriData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1287d-120">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="1287d-120">Type: \**BYTE\** _</span></span>

<span data-ttu-id="1287d-121">Um ponteiro opcional para informações de PRI (como um blob na memória) que representa os dados de esquema criados por uma chamada anterior para [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1287d-121">An optional pointer to PRI info (as a blob in memory) representing schema data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="1287d-122">Não libere *schemaPriData* até terminar de usar o indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="1287d-122">Don't free *schemaPriData* until after you've finished using the resource indexer.</span></span> <span data-ttu-id="1287d-123">Consulte também comentários.</span><span class="sxs-lookup"><span data-stu-id="1287d-123">Also see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1287d-124">*schemaPriSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1287d-124">*schemaPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1287d-125">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="1287d-125">Type: **ULONG**</span></span>

<span data-ttu-id="1287d-126">O tamanho dos dados apontados por *schemaPriData*.</span><span class="sxs-lookup"><span data-stu-id="1287d-126">The size of the data pointed to by *schemaPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="1287d-127">*dumptype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1287d-127">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1287d-128">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="1287d-128">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="1287d-129">Especifica o quão detalhado o despejo de XML deve ser ou se um esquema deve ser despejado.</span><span class="sxs-lookup"><span data-stu-id="1287d-129">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="1287d-130">*outputXmlData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1287d-130">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1287d-131">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="1287d-131">Type: **BYTE\*\***</span></span>

<span data-ttu-id="1287d-132">O endereço de um ponteiro para BYTE.</span><span class="sxs-lookup"><span data-stu-id="1287d-132">The address of a pointer to BYTE.</span></span> <span data-ttu-id="1287d-133">A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="1287d-133">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="1287d-134">Chame [**MrmFreeMemory**](mrmfreememory.md) com o ponteiro para byte para liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="1287d-134">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="1287d-135">*outputXmlSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1287d-135">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1287d-136">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="1287d-136">Type: \**ULONG\** _</span></span>

<span data-ttu-id="1287d-137">O endereço de um ULONG.</span><span class="sxs-lookup"><span data-stu-id="1287d-137">The address of a ULONG.</span></span> <span data-ttu-id="1287d-138">No _outputXmlSize \*, a função retorna o tamanho da memória alocada apontada por *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="1287d-138">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1287d-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1287d-139">Return value</span></span>

<span data-ttu-id="1287d-140">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1287d-140">Type: **HRESULT**</span></span>

<span data-ttu-id="1287d-141">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="1287d-141">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="1287d-142">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="1287d-142">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="1287d-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="1287d-143">Remarks</span></span>

<span data-ttu-id="1287d-144">Um pacote de recursos sem esquema é aquele criado com o argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passado para [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou com a opção *omitSchemaFromResourcePacks* no arquivo de configuração PRI).</span><span class="sxs-lookup"><span data-stu-id="1287d-144">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="1287d-145">Para despejar um pacote de recursos sem esquema, passe o caminho para os dados PRI do pacote principal como o argumento para o parâmetro *schemaPriData* .</span><span class="sxs-lookup"><span data-stu-id="1287d-145">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriData* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1287d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1287d-146">Requirements</span></span>



| <span data-ttu-id="1287d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="1287d-147">Requirement</span></span> | <span data-ttu-id="1287d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="1287d-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1287d-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1287d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1287d-150">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="1287d-150">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1287d-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1287d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1287d-152">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="1287d-152">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1287d-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1287d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="1287d-154"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1287d-154"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="1287d-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1287d-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="1287d-156"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1287d-156"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="1287d-157">DLL</span><span class="sxs-lookup"><span data-stu-id="1287d-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1287d-158"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1287d-158"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1287d-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="1287d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1287d-160">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="1287d-160">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

