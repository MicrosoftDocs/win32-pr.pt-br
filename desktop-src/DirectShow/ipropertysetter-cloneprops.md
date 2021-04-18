---
description: O método CloneProps clona um conjunto de propriedades desse setter de propriedade e as adiciona a um novo setter de propriedade.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'Método IPropertySetter:: CloneProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760184"
---
# <a name="ipropertysettercloneprops-method"></a><span data-ttu-id="95c3e-103">Método IPropertySetter:: CloneProps</span><span class="sxs-lookup"><span data-stu-id="95c3e-103">IPropertySetter::CloneProps method</span></span>

> [!Note]  
> <span data-ttu-id="95c3e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="95c3e-104">\[Deprecated.</span></span> <span data-ttu-id="95c3e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="95c3e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="95c3e-106">O `CloneProps` método clona um conjunto de propriedades deste setter de propriedade e os adiciona a um novo setter de propriedade.</span><span class="sxs-lookup"><span data-stu-id="95c3e-106">The `CloneProps` method clones a set of properties from this property setter and adds them to a new property setter.</span></span>

## <a name="syntax"></a><span data-ttu-id="95c3e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95c3e-107">Syntax</span></span>


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a><span data-ttu-id="95c3e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95c3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c3e-109">*ppSetter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95c3e-109">*ppSetter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95c3e-110">Recebe um ponteiro para a interface **IPropertySetter** do setter da nova propriedade.</span><span class="sxs-lookup"><span data-stu-id="95c3e-110">Receives a pointer to the **IPropertySetter** interface of the new property setter.</span></span>

</dd> <dt>

<span data-ttu-id="95c3e-111">*rtStart* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95c3e-111">*rtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c3e-112">Hora de início do intervalo de valores a serem clonados, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="95c3e-112">Start time of the range of values to clone, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="95c3e-113">*rtStop* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95c3e-113">*rtStop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c3e-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="95c3e-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c3e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95c3e-115">Return value</span></span>

<span data-ttu-id="95c3e-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="95c3e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95c3e-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95c3e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="95c3e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="95c3e-118">Remarks</span></span>

<span data-ttu-id="95c3e-119">Somente os valores que se enquadram após a hora de início especificada são clonados.</span><span class="sxs-lookup"><span data-stu-id="95c3e-119">Only values that fall after the specified start time are cloned.</span></span> <span data-ttu-id="95c3e-120">Os horários nos valores clonados são então ajustados em relação à hora de início.</span><span class="sxs-lookup"><span data-stu-id="95c3e-120">The times on the cloned values are then adjusted relative to the start time.</span></span> <span data-ttu-id="95c3e-121">Por exemplo, se *rtStart* for 20 milhões (2 segundos), um valor na hora 30 milhões (3 segundos) será clonado com o tempo 10 milhões (1 segundo).</span><span class="sxs-lookup"><span data-stu-id="95c3e-121">For example, if *rtStart* is 20000000 (2 seconds), then a value at time 30000000 (3 seconds) is cloned with time 10000000 (1 second).</span></span> <span data-ttu-id="95c3e-122">Por fim, cada propriedade clonada recebe um valor inicial igual ao valor da propriedade original na hora de início (interpolada corretamente, se necessário).</span><span class="sxs-lookup"><span data-stu-id="95c3e-122">Finally, each cloned property is given an initial value equal to the value of the original property at the start time (correctly interpolated if necessary).</span></span> <span data-ttu-id="95c3e-123">Na verdade, os dados da propriedade são divididos na hora de início especificada.</span><span class="sxs-lookup"><span data-stu-id="95c3e-123">In effect, the property data is split at the specified start time.</span></span>

<span data-ttu-id="95c3e-124">Se o método for executado com sucesso, a interface [**IPropertySetter**](ipropertysetter.md) que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="95c3e-124">If the method succeeds, the [**IPropertySetter**](ipropertysetter.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="95c3e-125">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="95c3e-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="95c3e-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="95c3e-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="95c3e-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="95c3e-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="95c3e-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="95c3e-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95c3e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c3e-129">Requirements</span></span>



| <span data-ttu-id="95c3e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="95c3e-130">Requirement</span></span> | <span data-ttu-id="95c3e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="95c3e-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95c3e-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95c3e-132">Header</span></span><br/>  | <dl> <span data-ttu-id="95c3e-133"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c3e-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="95c3e-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95c3e-134">Library</span></span><br/> | <dl> <span data-ttu-id="95c3e-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95c3e-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95c3e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="95c3e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c3e-137">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="95c3e-137">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="95c3e-138">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="95c3e-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




