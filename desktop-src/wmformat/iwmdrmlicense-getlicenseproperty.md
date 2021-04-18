---
title: Método getlicenciadoproperty IWMDRMLicense (wmdrmsdk. h)
description: O método getlicenciadoproperty recupera uma propriedade da licença atual.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Método getlicenciadoproperty Windows Media Format
- Método getlicenciadoproperty Windows Media Format, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método getlicenciadoproperty
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793274"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a><span data-ttu-id="68386-106">Método IWMDRMLicense:: getlicenseproperty</span><span class="sxs-lookup"><span data-stu-id="68386-106">IWMDRMLicense::GetLicenseProperty method</span></span>

<span data-ttu-id="68386-107">O método **Getlicenciadoproperty** recupera uma propriedade da licença atual.</span><span class="sxs-lookup"><span data-stu-id="68386-107">The **GetLicenseProperty** method retrieves a property from the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="68386-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68386-108">Syntax</span></span>


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a><span data-ttu-id="68386-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68386-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68386-110">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68386-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68386-111">Nome da propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="68386-111">Name of the property to retrieve.</span></span> <span data-ttu-id="68386-112">Defina como uma das constantes na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="68386-112">Set to one of the constants in the following table:</span></span>



| <span data-ttu-id="68386-113">Constante</span><span class="sxs-lookup"><span data-stu-id="68386-113">Constant</span></span>                   | <span data-ttu-id="68386-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="68386-114">Description</span></span>                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68386-115">\_wszWMDRMNet \_ revogação de g</span><span class="sxs-lookup"><span data-stu-id="68386-115">g\_wszWMDRMNet\_Revocation</span></span> | <span data-ttu-id="68386-116">Use para obter a lista de certificados do Windows Media DRM para dispositivos de rede para a licença atual.</span><span class="sxs-lookup"><span data-stu-id="68386-116">Use to get the Windows Media DRM for Network Devices revocation list for the current license.</span></span>                        |
| <span data-ttu-id="68386-117">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="68386-117">g\_wszWMDRM\_SAPLEVEL</span></span>      | <span data-ttu-id="68386-118">Use para obter o nível de caminho de áudio seguro (SAP) necessário para reproduzir o conteúdo coberto pela licença atual.</span><span class="sxs-lookup"><span data-stu-id="68386-118">Use to get the Secure Audio Path (SAP) level required to play content covered by the current license.</span></span>                |
| <span data-ttu-id="68386-119">g \_ wszWMDRM \_ SAPRequired</span><span class="sxs-lookup"><span data-stu-id="68386-119">g\_wszWMDRM\_SAPRequired</span></span>   | <span data-ttu-id="68386-120">Use para verificar se a licença atual requer que o SAP seja usado para reproduzir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="68386-120">Use to ascertain whether the current license requires SAP be used to play the content.</span></span>                               |
| <span data-ttu-id="68386-121">\_fonte de wszWMDRM g \_</span><span class="sxs-lookup"><span data-stu-id="68386-121">g\_wszWMDRM\_SOURCEID</span></span>      | <span data-ttu-id="68386-122">Use para obter o identificador de origem para a licença atual.</span><span class="sxs-lookup"><span data-stu-id="68386-122">Use to get the source identifier for the current license.</span></span>                                                            |
| <span data-ttu-id="68386-123">\_prioridade g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="68386-123">g\_wszWMDRM\_PRIORITY</span></span>      | <span data-ttu-id="68386-124">Use para obter a prioridade da licença atual.</span><span class="sxs-lookup"><span data-stu-id="68386-124">Use to get the priority of the current license.</span></span> <span data-ttu-id="68386-125">As licenças de prioridade mais alta são aplicadas antes das licenças de prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="68386-125">Higher priority licenses are applied before lower priority licenses.</span></span> |
| <span data-ttu-id="68386-126">g \_ wszWMDRM \_ uplinkid</span><span class="sxs-lookup"><span data-stu-id="68386-126">g\_wszWMDRM\_UplinkID</span></span>      | <span data-ttu-id="68386-127">Use para obter a ID de chave da licença raiz na cadeia de licença à qual a licença atual pertence.</span><span class="sxs-lookup"><span data-stu-id="68386-127">Use to get the key ID of the root license in the license chain that the current license belongs to.</span></span>                  |



 

</dd> <dt>

<span data-ttu-id="68386-128">*ppropVariant* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68386-128">*ppropVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68386-129">Recebe o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="68386-129">Receives the property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68386-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68386-130">Return value</span></span>

<span data-ttu-id="68386-131">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="68386-131">The method returns an **HRESULT**.</span></span> <span data-ttu-id="68386-132">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="68386-132">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="68386-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="68386-133">Return code</span></span>                                                                          | <span data-ttu-id="68386-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="68386-134">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="68386-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68386-135"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="68386-136">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="68386-136">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68386-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="68386-137">Remarks</span></span>

<span data-ttu-id="68386-138">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="68386-138">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="68386-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68386-139">Requirements</span></span>



| <span data-ttu-id="68386-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="68386-140">Requirement</span></span> | <span data-ttu-id="68386-141">Valor</span><span class="sxs-lookup"><span data-stu-id="68386-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68386-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68386-142">Header</span></span><br/>  | <dl> <span data-ttu-id="68386-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="68386-143"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="68386-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68386-144">Library</span></span><br/> | <dl> <span data-ttu-id="68386-145"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68386-145"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68386-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="68386-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68386-147">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="68386-147">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)
</dt> <dt>

[<span data-ttu-id="68386-148">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="68386-148">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





