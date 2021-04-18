---
title: Método IWMDRMLicenseManagement MonitorLicenseAcquisition (wmdrmsdk. h)
description: O método MonitorLicenseAcquisition inicia o monitoramento para um processo de aquisição de licença.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Formato de mídia do Windows do método MonitorLicenseAcquisition
- Método MonitorLicenseAcquisition Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método MonitorLicenseAcquisition
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793856"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a><span data-ttu-id="5e7e2-106">Método IWMDRMLicenseManagement:: MonitorLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="5e7e2-106">IWMDRMLicenseManagement::MonitorLicenseAcquisition method</span></span>

<span data-ttu-id="5e7e2-107">O método **MonitorLicenseAcquisition** inicia o monitoramento para um processo de aquisição de licença.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-107">The **MonitorLicenseAcquisition** method initiates monitoring for a license acquisition process.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7e2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e7e2-108">Syntax</span></span>


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="5e7e2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e7e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e7e2-110">*bstrKID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e7e2-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e7e2-111">ID da chave (KID) da licença que está sendo adquirida.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-111">Key ID (KID) of the license being acquired.</span></span>

</dd> <dt>

<span data-ttu-id="5e7e2-112">*bstrHeader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e7e2-112">*bstrHeader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e7e2-113">Cabeçalho de conteúdo que foi usado na chamada para o método [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="5e7e2-113">Content header that was used in the call to the [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5e7e2-114">*bstrActions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e7e2-114">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e7e2-115">Cadeia de caracteres que contém as ações solicitadas na chamada para o método **AcquireLicense** .</span><span class="sxs-lookup"><span data-stu-id="5e7e2-115">String containing the actions requested in the call to the **AcquireLicense** method.</span></span>

</dd> <dt>

<span data-ttu-id="5e7e2-116">*ppunkCancelationCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5e7e2-116">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e7e2-117">Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-117">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="5e7e2-118">Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="5e7e2-118">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e7e2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e7e2-119">Return value</span></span>

<span data-ttu-id="5e7e2-120">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-120">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5e7e2-121">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-121">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5e7e2-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5e7e2-122">Return code</span></span>                                                                          | <span data-ttu-id="5e7e2-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e7e2-123">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5e7e2-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e7e2-124"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5e7e2-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-125">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e7e2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e7e2-126">Remarks</span></span>

<span data-ttu-id="5e7e2-127">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-127">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e7e2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e7e2-128">Requirements</span></span>



| <span data-ttu-id="5e7e2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e7e2-129">Requirement</span></span> | <span data-ttu-id="5e7e2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5e7e2-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e7e2-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e7e2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5e7e2-132"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e7e2-132"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e7e2-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e7e2-133">Library</span></span><br/> | <dl> <span data-ttu-id="5e7e2-134"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e7e2-134"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e7e2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e7e2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e7e2-136">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="5e7e2-136">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





