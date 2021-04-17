---
title: Método CreateObject IWMDRMProvider (wmdrmsdk. h)
description: O método CreateObject recupera um ponteiro para uma interface especificada, criando o objeto de implementação, se necessário.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Método CreateObject Windows Media Format
- Método CreateObject Windows Media Format, interface IWMDRMProvider
- Formato de mídia do Windows da interface IWMDRMProvider, método CreateObject
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747868"
---
# <a name="iwmdrmprovidercreateobject-method"></a><span data-ttu-id="d2f26-106">Método IWMDRMProvider:: CreateObject</span><span class="sxs-lookup"><span data-stu-id="d2f26-106">IWMDRMProvider::CreateObject method</span></span>

<span data-ttu-id="d2f26-107">O método **CreateObject** recupera um ponteiro para uma interface especificada, criando o objeto de implementação, se necessário.</span><span class="sxs-lookup"><span data-stu-id="d2f26-107">The **CreateObject** method retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f26-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2f26-108">Syntax</span></span>


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="d2f26-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2f26-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f26-110">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2f26-110">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f26-111">Identificador da interface a ser criada.</span><span class="sxs-lookup"><span data-stu-id="d2f26-111">Identifier of the interface to be created.</span></span> <span data-ttu-id="d2f26-112">Defina como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2f26-112">Set to one of the following values.</span></span>

-   <span data-ttu-id="d2f26-113">IWMDRMLicenseManagement de IID \_</span><span class="sxs-lookup"><span data-stu-id="d2f26-113">IID\_IWMDRMLicenseManagement</span></span>
-   <span data-ttu-id="d2f26-114">IWMDRMLicenseQuery de IID \_</span><span class="sxs-lookup"><span data-stu-id="d2f26-114">IID\_IWMDRMLicenseQuery</span></span>
-   <span data-ttu-id="d2f26-115">IWMDRMNetReceiver de IID \_</span><span class="sxs-lookup"><span data-stu-id="d2f26-115">IID\_IWMDRMNetReceiver</span></span>
-   <span data-ttu-id="d2f26-116">IWMDRMNetTransmitter de IID \_</span><span class="sxs-lookup"><span data-stu-id="d2f26-116">IID\_IWMDRMNetTransmitter</span></span>
-   <span data-ttu-id="d2f26-117">IWMDRMSecurity de IID \_</span><span class="sxs-lookup"><span data-stu-id="d2f26-117">IID\_IWMDRMSecurity</span></span>

</dd> <dt>

<span data-ttu-id="d2f26-118">*ppvObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d2f26-118">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f26-119">Endereço de um ponteiro que recebe o endereço da interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="d2f26-119">Address of a pointer that receives the address of the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f26-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2f26-120">Return value</span></span>

<span data-ttu-id="d2f26-121">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d2f26-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d2f26-122">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2f26-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d2f26-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d2f26-123">Return code</span></span>                                                                          | <span data-ttu-id="d2f26-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2f26-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d2f26-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f26-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d2f26-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d2f26-126">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2f26-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2f26-127">Remarks</span></span>

<span data-ttu-id="d2f26-128">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d2f26-128">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f26-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2f26-129">Requirements</span></span>



| <span data-ttu-id="d2f26-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2f26-130">Requirement</span></span> | <span data-ttu-id="d2f26-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d2f26-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f26-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2f26-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d2f26-133"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f26-133"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2f26-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2f26-134">Library</span></span><br/> | <dl> <span data-ttu-id="d2f26-135"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2f26-135"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2f26-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2f26-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f26-137">**Interface IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="d2f26-137">**IWMDRMProvider Interface**</span></span>](iwmdrmprovider.md)
</dt> <dt>

[<span data-ttu-id="d2f26-138">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="d2f26-138">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="d2f26-139">**Interface IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="d2f26-139">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="d2f26-140">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="d2f26-140">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="d2f26-141">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="d2f26-141">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> <dt>

[<span data-ttu-id="d2f26-142">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="d2f26-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





