---
title: Função MrmIndexResourceContainerAutoQualifiers (MrmResourceIndexer. h)
description: Indexa os recursos de cadeia de caracteres contidos dentro de um arquivo de recursos (. resw/. resjson) ou um. priinfo ou. prifile, pertencente a um aplicativo UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menus de função MrmIndexResourceContainerAutoQualifiers e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812324"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a><span data-ttu-id="7d6c0-104">Função MrmIndexResourceContainerAutoQualifiers</span><span class="sxs-lookup"><span data-stu-id="7d6c0-104">MrmIndexResourceContainerAutoQualifiers function</span></span>

<span data-ttu-id="7d6c0-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7d6c0-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7d6c0-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7d6c0-107">Indexa os recursos de cadeia de caracteres contidos dentro de um arquivo de recursos (. resw/. resjson) ou um. priinfo ou. prifile, pertencente a um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-107">Indexes the string resources contained inside a Resources File (.resw/.resjson), or a .priinfo or .prifile, belonging to a UWP app.</span></span> <span data-ttu-id="7d6c0-108">Infere uma lista de qualificadores de recursos do parâmetro *containerPath* .</span><span class="sxs-lookup"><span data-stu-id="7d6c0-108">Infers a list of resource qualifiers from the *containerPath* parameter.</span></span> <span data-ttu-id="7d6c0-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="7d6c0-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6c0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d6c0-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a><span data-ttu-id="7d6c0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d6c0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6c0-112">*indexador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7d6c0-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6c0-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="7d6c0-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="7d6c0-114">Um identificador que identifica o indexador de recursos que indexará os recursos de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="7d6c0-115">*containerPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7d6c0-115">*containerPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6c0-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d6c0-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="7d6c0-117">Um caminho relativo para um. resw,. resjson,. priinfo ou. prifile que contém recursos de cadeia de caracteres que você deseja indexar.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-117">A relative path to a .resw, .resjson, .priinfo, or .prifile containing string resources that you want to index.</span></span> <span data-ttu-id="7d6c0-118">Esse caminho é relativo à raiz de projeto do aplicativo UWP para o qual você está gerando arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-118">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="7d6c0-119">Essa raiz do projeto é o valor de *projectRoot* que você passou para [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="7d6c0-119">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6c0-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d6c0-120">Return value</span></span>

<span data-ttu-id="7d6c0-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7d6c0-121">Type: **HRESULT**</span></span>

<span data-ttu-id="7d6c0-122">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-122">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="7d6c0-123">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-123">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d6c0-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d6c0-124">Remarks</span></span>

<span data-ttu-id="7d6c0-125">Os qualificadores de recursos são inferidos de *containerPath*.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-125">Resource qualifiers are inferred from *containerPath*.</span></span> <span data-ttu-id="7d6c0-126">Por exemplo, um valor de L "en-US \\ \\ Resources. resw" adiciona recursos de cadeia de caracteres com o qualificador "Language-en-US".</span><span class="sxs-lookup"><span data-stu-id="7d6c0-126">For example, a value of L"en-US\\\\resources.resw" adds string resources with the qualifier "language-en-US".</span></span>

<span data-ttu-id="7d6c0-127">O nome do arquivo de recursos será usado como o nome da subárvore do mapa de recursos para esses recursos quando você gerar posteriormente um arquivo PRI desse indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-127">The name of the Resources File will be used as the resource map subtree name for these resources when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d6c0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d6c0-128">Requirements</span></span>



| <span data-ttu-id="7d6c0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d6c0-129">Requirement</span></span> | <span data-ttu-id="7d6c0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7d6c0-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6c0-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d6c0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7d6c0-132">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="7d6c0-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7d6c0-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d6c0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7d6c0-134">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="7d6c0-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7d6c0-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d6c0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d6c0-136"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d6c0-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="7d6c0-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d6c0-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="7d6c0-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d6c0-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="7d6c0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7d6c0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d6c0-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d6c0-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7d6c0-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d6c0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6c0-142">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="7d6c0-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

