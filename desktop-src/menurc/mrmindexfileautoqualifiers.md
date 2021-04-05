---
title: Função MrmIndexFileAutoQualifiers (MrmResourceIndexer. h)
description: Indexa um arquivo de recurso que pertence a um aplicativo UWP. Infere uma lista de qualificadores de recursos do parâmetro filePath. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menus de função MrmIndexFileAutoQualifiers e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085219"
---
# <a name="mrmindexfileautoqualifiers-function"></a><span data-ttu-id="0b579-106">Função MrmIndexFileAutoQualifiers</span><span class="sxs-lookup"><span data-stu-id="0b579-106">MrmIndexFileAutoQualifiers function</span></span>

<span data-ttu-id="0b579-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0b579-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b579-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0b579-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b579-109">Indexa um arquivo de recurso que pertence a um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="0b579-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="0b579-110">Infere uma lista de qualificadores de recursos do parâmetro *FilePath* .</span><span class="sxs-lookup"><span data-stu-id="0b579-110">Infers a list of resource qualifiers from the *filePath* parameter.</span></span> <span data-ttu-id="0b579-111">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="0b579-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b579-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b579-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a><span data-ttu-id="0b579-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b579-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b579-114">*indexador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b579-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b579-115">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="0b579-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="0b579-116">Um identificador que identifica o indexador de recursos que indexará o arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="0b579-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="0b579-117">*FilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b579-117">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b579-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="0b579-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="0b579-119">Um caminho relativo para um arquivo que contém um recurso que você deseja indexar.</span><span class="sxs-lookup"><span data-stu-id="0b579-119">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="0b579-120">Esse caminho é relativo à raiz de projeto do aplicativo UWP para o qual você está gerando arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="0b579-120">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="0b579-121">Essa raiz do projeto é o valor de *projectRoot* que você passou para [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="0b579-121">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b579-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b579-122">Return value</span></span>

<span data-ttu-id="0b579-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0b579-123">Type: **HRESULT**</span></span>

<span data-ttu-id="0b579-124">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="0b579-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="0b579-125">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="0b579-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b579-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b579-126">Remarks</span></span>

<span data-ttu-id="0b579-127">O segmento de nome de arquivo de *FilePath* é usado como o nome do recurso; e qualificadores de recursos são derivados de seu caminho.</span><span class="sxs-lookup"><span data-stu-id="0b579-127">The file name segment of *filePath* is used as the resource name; and resource qualifiers are derived from its path.</span></span> <span data-ttu-id="0b579-128">Por exemplo, se você passar L "imagens \\ de-de" \\ escala-100 \\background.png "para *FilePath* , o indexador de recursos adicionará um recurso denominado" background.png "com qualificadores DE recursos" idioma-de-de "e" escala-100 ".</span><span class="sxs-lookup"><span data-stu-id="0b579-128">For example, if you pass L"Images\\de-DE\\scale-100\\background.png" to *filePath* then the resource indexer adds a resource named "background.png" with resource qualifiers "language-de-DE" and "scale-100".</span></span>

<span data-ttu-id="0b579-129">L "Files" será usado como o nome da subárvore do mapa de recursos para esse recurso quando você gerar posteriormente um arquivo PRI desse indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b579-129">L"Files" will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b579-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b579-130">Requirements</span></span>



| <span data-ttu-id="0b579-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b579-131">Requirement</span></span> | <span data-ttu-id="0b579-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0b579-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b579-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b579-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0b579-134">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="0b579-134">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0b579-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b579-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0b579-136">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="0b579-136">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0b579-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b579-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b579-138"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b579-138"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="0b579-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b579-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b579-140"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b579-140"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="0b579-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0b579-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b579-142"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b579-142"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0b579-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b579-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b579-144">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="0b579-144">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

