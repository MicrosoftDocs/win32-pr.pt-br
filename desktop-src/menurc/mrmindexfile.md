---
title: Função MrmIndexFile (MrmResourceIndexer. h)
description: Indexa um arquivo de recurso que pertence a um aplicativo UWP. Usa uma lista explícita (mas opcional) de qualificadores de recursos. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Menus de função MrmIndexFile e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455789"
---
# <a name="mrmindexfile-function"></a><span data-ttu-id="9c56b-106">Função MrmIndexFile</span><span class="sxs-lookup"><span data-stu-id="9c56b-106">MrmIndexFile function</span></span>

<span data-ttu-id="9c56b-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="9c56b-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9c56b-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="9c56b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9c56b-109">Indexa um arquivo de recurso que pertence a um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="9c56b-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="9c56b-110">Usa uma lista explícita (mas opcional) de qualificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c56b-110">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="9c56b-111">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="9c56b-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c56b-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c56b-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="9c56b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c56b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c56b-114">*indexador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c56b-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c56b-115">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="9c56b-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="9c56b-116">Um identificador que identifica o indexador de recursos que indexará o arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="9c56b-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="9c56b-117">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c56b-117">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c56b-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9c56b-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="9c56b-119">O URI de recurso a ser atribuído ao recurso.</span><span class="sxs-lookup"><span data-stu-id="9c56b-119">The resource URI to assign to the resource.</span></span> <span data-ttu-id="9c56b-120">O caminho será usado como o nome da subárvore do mapa de recursos para esse recurso quando você gerar posteriormente um arquivo PRI desse indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c56b-120">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="9c56b-121">*FilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c56b-121">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c56b-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9c56b-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="9c56b-123">Um caminho relativo para um arquivo que contém um recurso que você deseja indexar.</span><span class="sxs-lookup"><span data-stu-id="9c56b-123">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="9c56b-124">Esse caminho é relativo à raiz de projeto do aplicativo UWP para o qual você está gerando arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="9c56b-124">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="9c56b-125">Essa raiz do projeto é o valor de *projectRoot* que você passou para [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="9c56b-125">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c56b-126">*qualificadores* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9c56b-126">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c56b-127">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9c56b-127">Type: **PCWSTR**</span></span>

<span data-ttu-id="9c56b-128">Uma lista opcional de qualificadores de recursos, por exemplo, L "idioma-en-US \_ Scale-100 \_ contraste-Standard".</span><span class="sxs-lookup"><span data-stu-id="9c56b-128">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="9c56b-129">Uma cadeia de caracteres vazia ou **nullptr** indica um recurso neutro.</span><span class="sxs-lookup"><span data-stu-id="9c56b-129">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="9c56b-130">Os qualificadores de recursos *não* são inferidos de *ResourceURI* nem de *containerPath*.</span><span class="sxs-lookup"><span data-stu-id="9c56b-130">Resource qualifiers are *not* inferred from *resourceUri* nor from *containerPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c56b-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c56b-131">Return value</span></span>

<span data-ttu-id="9c56b-132">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c56b-132">Type: **HRESULT**</span></span>

<span data-ttu-id="9c56b-133">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="9c56b-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="9c56b-134">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="9c56b-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c56b-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c56b-135">Remarks</span></span>

<span data-ttu-id="9c56b-136">Se você quiser especificar quaisquer qualificadores de recursos, passe-os no parâmetro *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="9c56b-136">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="9c56b-137">Qualificadores de recursos *não* são inferidos de *ResourceURI* nem de *FilePath*.</span><span class="sxs-lookup"><span data-stu-id="9c56b-137">Resource qualifiers are *not* inferred from *resourceUri* nor from *filePath*.</span></span>

<span data-ttu-id="9c56b-138">O segmento de nome de arquivo de *ResourceURI* (não *FilePath*) é usado como o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9c56b-138">The file name segment of *resourceUri* (not *filePath*) is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c56b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c56b-139">Requirements</span></span>



| <span data-ttu-id="9c56b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c56b-140">Requirement</span></span> | <span data-ttu-id="9c56b-141">Valor</span><span class="sxs-lookup"><span data-stu-id="9c56b-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c56b-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c56b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9c56b-143">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="9c56b-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9c56b-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c56b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9c56b-145">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="9c56b-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9c56b-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c56b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c56b-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c56b-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="9c56b-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c56b-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c56b-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c56b-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="9c56b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9c56b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c56b-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c56b-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="9c56b-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c56b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c56b-153">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="9c56b-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

