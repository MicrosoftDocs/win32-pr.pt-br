---
description: O método SetProps define as propriedades do objeto de destino para o estado apropriado para o tempo especificado.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'Método IPropertySetter:: SetProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778434"
---
# <a name="ipropertysettersetprops-method"></a><span data-ttu-id="6bcc8-103">Método IPropertySetter:: SetProps</span><span class="sxs-lookup"><span data-stu-id="6bcc8-103">IPropertySetter::SetProps method</span></span>

> [!Note]  
> <span data-ttu-id="6bcc8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6bcc8-104">\[Deprecated.</span></span> <span data-ttu-id="6bcc8-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6bcc8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6bcc8-106">O `SetProps` método define as propriedades do objeto de destino para o estado apropriado para o tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="6bcc8-106">The `SetProps` method sets the properties of the target object to the appropriate state for the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bcc8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bcc8-107">Syntax</span></span>


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a><span data-ttu-id="6bcc8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bcc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bcc8-109">*pTarget* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bcc8-109">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bcc8-110">Ponteiro para o objeto de destino para o qual definir as propriedades.</span><span class="sxs-lookup"><span data-stu-id="6bcc8-110">Pointer to the target object for which to set the properties.</span></span>

</dd> <dt>

<span data-ttu-id="6bcc8-111">*rtNow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bcc8-111">*rtNow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bcc8-112">Hora na qual definir as propriedades, em unidades de 100 a nanossegundos ou – 1 para definir propriedades estáticas (aquelas que não variam ao longo do tempo).</span><span class="sxs-lookup"><span data-stu-id="6bcc8-112">Time at which to set the properties, in 100-nanosecond units, or –1 to set static properties (those that do not vary over time).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bcc8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6bcc8-113">Return value</span></span>

<span data-ttu-id="6bcc8-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6bcc8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6bcc8-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6bcc8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bcc8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bcc8-116">Remarks</span></span>

<span data-ttu-id="6bcc8-117">Esse método é chamado pelo DES para definir as propriedades em uma transição ou efeito.</span><span class="sxs-lookup"><span data-stu-id="6bcc8-117">This method is called by DES to set the properties on a transition or effect.</span></span> <span data-ttu-id="6bcc8-118">Normalmente, um aplicativo não chamará esse método.</span><span class="sxs-lookup"><span data-stu-id="6bcc8-118">An application will not normally call this method.</span></span>

<span data-ttu-id="6bcc8-119">O objeto especificado por *pTarget* deve implementar a interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="6bcc8-119">The object specified by *pTarget* must implement the **IDispatch** interface.</span></span>

> [!Note]  
> <span data-ttu-id="6bcc8-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6bcc8-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6bcc8-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6bcc8-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6bcc8-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6bcc8-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6bcc8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bcc8-123">Requirements</span></span>



| <span data-ttu-id="6bcc8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bcc8-124">Requirement</span></span> | <span data-ttu-id="6bcc8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6bcc8-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bcc8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bcc8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6bcc8-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bcc8-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6bcc8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bcc8-128">Library</span></span><br/> | <dl> <span data-ttu-id="6bcc8-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bcc8-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bcc8-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bcc8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bcc8-131">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="6bcc8-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="6bcc8-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="6bcc8-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




