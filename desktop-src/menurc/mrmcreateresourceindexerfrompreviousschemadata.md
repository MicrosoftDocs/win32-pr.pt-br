---
title: Função MrmCreateResourceIndexerFromPreviousSchemaData (MrmResourceIndexer. h)
description: Cria um indexador de recursos de dados de esquema na memória criados com uma chamada anterior para MrmDumpPriFileInMemory ou MrmDumpPriDataInMemory.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Menus de função MrmCreateResourceIndexerFromPreviousSchemaData e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455292"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a><span data-ttu-id="f44eb-104">Função MrmCreateResourceIndexerFromPreviousSchemaData</span><span class="sxs-lookup"><span data-stu-id="f44eb-104">MrmCreateResourceIndexerFromPreviousSchemaData function</span></span>

<span data-ttu-id="f44eb-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f44eb-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f44eb-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f44eb-107">Cria um indexador de recursos de dados de esquema na memória criados com uma chamada anterior para [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) ou [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="f44eb-107">Creates a resource indexer from in-memory schema data created with a previous call to either [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="f44eb-108">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="f44eb-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="f44eb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f44eb-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="f44eb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f44eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f44eb-111">*projectRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-111">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44eb-112">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f44eb-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="f44eb-113">A raiz do projeto do aplicativo UWP para o qual você irá gerar arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="f44eb-113">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="f44eb-114">Em outras palavras, o caminho para os arquivos de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f44eb-114">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="f44eb-115">Especifique isso para que você possa especificar caminhos relativos a essa raiz em chamadas de API subsequentes para o mesmo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="f44eb-115">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="f44eb-116">*platformVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-116">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44eb-117">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="f44eb-117">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="f44eb-118">A versão da plataforma de destino para o indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="f44eb-118">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="f44eb-119">*Defaultqualifiers* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-119">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f44eb-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f44eb-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="f44eb-121">Uma lista de qualificadores de recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="f44eb-121">A list of default resource qualifiers.</span></span> <span data-ttu-id="f44eb-122">Por exemplo, L "idioma-en-US \_ escala-100 \_ contraste-padrão"</span><span class="sxs-lookup"><span data-stu-id="f44eb-122">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="f44eb-123">*schemaXmlData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-123">*schemaXmlData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44eb-124">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="f44eb-124">Type: \**BYTE\** _</span></span>

<span data-ttu-id="f44eb-125">Um ponteiro para dados de esquema criados por uma chamada anterior para [_ *MrmDumpPriFileInMemory* \*](mrmdumpprifileinmemory.md) ou [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="f44eb-125">A pointer to schema data created by a previous call to either [_ *MrmDumpPriFileInMemory*\*](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="f44eb-126">Não libere *schemaXmlData* até terminar de usar o indexador de recursos criado por essa função.</span><span class="sxs-lookup"><span data-stu-id="f44eb-126">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="f44eb-127">*schemaXmlSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-127">*schemaXmlSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44eb-128">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="f44eb-128">Type: **ULONG**</span></span>

<span data-ttu-id="f44eb-129">O tamanho dos dados apontados por *schemaXmlData*.</span><span class="sxs-lookup"><span data-stu-id="f44eb-129">The size of the data pointed to by *schemaXmlData*.</span></span>

</dd> <dt>

<span data-ttu-id="f44eb-130">*indexador* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-130">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f44eb-131">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f44eb-131">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="f44eb-132">Um ponteiro para um identificador de indexador de recurso.</span><span class="sxs-lookup"><span data-stu-id="f44eb-132">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f44eb-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f44eb-133">Return value</span></span>

<span data-ttu-id="f44eb-134">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f44eb-134">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f44eb-135">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="f44eb-135">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="f44eb-136">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="f44eb-136">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f44eb-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="f44eb-137">Remarks</span></span>

<span data-ttu-id="f44eb-138">Não libere *schemaXmlData* até terminar de usar o indexador de recursos criado por essa função.</span><span class="sxs-lookup"><span data-stu-id="f44eb-138">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f44eb-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f44eb-139">Requirements</span></span>



| <span data-ttu-id="f44eb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f44eb-140">Requirement</span></span> | <span data-ttu-id="f44eb-141">Valor</span><span class="sxs-lookup"><span data-stu-id="f44eb-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44eb-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f44eb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f44eb-143">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f44eb-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f44eb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f44eb-145">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="f44eb-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f44eb-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f44eb-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f44eb-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f44eb-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="f44eb-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f44eb-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="f44eb-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f44eb-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="f44eb-150">DLL</span><span class="sxs-lookup"><span data-stu-id="f44eb-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f44eb-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f44eb-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f44eb-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="f44eb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44eb-153">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="f44eb-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

