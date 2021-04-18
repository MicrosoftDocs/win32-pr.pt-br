---
title: Função MrmCreateResourceIndexerFromPreviousPriFile (MrmResourceIndexer. h)
description: Cria um indexador de recurso a partir de um arquivo PRI criado com uma chamada anterior para MrmCreateResourceFile. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Menus de função MrmCreateResourceIndexerFromPreviousPriFile e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08170dc8ae25db34492273e7c612352d5e0530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753310"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a><span data-ttu-id="7a5d5-105">Função MrmCreateResourceIndexerFromPreviousPriFile</span><span class="sxs-lookup"><span data-stu-id="7a5d5-105">MrmCreateResourceIndexerFromPreviousPriFile function</span></span>

<span data-ttu-id="7a5d5-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7a5d5-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7a5d5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7a5d5-108">Cria um indexador de recurso a partir de um arquivo PRI criado com uma chamada anterior para [**MrmCreateResourceFile**](mrmcreateresourcefile.md).</span><span class="sxs-lookup"><span data-stu-id="7a5d5-108">Creates a resource indexer from a PRI file created with a previous call to [**MrmCreateResourceFile**](mrmcreateresourcefile.md).</span></span> <span data-ttu-id="7a5d5-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="7a5d5-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5d5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a5d5-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   priFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="7a5d5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a5d5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5d5-112">*projectRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a5d5-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5d5-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7a5d5-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="7a5d5-114">A raiz do projeto do aplicativo UWP para o qual você irá gerar arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="7a5d5-115">Em outras palavras, o caminho para os arquivos de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="7a5d5-116">Especifique isso para que você possa especificar caminhos relativos a essa raiz em chamadas de API subsequentes para o mesmo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="7a5d5-117">*platformVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a5d5-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5d5-118">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="7a5d5-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="7a5d5-119">A versão da plataforma de destino para o indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="7a5d5-120">*Defaultqualifiers* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7a5d5-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5d5-121">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7a5d5-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="7a5d5-122">Uma lista de qualificadores de recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="7a5d5-123">Por exemplo, L "idioma-en-US \_ escala-100 \_ contraste-padrão"</span><span class="sxs-lookup"><span data-stu-id="7a5d5-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="7a5d5-124">*priFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a5d5-124">*priFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5d5-125">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7a5d5-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="7a5d5-126">Um caminho de arquivo completo para um arquivo PRI.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-126">A full file path to a PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="7a5d5-127">*indexador* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7a5d5-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5d5-128">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="7a5d5-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="7a5d5-129">Um ponteiro para um identificador de indexador de recurso.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5d5-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a5d5-130">Return value</span></span>

<span data-ttu-id="7a5d5-131">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="7a5d5-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="7a5d5-132">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="7a5d5-133">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="7a5d5-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a5d5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a5d5-134">Requirements</span></span>



| <span data-ttu-id="7a5d5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a5d5-135">Requirement</span></span> | <span data-ttu-id="7a5d5-136">Valor</span><span class="sxs-lookup"><span data-stu-id="7a5d5-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5d5-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a5d5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5d5-138">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="7a5d5-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7a5d5-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a5d5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5d5-140">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="7a5d5-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a5d5-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a5d5-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a5d5-142"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a5d5-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="7a5d5-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a5d5-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a5d5-144"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a5d5-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="7a5d5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7a5d5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a5d5-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a5d5-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7a5d5-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a5d5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5d5-148">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="7a5d5-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

