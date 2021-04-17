---
title: Função MrmDumpPriFileInMemory (MrmResourceIndexer. h)
description: Despeja um arquivo PRI (que é binário) para seu equivalente XML (como dados na memória), a fim de torná-lo mais fácil de ser lido.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menus de função MrmDumpPriFileInMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770437"
---
# <a name="mrmdumpprifileinmemory-function"></a><span data-ttu-id="e10a1-104">Função MrmDumpPriFileInMemory</span><span class="sxs-lookup"><span data-stu-id="e10a1-104">MrmDumpPriFileInMemory function</span></span>

<span data-ttu-id="e10a1-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="e10a1-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e10a1-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="e10a1-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e10a1-107">Despeja um arquivo PRI (que é binário) para seu equivalente XML (como dados na memória), a fim de torná-lo mais fácil de ser lido.</span><span class="sxs-lookup"><span data-stu-id="e10a1-107">Dumps a PRI file (which is binary) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="e10a1-108">A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="e10a1-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="e10a1-109">Chame [**MrmFreeMemory**](mrmfreememory.md) com o mesmo ponteiro para liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="e10a1-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="e10a1-110">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="e10a1-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="e10a1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e10a1-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="e10a1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e10a1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10a1-113">*indexFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e10a1-113">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10a1-114">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e10a1-114">Type: **PCWSTR**</span></span>

<span data-ttu-id="e10a1-115">Um caminho de arquivo completo para um arquivo PRI.</span><span class="sxs-lookup"><span data-stu-id="e10a1-115">A full file path to a PRI file.</span></span> <span data-ttu-id="e10a1-116">Esse é o arquivo PRI que será despejado em XML.</span><span class="sxs-lookup"><span data-stu-id="e10a1-116">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="e10a1-117">*schemaPriFile* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e10a1-117">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e10a1-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e10a1-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="e10a1-119">Um caminho de arquivo completo opcional para um arquivo de esquema (ou para um arquivo PRI que representa um esquema; consulte comentários).</span><span class="sxs-lookup"><span data-stu-id="e10a1-119">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="e10a1-120">*dumptype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e10a1-120">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10a1-121">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="e10a1-121">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="e10a1-122">Especifica o quão detalhado o despejo de XML deve ser ou se um esquema deve ser despejado.</span><span class="sxs-lookup"><span data-stu-id="e10a1-122">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="e10a1-123">*outputXmlData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e10a1-123">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e10a1-124">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="e10a1-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="e10a1-125">O endereço de um ponteiro para BYTE.</span><span class="sxs-lookup"><span data-stu-id="e10a1-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="e10a1-126">A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="e10a1-126">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="e10a1-127">Chame [**MrmFreeMemory**](mrmfreememory.md) com o ponteiro para byte para liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="e10a1-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="e10a1-128">*outputXmlSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e10a1-128">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e10a1-129">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="e10a1-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="e10a1-130">O endereço de um ULONG.</span><span class="sxs-lookup"><span data-stu-id="e10a1-130">The address of a ULONG.</span></span> <span data-ttu-id="e10a1-131">No _outputXmlSize \*, a função retorna o tamanho da memória alocada apontada por *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="e10a1-131">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10a1-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e10a1-132">Return value</span></span>

<span data-ttu-id="e10a1-133">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e10a1-133">Type: **HRESULT**</span></span>

<span data-ttu-id="e10a1-134">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="e10a1-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="e10a1-135">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="e10a1-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e10a1-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="e10a1-136">Remarks</span></span>

<span data-ttu-id="e10a1-137">Um pacote de recursos sem esquema é aquele criado com o argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passado para [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou com a opção *omitSchemaFromResourcePacks* no arquivo de configuração PRI).</span><span class="sxs-lookup"><span data-stu-id="e10a1-137">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="e10a1-138">Para despejar um pacote de recursos sem esquema, passe o caminho para os dados PRI do pacote principal como o argumento para o parâmetro *schemaPriFile* .</span><span class="sxs-lookup"><span data-stu-id="e10a1-138">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10a1-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e10a1-139">Requirements</span></span>



| <span data-ttu-id="e10a1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e10a1-140">Requirement</span></span> | <span data-ttu-id="e10a1-141">Valor</span><span class="sxs-lookup"><span data-stu-id="e10a1-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10a1-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e10a1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e10a1-143">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="e10a1-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e10a1-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e10a1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e10a1-145">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="e10a1-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e10a1-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e10a1-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e10a1-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="e10a1-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="e10a1-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e10a1-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="e10a1-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e10a1-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="e10a1-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e10a1-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e10a1-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e10a1-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e10a1-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="e10a1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10a1-153">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="e10a1-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

