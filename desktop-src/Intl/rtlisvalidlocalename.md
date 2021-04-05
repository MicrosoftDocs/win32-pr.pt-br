---
description: Determina se uma localidade especificada pelo nome está instalada ou tem suporte no sistema operacional.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Função RtlIsValidLocaleName (Ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827056"
---
# <a name="rtlisvalidlocalename-function"></a><span data-ttu-id="f33e5-103">Função RtlIsValidLocaleName</span><span class="sxs-lookup"><span data-stu-id="f33e5-103">RtlIsValidLocaleName function</span></span>

<span data-ttu-id="f33e5-104">Determina se uma localidade especificada pelo nome está instalada ou tem suporte no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f33e5-104">Determines if a locale specified by name is installed or supported on the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="f33e5-105">Essa função está disponível para uso somente no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f33e5-105">This function is available for use in Windows Vista only.</span></span> <span data-ttu-id="f33e5-106">Ele pode ser alterado ou indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f33e5-106">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f33e5-107">Os aplicativos devem usar o [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="f33e5-107">Applications should use [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f33e5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f33e5-108">Syntax</span></span>


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a><span data-ttu-id="f33e5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f33e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f33e5-110">*Localename* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f33e5-110">*LocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f33e5-111">[Nome da localidade](locale-names.md) para validar.</span><span class="sxs-lookup"><span data-stu-id="f33e5-111">[Locale name](locale-names.md) to validate.</span></span> <span data-ttu-id="f33e5-112">Esse parâmetro pode especificar o nome de uma [localidade personalizada](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="f33e5-112">This parameter can specify the name of a [custom locale](custom-locales.md).</span></span>

</dd> <dt>

<span data-ttu-id="f33e5-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="f33e5-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f33e5-114">Sinalizadores que indicam se as localidades neutras são consideradas válidas.</span><span class="sxs-lookup"><span data-stu-id="f33e5-114">Flags indicating if neutral locales are considered valid.</span></span> <span data-ttu-id="f33e5-115">Atualmente, o único sinalizador definido é a [localidade \_ permitir \_ neutro](locale-allow-neutral.md).</span><span class="sxs-lookup"><span data-stu-id="f33e5-115">Currently the only defined flag is [LOCALE\_ALLOW\_NEUTRAL](locale-allow-neutral.md).</span></span> <span data-ttu-id="f33e5-116">O valor padrão é que eles não são.</span><span class="sxs-lookup"><span data-stu-id="f33e5-116">The default value is that they are not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f33e5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f33e5-117">Return value</span></span>

<span data-ttu-id="f33e5-118">Retorna um valor diferente de zero se for bem-sucedido ou 0 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f33e5-118">Returns a nonzero value if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f33e5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f33e5-119">Remarks</span></span>

<span data-ttu-id="f33e5-120">Essa função é semelhante a [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="f33e5-120">This function is similar to [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span> <span data-ttu-id="f33e5-121">A única diferença é que, se \_ a localidade permitir \_ neutro for definida, **RtlIsValidLocaleName** retornará **true** para um nome que corresponda a uma localidade neutra (como "en"), enquanto [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) retorna **true** somente para uma localidade específica (como "en-US").</span><span class="sxs-lookup"><span data-stu-id="f33e5-121">The only difference is that if LOCALE\_ALLOW\_NEUTRAL is set, **RtlIsValidLocaleName** returns **TRUE** for a name that corresponds to a neutral locale (such as "en"), while [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) returns **TRUE** only for a specific locale (such as "en-US").</span></span> <span data-ttu-id="f33e5-122">As localidades neutras são usadas como parte da estratégia de carregamento de recursos no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="f33e5-122">Neutral locales are used as part of the resource loading strategy in Windows Vista and later.</span></span> <span data-ttu-id="f33e5-123">Apenas uma pequena classe de aplicativos altamente especializados usa **RtlIsValidLocaleName** e define a \_ localidade \_ como neutra, pois as localidades neutras são de uso muito limitado.</span><span class="sxs-lookup"><span data-stu-id="f33e5-123">Only a small class of highly specialized applications use **RtlIsValidLocaleName** and set LOCALE\_ALLOW\_NEUTRAL, because neutral locales are of very limited use.</span></span> <span data-ttu-id="f33e5-124">Nenhuma das funções descritas na [chamada das funções "nome de localidade"](calling-the--locale-name--functions.md) aceita localidades neutras como entradas.</span><span class="sxs-lookup"><span data-stu-id="f33e5-124">None of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33e5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f33e5-125">Requirements</span></span>



| <span data-ttu-id="f33e5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f33e5-126">Requirement</span></span> | <span data-ttu-id="f33e5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f33e5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f33e5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f33e5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f33e5-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f33e5-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f33e5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f33e5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f33e5-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f33e5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f33e5-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f33e5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f33e5-133"><dt>Ntrtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f33e5-133"><dt>Ntrtl.h</dt></span></span> </dl>      |
| <span data-ttu-id="f33e5-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f33e5-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f33e5-135"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f33e5-135"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f33e5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f33e5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f33e5-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f33e5-137"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33e5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f33e5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33e5-139">Suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="f33e5-139">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="f33e5-140">Funções de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="f33e5-140">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="f33e5-141">**IsValidLocaleName**</span><span class="sxs-lookup"><span data-stu-id="f33e5-141">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




