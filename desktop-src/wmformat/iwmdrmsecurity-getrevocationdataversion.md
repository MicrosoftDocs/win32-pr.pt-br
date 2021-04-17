---
title: Método IWMDRMSecurity GetRevocationDataVersion (wmdrmsdk. h)
description: O método GetRevocationDataVersion recupera o número de versão de uma lista de certificados revogados no repositório local.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Formato de mídia do Windows do método GetRevocationDataVersion
- Método GetRevocationDataVersion Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetRevocationDataVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754694"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a><span data-ttu-id="bfb13-106">Método IWMDRMSecurity:: GetRevocationDataVersion</span><span class="sxs-lookup"><span data-stu-id="bfb13-106">IWMDRMSecurity::GetRevocationDataVersion method</span></span>

<span data-ttu-id="bfb13-107">O método **GetRevocationDataVersion** recupera o número de versão de uma lista de certificados revogados no repositório local.</span><span class="sxs-lookup"><span data-stu-id="bfb13-107">The **GetRevocationDataVersion** method retrieves the version number of a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb13-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfb13-108">Syntax</span></span>


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a><span data-ttu-id="bfb13-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfb13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfb13-110">*f \_ guidRevocationType* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="bfb13-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb13-111">GUID que especifica o tipo de lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="bfb13-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="bfb13-112">Defina como uma das constantes na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfb13-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="bfb13-113">Constante de GUID</span><span class="sxs-lookup"><span data-stu-id="bfb13-113">GUID constant</span></span>                 | <span data-ttu-id="bfb13-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfb13-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bfb13-115">\_aplicativo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="bfb13-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="bfb13-116">Especifica a lista de certificados revogados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfb13-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="bfb13-117">\_dispositivo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="bfb13-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="bfb13-118">Especifica a lista de certificados revogados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfb13-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="bfb13-119">WMDRM \_ RErevocationtype \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="bfb13-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="bfb13-120">Especifica a lista de revogação de certificados do Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="bfb13-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="bfb13-121">saída de *f \_ pdwCRLVersion* \[\]</span><span class="sxs-lookup"><span data-stu-id="bfb13-121">*f\_pdwCRLVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb13-122">Variável que recebe o número de versão.</span><span class="sxs-lookup"><span data-stu-id="bfb13-122">Variable that receives the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfb13-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bfb13-123">Return value</span></span>

<span data-ttu-id="bfb13-124">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bfb13-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bfb13-125">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfb13-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bfb13-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bfb13-126">Return code</span></span>                                                                          | <span data-ttu-id="bfb13-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfb13-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bfb13-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bfb13-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bfb13-129">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bfb13-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bfb13-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfb13-130">Requirements</span></span>



| <span data-ttu-id="bfb13-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfb13-131">Requirement</span></span> | <span data-ttu-id="bfb13-132">Valor</span><span class="sxs-lookup"><span data-stu-id="bfb13-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb13-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bfb13-133">Header</span></span><br/>  | <dl> <span data-ttu-id="bfb13-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfb13-134"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfb13-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfb13-135">Library</span></span><br/> | <dl> <span data-ttu-id="bfb13-136"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfb13-136"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfb13-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfb13-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb13-138">**Revogação e renovação de componentes automatizados**</span><span class="sxs-lookup"><span data-stu-id="bfb13-138">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="bfb13-139">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="bfb13-139">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="bfb13-140">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="bfb13-140">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="bfb13-141">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="bfb13-141">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





