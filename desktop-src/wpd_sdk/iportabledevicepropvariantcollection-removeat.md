---
description: O método RemoveAt remove o elemento armazenado no local especificado pelo índice fornecido.
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'Método IPortableDevicePropVariantCollection:: RemoveAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761139"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="66fb7-103">Método IPortableDevicePropVariantCollection:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="66fb7-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="66fb7-104">O método **RemoveAt** remove o elemento armazenado no local especificado pelo índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="66fb7-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="66fb7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66fb7-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="66fb7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66fb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66fb7-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66fb7-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66fb7-108">Especifica o índice do elemento a ser removido.</span><span class="sxs-lookup"><span data-stu-id="66fb7-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66fb7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66fb7-109">Return value</span></span>

<span data-ttu-id="66fb7-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="66fb7-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="66fb7-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="66fb7-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="66fb7-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="66fb7-112">Return code</span></span>                                                                                  | <span data-ttu-id="66fb7-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="66fb7-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="66fb7-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66fb7-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="66fb7-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="66fb7-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="66fb7-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="66fb7-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="66fb7-117">O índice especificado estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="66fb7-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66fb7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="66fb7-118">Remarks</span></span>

<span data-ttu-id="66fb7-119">Você deve especificar um índice com base em zero.</span><span class="sxs-lookup"><span data-stu-id="66fb7-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="66fb7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66fb7-120">Requirements</span></span>



| <span data-ttu-id="66fb7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="66fb7-121">Requirement</span></span> | <span data-ttu-id="66fb7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="66fb7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fb7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66fb7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="66fb7-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="66fb7-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="66fb7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66fb7-125">Library</span></span><br/> | <dl> <span data-ttu-id="66fb7-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66fb7-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66fb7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="66fb7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fb7-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="66fb7-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




