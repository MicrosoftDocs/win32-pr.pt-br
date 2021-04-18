---
description: O método SetSourceNameValidation especifica como o mecanismo de renderização valida nomes de arquivo.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'Método IRenderEngine:: SetSourceNameValidation (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757011"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a><span data-ttu-id="069ab-103">Método IRenderEngine:: SetSourceNameValidation</span><span class="sxs-lookup"><span data-stu-id="069ab-103">IRenderEngine::SetSourceNameValidation method</span></span>

> [!Note]  
> <span data-ttu-id="069ab-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="069ab-104">\[Deprecated.</span></span> <span data-ttu-id="069ab-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="069ab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="069ab-106">O `SetSourceNameValidation` método especifica como o mecanismo de renderização valida nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="069ab-106">The `SetSourceNameValidation` method specifies how the render engine validates file names.</span></span>

## <a name="syntax"></a><span data-ttu-id="069ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="069ab-107">Syntax</span></span>


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a><span data-ttu-id="069ab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="069ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="069ab-109">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="069ab-109">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="069ab-110">Valor **BSTR** que contém pares de cadeias de caracteres de filtro, formatados conforme exigido pelo membro **LpstrFilter** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="069ab-110">**BSTR** value containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="069ab-111">O localizador de mídia usará esse filtro se ele apresentar uma caixa de diálogo abrir arquivo ao usuário final.</span><span class="sxs-lookup"><span data-stu-id="069ab-111">The media locator uses this filter if it presents an Open File dialog box to the end user.</span></span>

</dd> <dt>

<span data-ttu-id="069ab-112">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="069ab-112">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="069ab-113">Ponteiro opcional para a interface [**IMediaLocator**](imedialocator.md) de um localizador de mídia a ser usado no lugar do padrão.</span><span class="sxs-lookup"><span data-stu-id="069ab-113">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="069ab-114">Para usar o localizador de mídia padrão, defina o valor desse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="069ab-114">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="069ab-115">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="069ab-115">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="069ab-116">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="069ab-116">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="069ab-117">Combinação de bits bit de [**sinalizadores de validação de nome de arquivo**](file-name-validation-flags.md) especificando o comportamento do localizador de mídia.</span><span class="sxs-lookup"><span data-stu-id="069ab-117">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="069ab-118">O sinalizador de verificação de VALIDATEF de SFN \_ \_ deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="069ab-118">The SFN\_VALIDATEF\_CHECK flag must be present.</span></span> <span data-ttu-id="069ab-119">O \_ sinalizador SFN VALIDATEF \_ hlinkMUTED não tem nenhum efeito com esse método.</span><span class="sxs-lookup"><span data-stu-id="069ab-119">The SFN\_VALIDATEF\_hlinkMUTED flag has no effect with this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="069ab-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="069ab-120">Return value</span></span>

<span data-ttu-id="069ab-121">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="069ab-121">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="069ab-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="069ab-122">Return code</span></span>                                                                                            | <span data-ttu-id="069ab-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="069ab-123">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="069ab-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="069ab-124"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="069ab-125">Êxito.</span><span class="sxs-lookup"><span data-stu-id="069ab-125">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="069ab-126"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="069ab-126"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="069ab-127">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="069ab-127">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="069ab-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="069ab-128">Remarks</span></span>

<span data-ttu-id="069ab-129">Usando o parâmetro *pOverride* , você pode fornecer sua própria implementação personalizada da interface [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="069ab-129">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="069ab-130">Por exemplo, o localizador de mídia padrão não notifica um aplicativo sobre os arquivos que ele encontra (ou não pode localizar).</span><span class="sxs-lookup"><span data-stu-id="069ab-130">For example, the default media locator does not notify an application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="069ab-131">Para contornar essa limitação, você pode implementar um localizador de mídia personalizado, tornando-o um wrapper para a versão padrão.</span><span class="sxs-lookup"><span data-stu-id="069ab-131">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="069ab-132">Em seguida, passe [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) chamadas diretamente para a versão padrão e examine o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="069ab-132">Then pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version and examine the return value.</span></span>

<span data-ttu-id="069ab-133">Atualmente, esse método não valida as fontes carregadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="069ab-133">Currently, this method does not validate dynamically loaded sources.</span></span> <span data-ttu-id="069ab-134">Consulte [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="069ab-134">See [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="069ab-135">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="069ab-135">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="069ab-136">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="069ab-136">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="069ab-137">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="069ab-137">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="069ab-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="069ab-138">Requirements</span></span>



| <span data-ttu-id="069ab-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="069ab-139">Requirement</span></span> | <span data-ttu-id="069ab-140">Valor</span><span class="sxs-lookup"><span data-stu-id="069ab-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="069ab-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="069ab-141">Header</span></span><br/>  | <dl> <span data-ttu-id="069ab-142"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="069ab-142"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="069ab-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="069ab-143">Library</span></span><br/> | <dl> <span data-ttu-id="069ab-144"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="069ab-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="069ab-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="069ab-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069ab-146">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="069ab-146">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="069ab-147">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="069ab-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
