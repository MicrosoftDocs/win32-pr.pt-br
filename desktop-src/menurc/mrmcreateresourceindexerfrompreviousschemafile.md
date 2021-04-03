---
title: Função MrmCreateResourceIndexerFromPreviousSchemaFile (MrmResourceIndexer. h)
description: Cria um indexador de recurso a partir de um arquivo de esquema criado com uma chamada anterior para MrmDumpPriFile. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Menus de função MrmCreateResourceIndexerFromPreviousSchemaFile e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 304e0aebe75ac416623cb1ec1053a7b6ae504194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645038"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a><span data-ttu-id="b7d1a-105">Função MrmCreateResourceIndexerFromPreviousSchemaFile</span><span class="sxs-lookup"><span data-stu-id="b7d1a-105">MrmCreateResourceIndexerFromPreviousSchemaFile function</span></span>

<span data-ttu-id="b7d1a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b7d1a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b7d1a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b7d1a-108">Cria um indexador de recurso a partir de um arquivo de esquema criado com uma chamada anterior para [**MrmDumpPriFile**](mrmdumpprifile.md).</span><span class="sxs-lookup"><span data-stu-id="b7d1a-108">Creates a resource indexer from a schema file created with a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span> <span data-ttu-id="b7d1a-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b7d1a-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d1a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7d1a-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="b7d1a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7d1a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d1a-112">*projectRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7d1a-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d1a-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b7d1a-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="b7d1a-114">A raiz do projeto do aplicativo UWP para o qual você irá gerar arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="b7d1a-115">Em outras palavras, o caminho para os arquivos de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="b7d1a-116">Especifique isso para que você possa especificar caminhos relativos a essa raiz em chamadas de API subsequentes para o mesmo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="b7d1a-117">*platformVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7d1a-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d1a-118">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="b7d1a-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="b7d1a-119">A versão da plataforma de destino para o indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="b7d1a-120">*Defaultqualifiers* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7d1a-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d1a-121">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b7d1a-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="b7d1a-122">Uma lista de qualificadores de recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="b7d1a-123">Por exemplo, L "idioma-en-US \_ escala-100 \_ contraste-padrão"</span><span class="sxs-lookup"><span data-stu-id="b7d1a-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="b7d1a-124">*esquema de esquemas* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7d1a-124">*schemaFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d1a-125">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b7d1a-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="b7d1a-126">Um caminho de arquivo completo para um arquivo de esquema criado por uma chamada anterior para [**MrmDumpPriFile**](mrmdumpprifile.md).</span><span class="sxs-lookup"><span data-stu-id="b7d1a-126">A full file path to a schema file created by a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7d1a-127">*indexador* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b7d1a-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d1a-128">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="b7d1a-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="b7d1a-129">Um ponteiro para um identificador de indexador de recurso.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d1a-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7d1a-130">Return value</span></span>

<span data-ttu-id="b7d1a-131">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b7d1a-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b7d1a-132">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="b7d1a-133">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="b7d1a-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d1a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7d1a-134">Requirements</span></span>



| <span data-ttu-id="b7d1a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d1a-135">Requirement</span></span> | <span data-ttu-id="b7d1a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="b7d1a-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d1a-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7d1a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d1a-138">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="b7d1a-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b7d1a-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7d1a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d1a-140">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="b7d1a-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7d1a-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7d1a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7d1a-142"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d1a-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="b7d1a-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7d1a-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7d1a-144"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7d1a-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="b7d1a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b7d1a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7d1a-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7d1a-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b7d1a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7d1a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d1a-148">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="b7d1a-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

