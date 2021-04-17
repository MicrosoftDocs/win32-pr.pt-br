---
title: Método IWMDRMSecurity GetRevocationData (wmdrmsdk. h)
description: O método GetRevocationData recupera uma lista de certificados revogados do repositório local.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Formato de mídia do Windows do método GetRevocationData
- Método GetRevocationData Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750877"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a><span data-ttu-id="d2b93-106">Método IWMDRMSecurity:: GetRevocationData</span><span class="sxs-lookup"><span data-stu-id="d2b93-106">IWMDRMSecurity::GetRevocationData method</span></span>

<span data-ttu-id="d2b93-107">O método **GetRevocationData** recupera uma lista de certificados revogados do repositório local.</span><span class="sxs-lookup"><span data-stu-id="d2b93-107">The **GetRevocationData** method retrieves a certificate revocation list from the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2b93-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2b93-108">Syntax</span></span>


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="d2b93-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2b93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2b93-110">*f \_ guidRevocationType* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d2b93-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b93-111">GUID que identifica o tipo de lista de revogação a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="d2b93-111">GUID identifying the type of revocation list to retrieve.</span></span> <span data-ttu-id="d2b93-112">Use uma das constantes na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2b93-112">Use one of the constants in the following table.</span></span>



| <span data-ttu-id="d2b93-113">Constante de GUID</span><span class="sxs-lookup"><span data-stu-id="d2b93-113">GUID constant</span></span>                 | <span data-ttu-id="d2b93-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2b93-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d2b93-115">\_aplicativo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="d2b93-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="d2b93-116">Especifica a lista de certificados revogados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2b93-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="d2b93-117">\_dispositivo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="d2b93-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="d2b93-118">Especifica a lista de certificados revogados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2b93-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="d2b93-119">WMDRM \_ RErevocationtype \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="d2b93-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="d2b93-120">Especifica a lista de revogação de certificados do Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="d2b93-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d2b93-121">saída de *f \_ pbCRL* \[\]</span><span class="sxs-lookup"><span data-stu-id="d2b93-121">*f\_pbCRL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b93-122">Buffer que recebe a lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="d2b93-122">Buffer that receives the revocation list.</span></span> <span data-ttu-id="d2b93-123">Defina como **NULL** para obter o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="d2b93-123">Set to **NULL** to get the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="d2b93-124">*f \_ pcbCRL* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d2b93-124">*f\_pcbCRL* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b93-125">O tamanho do buffer em bytes.</span><span class="sxs-lookup"><span data-stu-id="d2b93-125">Size of the buffer in bytes.</span></span> <span data-ttu-id="d2b93-126">Se *f \_ PbCRL* for **NULL**, esse valor será definido como o tamanho de buffer necessário na saída.</span><span class="sxs-lookup"><span data-stu-id="d2b93-126">If *f\_pbCRL* is **NULL**, this value is set to the required buffer size on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2b93-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2b93-127">Return value</span></span>

<span data-ttu-id="d2b93-128">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d2b93-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d2b93-129">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2b93-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d2b93-130">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d2b93-130">Return code</span></span>                                                                          | <span data-ttu-id="d2b93-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2b93-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d2b93-132"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b93-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d2b93-133">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d2b93-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d2b93-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2b93-134">Requirements</span></span>



| <span data-ttu-id="d2b93-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2b93-135">Requirement</span></span> | <span data-ttu-id="d2b93-136">Valor</span><span class="sxs-lookup"><span data-stu-id="d2b93-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b93-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2b93-137">Header</span></span><br/>  | <dl> <span data-ttu-id="d2b93-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b93-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2b93-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2b93-139">Library</span></span><br/> | <dl> <span data-ttu-id="d2b93-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2b93-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b93-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2b93-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b93-142">**Revogação e renovação de componentes automatizados**</span><span class="sxs-lookup"><span data-stu-id="d2b93-142">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="d2b93-143">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="d2b93-143">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="d2b93-144">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="d2b93-144">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="d2b93-145">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="d2b93-145">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





