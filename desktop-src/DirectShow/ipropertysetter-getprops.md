---
description: O método GetProps recupera as propriedades definidas neste objeto, com seus valores correspondentes.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'Método IPropertySetter:: GetProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813086"
---
# <a name="ipropertysettergetprops-method"></a><span data-ttu-id="3095e-103">Método IPropertySetter:: GetProps</span><span class="sxs-lookup"><span data-stu-id="3095e-103">IPropertySetter::GetProps method</span></span>

> [!Note]  
> <span data-ttu-id="3095e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="3095e-104">\[Deprecated.</span></span> <span data-ttu-id="3095e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3095e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3095e-106">O `GetProps` método recupera as propriedades definidas neste objeto, com seus valores correspondentes.</span><span class="sxs-lookup"><span data-stu-id="3095e-106">The `GetProps` method retrieves the properties set on this object, with their corresponding values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3095e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3095e-107">Syntax</span></span>


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a><span data-ttu-id="3095e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3095e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3095e-109">*pcParams* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3095e-109">*pcParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3095e-110">Recebe o número de estruturas retornadas em *paParam*.</span><span class="sxs-lookup"><span data-stu-id="3095e-110">Receives the number of structures returned in *paParam*.</span></span>

</dd> <dt>

<span data-ttu-id="3095e-111">*paParam* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3095e-111">*paParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3095e-112">Endereço de um ponteiro para uma matriz de [**estruturas \_ param Dexter**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="3095e-112">Address of a pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="3095e-113">*paValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3095e-113">*paValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3095e-114">Endereço de um ponteiro para uma matriz de estruturas de [**\_ valor Dexter**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="3095e-114">Address of a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3095e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3095e-115">Return value</span></span>

<span data-ttu-id="3095e-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3095e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3095e-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3095e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3095e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3095e-118">Remarks</span></span>

<span data-ttu-id="3095e-119">Para cada propriedade retornada em *paParam*, o membro **nValores** indica o número de estruturas de [**\_ valor Dexter**](dexter-value.md) associadas à propriedade.</span><span class="sxs-lookup"><span data-stu-id="3095e-119">For each property returned in *paParam*, the **nValues** member indicates the number of [**DEXTER\_VALUE**](dexter-value.md) structures associated with the property.</span></span> <span data-ttu-id="3095e-120">Os pares são retornados em ordem de tempo crescente para cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="3095e-120">The pairs are returned in ascending time order for each property.</span></span>

<span data-ttu-id="3095e-121">Quando você terminar de usar as estruturas retornadas, chame [**IPropertySetter:: FreeProps**](ipropertysetter-freeprops.md) para liberar os recursos alocados por esse método.</span><span class="sxs-lookup"><span data-stu-id="3095e-121">When you are finished using the returned structures, call [**IPropertySetter::FreeProps**](ipropertysetter-freeprops.md) to free the resources allocated by this method.</span></span>

> [!Note]  
> <span data-ttu-id="3095e-122">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="3095e-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3095e-123">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3095e-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3095e-124">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3095e-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3095e-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3095e-125">Examples</span></span>

<span data-ttu-id="3095e-126">O exemplo de código a seguir mostra como iterar por todos os valores em uma instância do setter de propriedade:</span><span class="sxs-lookup"><span data-stu-id="3095e-126">The following code example shows how to iterate through all the values on an instance of the property setter:</span></span>


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a><span data-ttu-id="3095e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3095e-127">Requirements</span></span>



| <span data-ttu-id="3095e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3095e-128">Requirement</span></span> | <span data-ttu-id="3095e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3095e-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3095e-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3095e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3095e-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3095e-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3095e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3095e-132">Library</span></span><br/> | <dl> <span data-ttu-id="3095e-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3095e-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3095e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3095e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3095e-135">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="3095e-135">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="3095e-136">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="3095e-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




