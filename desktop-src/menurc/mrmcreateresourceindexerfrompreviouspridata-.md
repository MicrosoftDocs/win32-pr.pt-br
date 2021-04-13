---
title: Função MrmCreateResourceIndexerFromPreviousPriData (MrmResourceIndexer. h)
description: Cria um indexador de recursos por meio de dados PRI criados por uma chamada anterior para MrmCreateResourceFileInMemory. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- Menus de função MrmCreateResourceIndexerFromPreviousPriData e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152ded28e6158fb80d8157c751026091afb51f65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295850"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a><span data-ttu-id="23b45-105">Função MrmCreateResourceIndexerFromPreviousPriData</span><span class="sxs-lookup"><span data-stu-id="23b45-105">MrmCreateResourceIndexerFromPreviousPriData function</span></span>

<span data-ttu-id="23b45-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="23b45-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="23b45-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="23b45-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="23b45-108">Cria um indexador de recursos por meio de dados PRI criados por uma chamada anterior para [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="23b45-108">Creates a resource indexer from PRI data created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="23b45-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="23b45-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="23b45-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23b45-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="23b45-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23b45-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b45-112">*projectRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23b45-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b45-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="23b45-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="23b45-114">A raiz do projeto do aplicativo UWP para o qual você irá gerar arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="23b45-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="23b45-115">Em outras palavras, o caminho para os arquivos de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23b45-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="23b45-116">Especifique isso para que você possa especificar caminhos relativos a essa raiz em chamadas de API subsequentes para o mesmo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="23b45-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="23b45-117">*platformVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23b45-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b45-118">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="23b45-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="23b45-119">A versão da plataforma de destino para o indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="23b45-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="23b45-120">*Defaultqualifiers* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="23b45-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="23b45-121">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="23b45-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="23b45-122">Uma lista de qualificadores de recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="23b45-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="23b45-123">Por exemplo, L "idioma-en-US \_ escala-100 \_ contraste-padrão"</span><span class="sxs-lookup"><span data-stu-id="23b45-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="23b45-124">*priData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23b45-124">*priData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b45-125">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="23b45-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="23b45-126">Um ponteiro para dados PRI criados por uma chamada anterior para [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="23b45-126">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="23b45-127">Não libere *priData* até terminar de usar o indexador de recursos criado por essa função.</span><span class="sxs-lookup"><span data-stu-id="23b45-127">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="23b45-128">*priSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23b45-128">*priSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b45-129">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="23b45-129">Type: **ULONG**</span></span>

<span data-ttu-id="23b45-130">O tamanho dos dados apontados por *priData*.</span><span class="sxs-lookup"><span data-stu-id="23b45-130">The size of the data pointed to by *priData*.</span></span>

</dd> <dt>

<span data-ttu-id="23b45-131">*indexador* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="23b45-131">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="23b45-132">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="23b45-132">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="23b45-133">Um ponteiro para um identificador de indexador de recurso.</span><span class="sxs-lookup"><span data-stu-id="23b45-133">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b45-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23b45-134">Return value</span></span>

<span data-ttu-id="23b45-135">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="23b45-135">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="23b45-136">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="23b45-136">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="23b45-137">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="23b45-137">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="23b45-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="23b45-138">Remarks</span></span>

<span data-ttu-id="23b45-139">Não libere *priData* até terminar de usar o indexador de recursos criado por essa função.</span><span class="sxs-lookup"><span data-stu-id="23b45-139">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="23b45-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23b45-140">Requirements</span></span>



| <span data-ttu-id="23b45-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b45-141">Requirement</span></span> | <span data-ttu-id="23b45-142">Valor</span><span class="sxs-lookup"><span data-stu-id="23b45-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23b45-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b45-143">Minimum supported client</span></span><br/> | <span data-ttu-id="23b45-144">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="23b45-144">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="23b45-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b45-145">Minimum supported server</span></span><br/> | <span data-ttu-id="23b45-146">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="23b45-146">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="23b45-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23b45-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b45-148"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="23b45-148"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="23b45-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23b45-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="23b45-150"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23b45-150"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="23b45-151">DLL</span><span class="sxs-lookup"><span data-stu-id="23b45-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b45-152"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b45-152"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="23b45-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="23b45-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b45-154">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="23b45-154">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

