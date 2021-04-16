---
description: O método LogError registra um erro. Os aplicativos não precisam chamar esse método. Ele é chamado internamente em resposta a erros de renderização.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'Método IAMErrorLog:: LogError (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750275"
---
# <a name="iamerrorloglogerror-method"></a><span data-ttu-id="f5adc-105">Método IAMErrorLog:: LogError</span><span class="sxs-lookup"><span data-stu-id="f5adc-105">IAMErrorLog::LogError method</span></span>

> [!Note]  
> <span data-ttu-id="f5adc-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f5adc-106">\[Deprecated.</span></span> <span data-ttu-id="f5adc-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5adc-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5adc-108">O método **LogError** registra um erro.</span><span class="sxs-lookup"><span data-stu-id="f5adc-108">The **LogError** method logs an error.</span></span> <span data-ttu-id="f5adc-109">Os aplicativos não precisam chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="f5adc-109">Applications do not need to call this method.</span></span> <span data-ttu-id="f5adc-110">Ele é chamado internamente em resposta a erros de renderização.</span><span class="sxs-lookup"><span data-stu-id="f5adc-110">It is called internally in response to rendering errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5adc-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5adc-111">Syntax</span></span>


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f5adc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5adc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5adc-113">*Gravidade*</span><span class="sxs-lookup"><span data-stu-id="f5adc-113">*Severity*</span></span> 
</dt> <dd>

<span data-ttu-id="f5adc-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f5adc-114">Reserved.</span></span> <span data-ttu-id="f5adc-115">Não use.</span><span class="sxs-lookup"><span data-stu-id="f5adc-115">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="f5adc-116">*ErrorString*</span><span class="sxs-lookup"><span data-stu-id="f5adc-116">*ErrorString*</span></span> 
</dt> <dd>

<span data-ttu-id="f5adc-117">Valor da cadeia de caracteres que contém o texto do erro.</span><span class="sxs-lookup"><span data-stu-id="f5adc-117">String value containing the text of the error.</span></span>

</dd> <dt>

<span data-ttu-id="f5adc-118">*ErrorCode*</span><span class="sxs-lookup"><span data-stu-id="f5adc-118">*ErrorCode*</span></span> 
</dt> <dd>

<span data-ttu-id="f5adc-119">Código do erro.</span><span class="sxs-lookup"><span data-stu-id="f5adc-119">Error code.</span></span>

</dd> <dt>

<span data-ttu-id="f5adc-120">*resultado*</span><span class="sxs-lookup"><span data-stu-id="f5adc-120">*hresult*</span></span> 
</dt> <dd>

<span data-ttu-id="f5adc-121">O valor HRESULT retornado pela chamada de método que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="f5adc-121">The HRESULT value that was returned by the method call that caused the error.</span></span>

</dd> <dt>

<span data-ttu-id="f5adc-122">*pExtraInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5adc-122">*pExtraInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5adc-123">Ponteiro para uma variante que contém informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="f5adc-123">Pointer to a VARIANT that contains any additional information about the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5adc-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5adc-124">Return value</span></span>

<span data-ttu-id="f5adc-125">Retornar o valor do parâmetro *HRESULT* .</span><span class="sxs-lookup"><span data-stu-id="f5adc-125">Return the value of the *hresult* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5adc-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5adc-126">Remarks</span></span>

<span data-ttu-id="f5adc-127">Dentro desse método, não libere a **variante** apontada por *pExtraInfo*.</span><span class="sxs-lookup"><span data-stu-id="f5adc-127">Within this method, do not free the **VARIANT** pointed to by *pExtraInfo*.</span></span> <span data-ttu-id="f5adc-128">Além disso, a **variante** torna-se inválida depois que o método retorna, portanto, não tente fazer referência posteriormente.</span><span class="sxs-lookup"><span data-stu-id="f5adc-128">Also, the **VARIANT** becomes invalid after the method returns, so do not try to reference it later.</span></span>

<span data-ttu-id="f5adc-129">Implemente esse método para retornar o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="f5adc-129">Implement this method to return as quickly as possible.</span></span> <span data-ttu-id="f5adc-130">Não faça chamadas de função de dentro desse método que possam bloquear a execução do programa.</span><span class="sxs-lookup"><span data-stu-id="f5adc-130">Do not make function calls from inside this method that might block program execution.</span></span> <span data-ttu-id="f5adc-131">Por exemplo, não chame funções que enviam mensagens de janela, bloqueiem eventos ou, de outra forma, podem bloquear a execução.</span><span class="sxs-lookup"><span data-stu-id="f5adc-131">For example, do not call functions that send window messages, block on events, or otherwise might block execution.</span></span> <span data-ttu-id="f5adc-132">Isso pode fazer com que o computador pare de responder.</span><span class="sxs-lookup"><span data-stu-id="f5adc-132">Doing so could cause the computer to stop responding.</span></span>

<span data-ttu-id="f5adc-133">Para obter uma lista de erros definidos pelo DES, juntamente com o significado e o tipo de dados da **variante** apontada por *PExtraInfo*, consulte [erros de renderização](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f5adc-133">For a list of errors defined by DES, along with the meaning and data type of the **VARIANT** pointed to by *pExtraInfo*, see [Rendering Errors](rendering-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="f5adc-134">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f5adc-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5adc-135">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5adc-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5adc-136">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f5adc-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5adc-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5adc-137">Requirements</span></span>



| <span data-ttu-id="f5adc-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5adc-138">Requirement</span></span> | <span data-ttu-id="f5adc-139">Valor</span><span class="sxs-lookup"><span data-stu-id="f5adc-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5adc-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5adc-140">Header</span></span><br/>  | <dl> <span data-ttu-id="f5adc-141"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5adc-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5adc-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5adc-142">Library</span></span><br/> | <dl> <span data-ttu-id="f5adc-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5adc-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5adc-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5adc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5adc-145">**Interface IAMErrorLog**</span><span class="sxs-lookup"><span data-stu-id="f5adc-145">**IAMErrorLog Interface**</span></span>](iamerrorlog.md)
</dt> <dt>

[<span data-ttu-id="f5adc-146">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="f5adc-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




