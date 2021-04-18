---
title: Método IWMDRMDevice SetLicenseResponse
description: O método SetLicenseResponse define a resposta da licença.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Método SetLicenseResponse Windows Media Gerenciador de Dispositivos
- Método SetLicenseResponse Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método SetLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781293"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a><span data-ttu-id="8064c-106">Método IWMDRMDevice:: SetLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="8064c-106">IWMDRMDevice::SetLicenseResponse method</span></span>

<span data-ttu-id="8064c-107">O método **SetLicenseResponse** define a resposta da licença.</span><span class="sxs-lookup"><span data-stu-id="8064c-107">The **SetLicenseResponse** method sets the license response.</span></span>

## <a name="syntax"></a><span data-ttu-id="8064c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8064c-108">Syntax</span></span>


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="8064c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8064c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8064c-110">*pbResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8064c-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8064c-111">Especifica a resposta a ser definida.</span><span class="sxs-lookup"><span data-stu-id="8064c-111">Specifies the response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="8064c-112">*cbResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8064c-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8064c-113">Tamanho da resposta, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8064c-113">Size of the response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8064c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8064c-114">Return value</span></span>

<span data-ttu-id="8064c-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8064c-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8064c-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8064c-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8064c-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8064c-117">Return code</span></span>                                                                          | <span data-ttu-id="8064c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8064c-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8064c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8064c-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8064c-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8064c-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8064c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8064c-121">Requirements</span></span>



| <span data-ttu-id="8064c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8064c-122">Requirement</span></span> | <span data-ttu-id="8064c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8064c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8064c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8064c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8064c-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8064c-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="8064c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8064c-126">Library</span></span><br/> | <dl> <span data-ttu-id="8064c-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8064c-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8064c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8064c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8064c-129">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="8064c-129">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





