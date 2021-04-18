---
title: Função MrmIndexEmbeddedData (MrmResourceIndexer. h)
description: Indexa um único recurso embeddeddata que pertence a um aplicativo UWP.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- Menus de função MrmIndexEmbeddedData e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d08e0e125e7919ad3eb32e6cba2184356fce5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781001"
---
# <a name="mrmindexembeddeddata-function"></a><span data-ttu-id="90dd1-104">Função MrmIndexEmbeddedData</span><span class="sxs-lookup"><span data-stu-id="90dd1-104">MrmIndexEmbeddedData function</span></span>

<span data-ttu-id="90dd1-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="90dd1-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90dd1-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="90dd1-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90dd1-107">Indexa um único recurso **embeddeddata** que pertence a um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="90dd1-107">Indexes a single **embeddeddata** resource belonging to a UWP app.</span></span> <span data-ttu-id="90dd1-108">Usa uma lista explícita (mas opcional) de qualificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="90dd1-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="90dd1-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="90dd1-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="90dd1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90dd1-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="90dd1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90dd1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90dd1-112">*indexador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90dd1-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90dd1-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="90dd1-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="90dd1-114">Um identificador que identifica o indexador de recursos que indexará o arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="90dd1-114">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="90dd1-115">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90dd1-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90dd1-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="90dd1-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="90dd1-117">O URI de recurso a ser atribuído ao recurso.</span><span class="sxs-lookup"><span data-stu-id="90dd1-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="90dd1-118">O caminho será usado como o nome da subárvore do mapa de recursos para esse recurso quando você gerar posteriormente um arquivo PRI desse indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="90dd1-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="90dd1-119">*embeddedData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90dd1-119">*embeddedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90dd1-120">Tipo: \**const byte \** _</span><span class="sxs-lookup"><span data-stu-id="90dd1-120">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="90dd1-121">Um ponteiro para os dados do recurso que você deseja indexar.</span><span class="sxs-lookup"><span data-stu-id="90dd1-121">A pointer to the data of the resource that you want to index.</span></span>

</dd> <dt>

<span data-ttu-id="90dd1-122">_embeddedDataSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90dd1-122">_embeddedDataSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90dd1-123">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="90dd1-123">Type: **ULONG**</span></span>

<span data-ttu-id="90dd1-124">O tamanho dos dados apontados por *embeddedData*.</span><span class="sxs-lookup"><span data-stu-id="90dd1-124">The size of the data pointed to by *embeddedData*.</span></span>

</dd> <dt>

<span data-ttu-id="90dd1-125">*qualificadores* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="90dd1-125">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90dd1-126">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="90dd1-126">Type: **PCWSTR**</span></span>

<span data-ttu-id="90dd1-127">Uma lista opcional de qualificadores de recursos, por exemplo, L "idioma-en-US \_ Scale-100 \_ contraste-Standard".</span><span class="sxs-lookup"><span data-stu-id="90dd1-127">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="90dd1-128">Uma cadeia de caracteres vazia ou **nullptr** indica um recurso neutro.</span><span class="sxs-lookup"><span data-stu-id="90dd1-128">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="90dd1-129">Qualificadores de recursos *não* são inferidos de *ResourceURI*.</span><span class="sxs-lookup"><span data-stu-id="90dd1-129">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90dd1-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90dd1-130">Return value</span></span>

<span data-ttu-id="90dd1-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="90dd1-131">Type: **HRESULT**</span></span>

<span data-ttu-id="90dd1-132">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="90dd1-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="90dd1-133">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="90dd1-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="90dd1-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="90dd1-134">Remarks</span></span>

<span data-ttu-id="90dd1-135">Se você quiser especificar quaisquer qualificadores de recursos, passe-os no parâmetro *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="90dd1-135">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="90dd1-136">Qualificadores de recursos *não* são inferidos de *ResourceURI*.</span><span class="sxs-lookup"><span data-stu-id="90dd1-136">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="90dd1-137">O segmento de nome de arquivo de *ResourceURI* é usado como o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="90dd1-137">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="90dd1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90dd1-138">Requirements</span></span>



| <span data-ttu-id="90dd1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="90dd1-139">Requirement</span></span> | <span data-ttu-id="90dd1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="90dd1-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90dd1-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90dd1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="90dd1-142">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="90dd1-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="90dd1-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90dd1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="90dd1-144">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="90dd1-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="90dd1-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90dd1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="90dd1-146"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="90dd1-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="90dd1-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90dd1-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="90dd1-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90dd1-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="90dd1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="90dd1-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90dd1-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90dd1-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="90dd1-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="90dd1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90dd1-152">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="90dd1-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

