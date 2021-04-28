---
description: 'Método IPortableDeviceValuesCollection:: RemoveAt – o método RemoveAt remove o elemento armazenado no local especificado pelo índice fornecido.'
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: 'Método IPortableDeviceValuesCollection:: RemoveAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083164"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a><span data-ttu-id="dcfda-103">Método IPortableDeviceValuesCollection:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="dcfda-103">IPortableDeviceValuesCollection::RemoveAt method</span></span>

<span data-ttu-id="dcfda-104">O método **RemoveAt** remove o elemento armazenado no local especificado pelo índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="dcfda-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfda-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcfda-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="dcfda-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcfda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcfda-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcfda-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcfda-108">Especifica o índice do elemento a ser removido.</span><span class="sxs-lookup"><span data-stu-id="dcfda-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcfda-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dcfda-109">Return value</span></span>

<span data-ttu-id="dcfda-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dcfda-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dcfda-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dcfda-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dcfda-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dcfda-112">Return code</span></span>                                                                                  | <span data-ttu-id="dcfda-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcfda-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="dcfda-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfda-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dcfda-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dcfda-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="dcfda-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfda-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dcfda-117">O índice especificado estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="dcfda-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dcfda-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcfda-118">Remarks</span></span>

<span data-ttu-id="dcfda-119">Você deve especificar um índice com base em zero.</span><span class="sxs-lookup"><span data-stu-id="dcfda-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfda-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcfda-120">Requirements</span></span>



| <span data-ttu-id="dcfda-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcfda-121">Requirement</span></span> | <span data-ttu-id="dcfda-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dcfda-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfda-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dcfda-123">Header</span></span><br/>  | <dl> <span data-ttu-id="dcfda-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcfda-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="dcfda-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcfda-125">Library</span></span><br/> | <dl> <span data-ttu-id="dcfda-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcfda-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfda-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dcfda-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfda-128">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="dcfda-128">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




