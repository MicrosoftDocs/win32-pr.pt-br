---
title: Método IWMDRMSecurity CheckCertForRevocation (wmdrmsdk. h)
description: O método CheckCertForRevocation determina se um certificado foi revogado.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Formato de mídia do Windows do método CheckCertForRevocation
- Método CheckCertForRevocation Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método CheckCertForRevocation
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752558"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a><span data-ttu-id="92402-106">Método IWMDRMSecurity:: CheckCertForRevocation</span><span class="sxs-lookup"><span data-stu-id="92402-106">IWMDRMSecurity::CheckCertForRevocation method</span></span>

<span data-ttu-id="92402-107">O método **CheckCertForRevocation** determina se um certificado foi revogado.</span><span class="sxs-lookup"><span data-stu-id="92402-107">The **CheckCertForRevocation** method determines whether a certificate has been revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="92402-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92402-108">Syntax</span></span>


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a><span data-ttu-id="92402-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92402-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92402-110">*rguidRevocationList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92402-110">*rguidRevocationList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92402-111">GUID que identifica a lista de revogação a ser usada.</span><span class="sxs-lookup"><span data-stu-id="92402-111">GUID identifying the revocation list to use.</span></span> <span data-ttu-id="92402-112">Defina como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="92402-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="92402-113">Constante de GUID</span><span class="sxs-lookup"><span data-stu-id="92402-113">GUID constant</span></span>                 | <span data-ttu-id="92402-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="92402-114">Description</span></span>                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="92402-115">\_aplicativo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="92402-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="92402-116">Especifica a lista de certificados revogados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92402-116">Specifies the application certificate revocation list.</span></span>                                     |
| <span data-ttu-id="92402-117">\_dispositivo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="92402-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="92402-118">Especifica a lista de certificados revogados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92402-118">Specifies the device certificate revocation list.</span></span>                                          |
| <span data-ttu-id="92402-119">WMDRM \_ RErevocationtype \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="92402-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="92402-120">Especifica a lista de revogação de certificados do Microsoft Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="92402-120">Specifies the Microsoft Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="92402-121">*pbCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92402-121">*pbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92402-122">Buffer que contém o certificado a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="92402-122">Buffer containing the certificate to look up.</span></span>

</dd> <dt>

<span data-ttu-id="92402-123">*cbCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92402-123">*cbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92402-124">Tamanho do buffer *pbCert*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="92402-124">Size of the buffer *pbCert*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="92402-125">*fRevoked* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="92402-125">*fRevoked* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92402-126">Na saída, indica se o certificado está presente na lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="92402-126">On output, indicates whether the certificate is present in the revocation list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92402-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92402-127">Return value</span></span>

<span data-ttu-id="92402-128">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="92402-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="92402-129">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="92402-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="92402-130">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="92402-130">Return code</span></span>                                                                          | <span data-ttu-id="92402-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="92402-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="92402-132"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="92402-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="92402-133">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="92402-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="92402-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92402-134">Requirements</span></span>



| <span data-ttu-id="92402-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="92402-135">Requirement</span></span> | <span data-ttu-id="92402-136">Valor</span><span class="sxs-lookup"><span data-stu-id="92402-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92402-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92402-137">Header</span></span><br/>  | <dl> <span data-ttu-id="92402-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="92402-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="92402-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92402-139">Library</span></span><br/> | <dl> <span data-ttu-id="92402-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92402-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92402-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="92402-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92402-142">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="92402-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





