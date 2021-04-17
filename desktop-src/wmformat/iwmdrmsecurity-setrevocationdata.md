---
title: Método IWMDRMSecurity SetRevocationData (wmdrmsdk. h)
description: O método SetRevocationData define uma lista de certificados revogados no repositório local.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Formato de mídia do Windows do método SetRevocationData
- Método SetRevocationData Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método SetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754693"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a><span data-ttu-id="aded5-106">Método IWMDRMSecurity:: SetRevocationData</span><span class="sxs-lookup"><span data-stu-id="aded5-106">IWMDRMSecurity::SetRevocationData method</span></span>

<span data-ttu-id="aded5-107">O método **SetRevocationData** define uma lista de certificados revogados no repositório local.</span><span class="sxs-lookup"><span data-stu-id="aded5-107">The **SetRevocationData** method sets a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="aded5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aded5-108">Syntax</span></span>


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="aded5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aded5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aded5-110">*f \_ guidRevocationType* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="aded5-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aded5-111">GUID que especifica o tipo de lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="aded5-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="aded5-112">Defina como uma das constantes na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aded5-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="aded5-113">Constante de GUID</span><span class="sxs-lookup"><span data-stu-id="aded5-113">GUID constant</span></span>                 | <span data-ttu-id="aded5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="aded5-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aded5-115">\_aplicativo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="aded5-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="aded5-116">Especifica a lista de certificados revogados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aded5-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="aded5-117">\_dispositivo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="aded5-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="aded5-118">Especifica a lista de certificados revogados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aded5-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="aded5-119">WMDRM \_ RErevocationtype \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="aded5-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="aded5-120">Especifica a lista de revogação de certificados do Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="aded5-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="aded5-121">*f \_ pbCRL* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="aded5-121">*f\_pbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aded5-122">Buffer que contém a lista de certificados revogados.</span><span class="sxs-lookup"><span data-stu-id="aded5-122">Buffer containing the certificate revocation list.</span></span>

</dd> <dt>

<span data-ttu-id="aded5-123">*f \_ cbCRL* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="aded5-123">*f\_cbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aded5-124">Tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="aded5-124">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aded5-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aded5-125">Return value</span></span>

<span data-ttu-id="aded5-126">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aded5-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aded5-127">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aded5-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aded5-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="aded5-128">Return code</span></span>                                                                          | <span data-ttu-id="aded5-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="aded5-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="aded5-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aded5-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="aded5-131">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="aded5-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aded5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aded5-132">Requirements</span></span>



| <span data-ttu-id="aded5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="aded5-133">Requirement</span></span> | <span data-ttu-id="aded5-134">Valor</span><span class="sxs-lookup"><span data-stu-id="aded5-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aded5-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aded5-135">Header</span></span><br/>  | <dl> <span data-ttu-id="aded5-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="aded5-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="aded5-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aded5-137">Library</span></span><br/> | <dl> <span data-ttu-id="aded5-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aded5-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aded5-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="aded5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aded5-140">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="aded5-140">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="aded5-141">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="aded5-141">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="aded5-142">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="aded5-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





