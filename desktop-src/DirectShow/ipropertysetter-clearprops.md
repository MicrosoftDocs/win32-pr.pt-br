---
description: O método ClearProps limpa todos os dados de Propriedade do setter de propriedade. O aplicativo pode definir novos dados de propriedade depois de chamar essa função.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'Método IPropertySetter:: ClearProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757012"
---
# <a name="ipropertysetterclearprops-method"></a><span data-ttu-id="c1825-104">Método IPropertySetter:: ClearProps</span><span class="sxs-lookup"><span data-stu-id="c1825-104">IPropertySetter::ClearProps method</span></span>

> [!Note]  
> <span data-ttu-id="c1825-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c1825-105">\[Deprecated.</span></span> <span data-ttu-id="c1825-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1825-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1825-107">O `ClearProps` método limpa todos os dados de Propriedade do setter de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c1825-107">The `ClearProps` method clears all property data from the property setter.</span></span> <span data-ttu-id="c1825-108">O aplicativo pode definir novos dados de propriedade depois de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="c1825-108">The application can set new property data after calling this function.</span></span>

<span data-ttu-id="c1825-109">Limpar os dados de propriedade não restaura as propriedades do objeto para seus valores originais.</span><span class="sxs-lookup"><span data-stu-id="c1825-109">Clearing the property data does not restore the object's properties to their original values.</span></span> <span data-ttu-id="c1825-110">Ele simplesmente impede que o DirectShow aplique outras alterações.</span><span class="sxs-lookup"><span data-stu-id="c1825-110">It simply prevents DirectShow from applying any further changes.</span></span> <span data-ttu-id="c1825-111">Os valores de propriedade são aplicados em tempo de execução quando o projeto é renderizado.</span><span class="sxs-lookup"><span data-stu-id="c1825-111">Property values are applied at run time when the project renders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1825-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1825-112">Syntax</span></span>


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a><span data-ttu-id="c1825-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1825-113">Parameters</span></span>

<span data-ttu-id="c1825-114">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c1825-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1825-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1825-115">Return value</span></span>

<span data-ttu-id="c1825-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c1825-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1825-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1825-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1825-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1825-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1825-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c1825-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c1825-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1825-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c1825-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c1825-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1825-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1825-122">Requirements</span></span>



| <span data-ttu-id="c1825-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1825-123">Requirement</span></span> | <span data-ttu-id="c1825-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c1825-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1825-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1825-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c1825-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1825-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c1825-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1825-127">Library</span></span><br/> | <dl> <span data-ttu-id="c1825-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1825-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1825-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1825-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1825-130">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="c1825-130">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="c1825-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="c1825-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




