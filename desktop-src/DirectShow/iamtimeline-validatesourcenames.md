---
description: O método ValidateSourceNames valida nomes de origem na linha do tempo, usando o localizador de mídia. Opcionalmente, esse método também atualiza qualquer objeto de origem para o qual ele localiza um arquivo.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'Método IAMTimeline:: ValidateSourceNames (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787143"
---
# <a name="iamtimelinevalidatesourcenames-method"></a><span data-ttu-id="53195-104">Método IAMTimeline:: ValidateSourceNames</span><span class="sxs-lookup"><span data-stu-id="53195-104">IAMTimeline::ValidateSourceNames method</span></span>

> [!Note]  
> <span data-ttu-id="53195-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="53195-105">\[Deprecated.</span></span> <span data-ttu-id="53195-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53195-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53195-107">O `ValidateSourceNames` método valida os nomes de origem na linha do tempo, usando o localizador de mídia.</span><span class="sxs-lookup"><span data-stu-id="53195-107">The `ValidateSourceNames` method validates source names in the timeline, using the media locator.</span></span> <span data-ttu-id="53195-108">Opcionalmente, esse método também atualiza qualquer objeto de origem para o qual ele localiza um arquivo.</span><span class="sxs-lookup"><span data-stu-id="53195-108">Optionally, this method also updates any source object for which it locates a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="53195-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53195-109">Syntax</span></span>


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a><span data-ttu-id="53195-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53195-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53195-111">*ValidateFlags*</span><span class="sxs-lookup"><span data-stu-id="53195-111">*ValidateFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="53195-112">Combinação de bits bit de [**sinalizadores de validação de nome de arquivo**](file-name-validation-flags.md) especificando o comportamento do localizador de mídia.</span><span class="sxs-lookup"><span data-stu-id="53195-112">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="53195-113">Os \_ sinalizadores de verificação SFN VALIDATEF \_ replace e SFN \_ VALIDATEF \_ devem estar presentes ou o método retorna E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="53195-113">The SFN\_VALIDATEF\_REPLACE and SFN\_VALIDATEF\_CHECK flags must be present, or the method returns E\_INVALIDARG.</span></span>

</dd> <dt>

<span data-ttu-id="53195-114">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="53195-114">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="53195-115">Ponteiro opcional para a interface [**IMediaLocator**](imedialocator.md) de um localizador de mídia a ser usado no lugar do padrão.</span><span class="sxs-lookup"><span data-stu-id="53195-115">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="53195-116">Para usar o localizador de mídia padrão, defina o valor desse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="53195-116">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="53195-117">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="53195-117">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="53195-118">*NotifyEventHandle*</span><span class="sxs-lookup"><span data-stu-id="53195-118">*NotifyEventHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="53195-119">Identificador para um evento.</span><span class="sxs-lookup"><span data-stu-id="53195-119">Handle to an event.</span></span> <span data-ttu-id="53195-120">O método sinaliza o evento depois de concluir a validação.</span><span class="sxs-lookup"><span data-stu-id="53195-120">The method signals the event after it has completed the validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53195-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53195-121">Return value</span></span>

<span data-ttu-id="53195-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="53195-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53195-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53195-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53195-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="53195-124">Remarks</span></span>

<span data-ttu-id="53195-125">Usando o parâmetro *pOverride* , você pode fornecer sua própria implementação personalizada da interface [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="53195-125">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="53195-126">Por exemplo, o localizador de mídia padrão não notificará seu aplicativo sobre os arquivos que ele encontra (ou não pode localizar).</span><span class="sxs-lookup"><span data-stu-id="53195-126">For example, the default media locator will not notify your application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="53195-127">Para contornar essa limitação, você pode implementar um localizador de mídia personalizado, tornando-o um wrapper para a versão padrão.</span><span class="sxs-lookup"><span data-stu-id="53195-127">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="53195-128">Em sua versão personalizada, passe [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) chamadas diretamente para a versão padrão e examine o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="53195-128">In your custom version, pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version, and examine the return value.</span></span>

> [!Note]  
> <span data-ttu-id="53195-129">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="53195-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53195-130">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="53195-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53195-131">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="53195-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53195-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53195-132">Requirements</span></span>



| <span data-ttu-id="53195-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="53195-133">Requirement</span></span> | <span data-ttu-id="53195-134">Valor</span><span class="sxs-lookup"><span data-stu-id="53195-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53195-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53195-135">Header</span></span><br/>  | <dl> <span data-ttu-id="53195-136"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="53195-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53195-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53195-137">Library</span></span><br/> | <dl> <span data-ttu-id="53195-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53195-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53195-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="53195-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53195-140">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="53195-140">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="53195-141">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="53195-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




