---
title: Função MrmCreateResourceIndexer (MrmResourceIndexer. h)
description: Cria um indexador de recursos, usado para gerar arquivos de índice de recurso de pacote (PRI) para um aplicativo UWP. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Menus de função MrmCreateResourceIndexer e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369848"
---
# <a name="mrmcreateresourceindexer-function"></a><span data-ttu-id="1cdd6-105">Função MrmCreateResourceIndexer</span><span class="sxs-lookup"><span data-stu-id="1cdd6-105">MrmCreateResourceIndexer function</span></span>

<span data-ttu-id="1cdd6-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1cdd6-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1cdd6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1cdd6-108">Cria um indexador de recursos, usado para gerar arquivos de índice de recurso de pacote (PRI) para um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-108">Creates a resource indexer, used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="1cdd6-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="1cdd6-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cdd6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cdd6-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="1cdd6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cdd6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cdd6-112">*packageFamilyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cdd6-112">*packageFamilyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cdd6-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="1cdd6-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="1cdd6-114">O nome da família de pacotes do aplicativo UWP para o qual você irá gerar arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-114">The package family name of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="1cdd6-115">Esse valor será usado como o nome do mapa de recursos quando você gerar posteriormente um arquivo PRI desse indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-115">This value will be used as the resource map name when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="1cdd6-116">*projectRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cdd6-116">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cdd6-117">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="1cdd6-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="1cdd6-118">A raiz do projeto do aplicativo UWP para o qual você irá gerar arquivos PRI.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-118">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="1cdd6-119">Em outras palavras, o caminho para os arquivos de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-119">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="1cdd6-120">Especifique isso para que você possa especificar caminhos relativos a essa raiz em chamadas de API subsequentes para o mesmo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-120">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="1cdd6-121">*platformVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cdd6-121">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cdd6-122">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="1cdd6-122">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="1cdd6-123">A versão da plataforma de destino para o indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-123">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="1cdd6-124">*Defaultqualifiers* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1cdd6-124">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cdd6-125">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="1cdd6-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="1cdd6-126">Uma lista de qualificadores de recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-126">A list of default resource qualifiers.</span></span> <span data-ttu-id="1cdd6-127">Por exemplo, L "idioma-en-US \_ escala-100 \_ contraste-padrão"</span><span class="sxs-lookup"><span data-stu-id="1cdd6-127">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="1cdd6-128">*indexador* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1cdd6-128">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cdd6-129">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="1cdd6-129">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="1cdd6-130">Um ponteiro para um identificador de indexador de recurso.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-130">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cdd6-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cdd6-131">Return value</span></span>

<span data-ttu-id="1cdd6-132">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1cdd6-132">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1cdd6-133">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="1cdd6-134">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="1cdd6-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cdd6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cdd6-135">Requirements</span></span>



| <span data-ttu-id="1cdd6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cdd6-136">Requirement</span></span> | <span data-ttu-id="1cdd6-137">Valor</span><span class="sxs-lookup"><span data-stu-id="1cdd6-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cdd6-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cdd6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1cdd6-139">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="1cdd6-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1cdd6-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cdd6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1cdd6-141">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="1cdd6-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1cdd6-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cdd6-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cdd6-143"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cdd6-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="1cdd6-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cdd6-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cdd6-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cdd6-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="1cdd6-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1cdd6-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cdd6-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cdd6-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1cdd6-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cdd6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cdd6-149">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="1cdd6-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

