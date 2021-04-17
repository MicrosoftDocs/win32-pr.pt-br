---
description: O método GetIPortableDeviceValuesFromBuffer desserializa uma matriz de bytes para uma interface IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'Método IWpdSerializer:: GetIPortableDeviceValuesFromBuffer (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787551"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a><span data-ttu-id="9aa7b-103">Método IWpdSerializer:: GetIPortableDeviceValuesFromBuffer</span><span class="sxs-lookup"><span data-stu-id="9aa7b-103">IWpdSerializer::GetIPortableDeviceValuesFromBuffer method</span></span>

<span data-ttu-id="9aa7b-104">O método **GetIPortableDeviceValuesFromBuffer** desserializa uma matriz de bytes para uma interface **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="9aa7b-104">The **GetIPortableDeviceValuesFromBuffer** method deserializes a byte array to an **IPortableDeviceValues** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aa7b-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a><span data-ttu-id="9aa7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aa7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa7b-107">*pBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aa7b-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa7b-108">Ponteiro para o buffer a ser desserializado.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-108">Pointer to the buffer to deserialize.</span></span>

</dd> <dt>

<span data-ttu-id="9aa7b-109">*dwInputBufferLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aa7b-109">*dwInputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa7b-110">**DWORD** que especifica o tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-110">**DWORD** that specifies the size of the buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9aa7b-111">*ppParams* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9aa7b-111">*ppParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa7b-112">Endereço de uma variável que recebe um ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) criada a partir do buffer.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-112">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface created from the buffer.</span></span> <span data-ttu-id="9aa7b-113">O aplicativo é responsável por chamar o **lançamento** na interface.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-113">The application is responsible for calling **Release** on the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa7b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9aa7b-114">Return value</span></span>

<span data-ttu-id="9aa7b-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9aa7b-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9aa7b-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9aa7b-117">Return code</span></span>                                                                                  | <span data-ttu-id="9aa7b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="9aa7b-118">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="9aa7b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9aa7b-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9aa7b-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-120">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="9aa7b-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="9aa7b-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="9aa7b-122">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-122">A required pointer argument was **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="9aa7b-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="9aa7b-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="9aa7b-124">Ocorreu um erro de conversão não especificado.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-124">An unspecified conversion error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9aa7b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aa7b-125">Requirements</span></span>



| <span data-ttu-id="9aa7b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa7b-126">Requirement</span></span> | <span data-ttu-id="9aa7b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9aa7b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa7b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aa7b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9aa7b-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aa7b-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9aa7b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9aa7b-130">Library</span></span><br/> | <dl> <span data-ttu-id="9aa7b-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aa7b-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aa7b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9aa7b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa7b-133">**Interface IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="9aa7b-133">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




