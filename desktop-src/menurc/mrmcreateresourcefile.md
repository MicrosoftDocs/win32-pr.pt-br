---
title: Função MrmCreateResourceFile (MrmResourceIndexer. h)
description: Cria um arquivo PRI (denominado \ 0034; Resources. pri \ 0034;), ou arquivos, no disco na pasta especificada. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Menus de função MrmCreateResourceFile e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645040"
---
# <a name="mrmcreateresourcefile-function"></a><span data-ttu-id="ca731-105">Função MrmCreateResourceFile</span><span class="sxs-lookup"><span data-stu-id="ca731-105">MrmCreateResourceFile function</span></span>

<span data-ttu-id="ca731-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="ca731-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ca731-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="ca731-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ca731-108">Cria um arquivo PRI (chamado "Resources. pri"), ou arquivos, no disco na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="ca731-108">Creates a PRI file (named "resources.pri"), or files, on disk in the specified folder.</span></span> <span data-ttu-id="ca731-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="ca731-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca731-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca731-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="ca731-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca731-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca731-112">*indexador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca731-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca731-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="ca731-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="ca731-114">Um identificador que identifica o indexador de recursos do qual criar o arquivo PRI.</span><span class="sxs-lookup"><span data-stu-id="ca731-114">A handle identifying the resource indexer from which to create the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="ca731-115">*packagmode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca731-115">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca731-116">Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="ca731-116">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="ca731-117">Especifica se o arquivo PRI deve ser autônomo, ser dividido automaticamente pelo qualificador de recursos ou ser um pacote de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca731-117">Specifies whether the PRI file should be standalone, be automatically split by resource qualifier, or be a resource pack.</span></span>

</dd> <dt>

<span data-ttu-id="ca731-118">*packagoptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca731-118">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca731-119">Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="ca731-119">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="ca731-120">Especifica opções adicionais sobre o arquivo PRI.</span><span class="sxs-lookup"><span data-stu-id="ca731-120">Specifies additional options about the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="ca731-121">*outputDirectory*</span><span class="sxs-lookup"><span data-stu-id="ca731-121">*outputDirectory*</span></span> 
</dt> <dd>

<span data-ttu-id="ca731-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ca731-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="ca731-123">Um caminho para uma pasta na qual salvar o arquivo PRI.</span><span class="sxs-lookup"><span data-stu-id="ca731-123">A path to a folder in which to save the PRI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca731-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca731-124">Return value</span></span>

<span data-ttu-id="ca731-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ca731-125">Type: **HRESULT**</span></span>

<span data-ttu-id="ca731-126">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="ca731-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="ca731-127">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="ca731-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca731-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca731-128">Requirements</span></span>



| <span data-ttu-id="ca731-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca731-129">Requirement</span></span> | <span data-ttu-id="ca731-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ca731-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca731-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca731-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ca731-132">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="ca731-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ca731-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca731-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ca731-134">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="ca731-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca731-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca731-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca731-136"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca731-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="ca731-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca731-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca731-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca731-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="ca731-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ca731-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca731-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca731-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ca731-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca731-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca731-142">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="ca731-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

