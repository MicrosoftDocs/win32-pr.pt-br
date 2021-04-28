---
description: 'Método IPortableDeviceKeyCollection:: RemoveAt – o método RemoveAt remove o elemento armazenado no local especificado pelo índice fornecido.'
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'Método IPortableDeviceKeyCollection:: RemoveAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3ec2b1137e7959a646c2943ab1aa7a5c3428d3c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109934"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="4c678-103">Método IPortableDeviceKeyCollection:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="4c678-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="4c678-104">O método **RemoveAt** remove o elemento armazenado no local especificado pelo índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="4c678-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c678-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c678-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4c678-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c678-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c678-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4c678-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c678-108">Especifica o índice do elemento a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4c678-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c678-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4c678-109">Return value</span></span>

<span data-ttu-id="4c678-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4c678-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4c678-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c678-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4c678-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4c678-112">Return code</span></span>                                                                                  | <span data-ttu-id="4c678-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c678-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4c678-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c678-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4c678-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4c678-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="4c678-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4c678-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4c678-117">O índice especificado estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="4c678-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4c678-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c678-118">Remarks</span></span>

<span data-ttu-id="4c678-119">Você deve especificar um índice com base em zero.</span><span class="sxs-lookup"><span data-stu-id="4c678-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c678-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c678-120">Requirements</span></span>



| <span data-ttu-id="4c678-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c678-121">Requirement</span></span> | <span data-ttu-id="4c678-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4c678-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c678-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c678-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4c678-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c678-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c678-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c678-125">Library</span></span><br/> | <dl> <span data-ttu-id="4c678-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c678-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c678-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4c678-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c678-128">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="4c678-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




