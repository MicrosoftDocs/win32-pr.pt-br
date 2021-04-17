---
title: Função MrmCreateConfig (MrmResourceIndexer. h)
description: Cria um novo arquivo de configuração PRI inicializado definindo os padrões de qualificador que você especificar. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- Menus de função MrmCreateConfig e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3adb270d9bbd9194822181314a697fa1d267a127
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755143"
---
# <a name="mrmcreateconfig-function"></a><span data-ttu-id="485a3-105">Função MrmCreateConfig</span><span class="sxs-lookup"><span data-stu-id="485a3-105">MrmCreateConfig function</span></span>

<span data-ttu-id="485a3-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="485a3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="485a3-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="485a3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="485a3-108">Cria um novo arquivo de configuração PRI inicializado definindo os padrões de qualificador que você especificar.</span><span class="sxs-lookup"><span data-stu-id="485a3-108">Creates a new, initialized PRI config file defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="485a3-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="485a3-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="485a3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="485a3-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="485a3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="485a3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="485a3-112">*platformVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="485a3-112">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485a3-113">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="485a3-113">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="485a3-114">A versão da plataforma (*targetOsVersion*) a ser usada para o arquivo de configuração gerado.</span><span class="sxs-lookup"><span data-stu-id="485a3-114">The platform version (*targetOsVersion*) to use for the generated configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="485a3-115">*Defaultqualifiers* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="485a3-115">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="485a3-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="485a3-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="485a3-117">Uma lista de qualificadores de recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="485a3-117">A list of default resource qualifiers.</span></span> <span data-ttu-id="485a3-118">Por exemplo, L "idioma-en-US \_ escala-100 \_ contraste-padrão"</span><span class="sxs-lookup"><span data-stu-id="485a3-118">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="485a3-119">*outputXmlFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="485a3-119">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485a3-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="485a3-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="485a3-121">O caminho do arquivo de configuração a ser criado.</span><span class="sxs-lookup"><span data-stu-id="485a3-121">The path of the configuration file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="485a3-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="485a3-122">Return value</span></span>

<span data-ttu-id="485a3-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="485a3-123">Type: **HRESULT**</span></span>

<span data-ttu-id="485a3-124">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="485a3-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="485a3-125">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="485a3-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="485a3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="485a3-126">Requirements</span></span>



| <span data-ttu-id="485a3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="485a3-127">Requirement</span></span> | <span data-ttu-id="485a3-128">Valor</span><span class="sxs-lookup"><span data-stu-id="485a3-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="485a3-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="485a3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="485a3-130">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="485a3-130">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="485a3-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="485a3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="485a3-132">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="485a3-132">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="485a3-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="485a3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="485a3-134"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="485a3-134"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="485a3-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="485a3-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="485a3-136"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="485a3-136"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="485a3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="485a3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="485a3-138"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="485a3-138"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="485a3-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="485a3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485a3-140">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="485a3-140">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

