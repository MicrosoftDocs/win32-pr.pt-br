---
title: Função MrmIndexString (MrmResourceIndexer. h)
description: Indexa um único recurso de cadeia de caracteres que pertence a um aplicativo UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Menus de função MrmIndexString e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085218"
---
# <a name="mrmindexstring-function"></a><span data-ttu-id="bbaed-104">Função MrmIndexString</span><span class="sxs-lookup"><span data-stu-id="bbaed-104">MrmIndexString function</span></span>

<span data-ttu-id="bbaed-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="bbaed-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bbaed-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="bbaed-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bbaed-107">Indexa um único recurso de cadeia de caracteres que pertence a um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="bbaed-107">Indexes a single string resource belonging to a UWP app.</span></span> <span data-ttu-id="bbaed-108">Usa uma lista explícita (mas opcional) de qualificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbaed-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="bbaed-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="bbaed-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="bbaed-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbaed-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="bbaed-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbaed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbaed-112">*indexador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaed-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaed-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="bbaed-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="bbaed-114">Um identificador que identifica o indexador de recursos que indexará os recursos de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bbaed-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="bbaed-115">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaed-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaed-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bbaed-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="bbaed-117">O URI de recurso a ser atribuído ao recurso.</span><span class="sxs-lookup"><span data-stu-id="bbaed-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="bbaed-118">O caminho será usado como o nome da subárvore do mapa de recursos para esse recurso quando você gerar posteriormente um arquivo PRI desse indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbaed-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="bbaed-119">*origemstring* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaed-119">*resourceString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaed-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bbaed-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="bbaed-121">O valor do recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bbaed-121">The value of the string resource.</span></span>

</dd> <dt>

<span data-ttu-id="bbaed-122">*qualificadores* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bbaed-122">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaed-123">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bbaed-123">Type: **PCWSTR**</span></span>

<span data-ttu-id="bbaed-124">Uma lista opcional de qualificadores de recursos, por exemplo, L "idioma-en-US \_ Scale-100 \_ contraste-Standard".</span><span class="sxs-lookup"><span data-stu-id="bbaed-124">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="bbaed-125">Uma cadeia de caracteres vazia ou **nullptr** indica um recurso neutro.</span><span class="sxs-lookup"><span data-stu-id="bbaed-125">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="bbaed-126">Qualificadores de recursos *não* são inferidos de *ResourceURI*.</span><span class="sxs-lookup"><span data-stu-id="bbaed-126">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbaed-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbaed-127">Return value</span></span>

<span data-ttu-id="bbaed-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bbaed-128">Type: **HRESULT**</span></span>

<span data-ttu-id="bbaed-129">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="bbaed-129">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="bbaed-130">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="bbaed-130">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbaed-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbaed-131">Remarks</span></span>

<span data-ttu-id="bbaed-132">Se você quiser especificar quaisquer qualificadores de recursos, passe-os no parâmetro *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="bbaed-132">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="bbaed-133">Qualificadores de recursos *não* são inferidos de *ResourceURI*.</span><span class="sxs-lookup"><span data-stu-id="bbaed-133">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="bbaed-134">O segmento de nome de arquivo de *ResourceURI* é usado como o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bbaed-134">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbaed-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbaed-135">Requirements</span></span>



| <span data-ttu-id="bbaed-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbaed-136">Requirement</span></span> | <span data-ttu-id="bbaed-137">Valor</span><span class="sxs-lookup"><span data-stu-id="bbaed-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbaed-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbaed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bbaed-139">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="bbaed-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bbaed-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbaed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bbaed-141">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="bbaed-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bbaed-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbaed-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbaed-143"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbaed-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="bbaed-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bbaed-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="bbaed-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbaed-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="bbaed-146">DLL</span><span class="sxs-lookup"><span data-stu-id="bbaed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbaed-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbaed-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bbaed-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbaed-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbaed-149">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="bbaed-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

