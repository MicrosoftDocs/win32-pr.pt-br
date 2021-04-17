---
description: O método setbuffervalue adiciona um novo valor de BYTE \* (tipo VT \_ vector \| VT \_ UI1) ou substitui um existente.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'Método IPortableDeviceValues:: setbuffervalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749343"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a><span data-ttu-id="4b1a0-103">Método IPortableDeviceValues:: setbuffervalue</span><span class="sxs-lookup"><span data-stu-id="4b1a0-103">IPortableDeviceValues::SetBufferValue method</span></span>

<span data-ttu-id="4b1a0-104">O método **Setbuffervalue** adiciona um novo valor de **byte** \* (tipo VT \_ vector \| VT \_ UI1) ou substitui um existente.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-104">The **SetBufferValue** method adds a new **BYTE**\* value (type VT\_VECTOR \| VT\_UI1) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b1a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b1a0-105">Syntax</span></span>


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a><span data-ttu-id="4b1a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b1a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b1a0-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4b1a0-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1a0-108">Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a0-109">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4b1a0-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1a0-110">Um **byte \*** que contém os dados a serem gravados no item.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-110">A **BYTE\*** that contains the data to write to the item.</span></span> <span data-ttu-id="4b1a0-111">Os dados de buffer enviados são copiados para a interface, para que o chamador possa liberar esse buffer depois de fazer essa chamada.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-111">The submitted buffer data is copied to the interface, so the caller can free this buffer after making this call.</span></span>

</dd> <dt>

<span data-ttu-id="4b1a0-112">*cbValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4b1a0-112">*cbValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1a0-113">O tamanho do valor apontado *por value, em* bytes.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-113">The size of the value pointed to by *pValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b1a0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b1a0-114">Return value</span></span>

<span data-ttu-id="4b1a0-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4b1a0-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4b1a0-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4b1a0-117">Return code</span></span>                                                                          | <span data-ttu-id="4b1a0-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b1a0-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4b1a0-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1a0-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4b1a0-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b1a0-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b1a0-121">Remarks</span></span>

<span data-ttu-id="4b1a0-122">Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-122">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="4b1a0-123">A memória de chave existente é liberada adequadamente.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-123">The existing key memory is released appropriately.</span></span>

<span data-ttu-id="4b1a0-124">Não há suporte para a definição de um buffer **nulo** ou de tamanho zero.</span><span class="sxs-lookup"><span data-stu-id="4b1a0-124">Setting a **NULL** or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b1a0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b1a0-125">Requirements</span></span>



| <span data-ttu-id="4b1a0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b1a0-126">Requirement</span></span> | <span data-ttu-id="4b1a0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4b1a0-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b1a0-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b1a0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4b1a0-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b1a0-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b1a0-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b1a0-130">Library</span></span><br/> | <dl> <span data-ttu-id="4b1a0-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b1a0-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b1a0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b1a0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b1a0-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="4b1a0-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="4b1a0-134">**IPortableDeviceValues:: getbuffervalue**</span><span class="sxs-lookup"><span data-stu-id="4b1a0-134">**IPortableDeviceValues::GetBufferValue**</span></span>](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




