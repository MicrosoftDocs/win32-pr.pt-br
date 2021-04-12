---
title: Função MrmCreateConfigInMemory (MrmResourceIndexer. h)
description: Cria novas informações de configuração PRI inicializadas (como dados na memória, não como um arquivo) definindo os padrões de qualificador que você especificar.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Menus de função MrmCreateConfigInMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499680"
---
# <a name="mrmcreateconfiginmemory-function"></a><span data-ttu-id="38142-104">Função MrmCreateConfigInMemory</span><span class="sxs-lookup"><span data-stu-id="38142-104">MrmCreateConfigInMemory function</span></span>

<span data-ttu-id="38142-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="38142-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="38142-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="38142-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="38142-107">Cria novas informações de configuração PRI inicializadas (como dados na memória, não como um arquivo) definindo os padrões de qualificador que você especificar.</span><span class="sxs-lookup"><span data-stu-id="38142-107">Creates new, initialized PRI configuration info (as in-memory data, not as a file) defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="38142-108">A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="38142-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="38142-109">Chame [**MrmFreeMemory**](mrmfreememory.md) com o mesmo ponteiro para liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="38142-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="38142-110">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="38142-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="38142-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38142-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="38142-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38142-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38142-113">*platformVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38142-113">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38142-114">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="38142-114">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="38142-115">A versão da plataforma (*targetOsVersion*) a ser usada para as informações de configuração geradas.</span><span class="sxs-lookup"><span data-stu-id="38142-115">The platform version (*targetOsVersion*) to use for the generated configuration info.</span></span>

</dd> <dt>

<span data-ttu-id="38142-116">*Defaultqualifiers* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="38142-116">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38142-117">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="38142-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="38142-118">Uma lista de qualificadores de recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="38142-118">A list of default resource qualifiers.</span></span> <span data-ttu-id="38142-119">Por exemplo, L "idioma-en-US \_ escala-100 \_ contraste-padrão"</span><span class="sxs-lookup"><span data-stu-id="38142-119">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="38142-120">*outputXmlData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38142-120">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38142-121">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="38142-121">Type: **BYTE\*\***</span></span>

<span data-ttu-id="38142-122">O endereço de um ponteiro para BYTE.</span><span class="sxs-lookup"><span data-stu-id="38142-122">The address of a pointer to BYTE.</span></span> <span data-ttu-id="38142-123">A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="38142-123">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="38142-124">Chame [**MrmFreeMemory**](mrmfreememory.md) com o ponteiro para byte para liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="38142-124">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="38142-125">*outputXmlSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38142-125">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38142-126">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="38142-126">Type: \**ULONG\** _</span></span>

<span data-ttu-id="38142-127">O endereço de um ULONG.</span><span class="sxs-lookup"><span data-stu-id="38142-127">The address of a ULONG.</span></span> <span data-ttu-id="38142-128">No _outputXmlSize \*, a função retorna o tamanho da memória alocada apontada por *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="38142-128">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38142-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38142-129">Return value</span></span>

<span data-ttu-id="38142-130">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="38142-130">Type: **HRESULT**</span></span>

<span data-ttu-id="38142-131">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="38142-131">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="38142-132">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="38142-132">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="38142-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38142-133">Requirements</span></span>



| <span data-ttu-id="38142-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="38142-134">Requirement</span></span> | <span data-ttu-id="38142-135">Valor</span><span class="sxs-lookup"><span data-stu-id="38142-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38142-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38142-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38142-137">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="38142-137">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="38142-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38142-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38142-139">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="38142-139">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="38142-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38142-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="38142-141"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="38142-141"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="38142-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38142-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="38142-143"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38142-143"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="38142-144">DLL</span><span class="sxs-lookup"><span data-stu-id="38142-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38142-145"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38142-145"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="38142-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="38142-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38142-147">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="38142-147">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

