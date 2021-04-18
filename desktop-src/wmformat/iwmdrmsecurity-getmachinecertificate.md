---
title: Método IWMDRMSecurity GetMachineCertificate (wmdrmsdk. h)
description: O método GetMachineCertificate recupera o certificado do computador do subsistema DRM no computador cliente.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Formato de mídia do Windows do método GetMachineCertificate
- Método GetMachineCertificate Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetMachineCertificate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752156"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a><span data-ttu-id="79592-106">Método IWMDRMSecurity:: GetMachineCertificate</span><span class="sxs-lookup"><span data-stu-id="79592-106">IWMDRMSecurity::GetMachineCertificate method</span></span>

<span data-ttu-id="79592-107">O método **GetMachineCertificate** recupera o certificado do computador do subsistema DRM no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="79592-107">The **GetMachineCertificate** method retrieves the machine certificate of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="79592-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79592-108">Syntax</span></span>


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="79592-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79592-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79592-110">*dwCertificateType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79592-110">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79592-111">Tipo de certificado a recuperar.</span><span class="sxs-lookup"><span data-stu-id="79592-111">Type of certificate to retrieve.</span></span> <span data-ttu-id="79592-112">Defina como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="79592-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="79592-113">Valor</span><span class="sxs-lookup"><span data-stu-id="79592-113">Value</span></span>                        | <span data-ttu-id="79592-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="79592-114">Description</span></span>                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79592-115">\_Tipo de certificado WMDRM \_ \_ v1</span><span class="sxs-lookup"><span data-stu-id="79592-115">WMDRM\_CERTIFICATE\_TYPE\_V1</span></span> | <span data-ttu-id="79592-116">O certificado será recuperado no formato usado por componentes herdados.</span><span class="sxs-lookup"><span data-stu-id="79592-116">The certificate will be retrieved in the format used by legacy components.</span></span>            |
| <span data-ttu-id="79592-117">\_Tipo de certificado WMDRM \_ \_ v2</span><span class="sxs-lookup"><span data-stu-id="79592-117">WMDRM\_CERTIFICATE\_TYPE\_V2</span></span> | <span data-ttu-id="79592-118">O certificado será recuperado no formato usado pelos componentes do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="79592-118">The certificate will be retrieved in the format used by the Windows Vista components.</span></span> |



 

</dd> <dt>

<span data-ttu-id="79592-119">saída de *rgbVersion \[ 4 \]* \[\]</span><span class="sxs-lookup"><span data-stu-id="79592-119">*rgbVersion\[4\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79592-120">Matriz de quatro bytes especificando a versão do subsistema DRM no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="79592-120">Array of four bytes specifying the version of the DRM subsystem on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="79592-121">*ppbCertificate* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="79592-121">*ppbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79592-122">Endereço de uma variável que recebe um ponteiro para os dados do certificado.</span><span class="sxs-lookup"><span data-stu-id="79592-122">Address of a variable that receives a pointer to the certificate data.</span></span> <span data-ttu-id="79592-123">Defina como **NULL** para que o método forneça o tamanho do buffer necessário para manter o certificado em *pcbCertificate*.</span><span class="sxs-lookup"><span data-stu-id="79592-123">Set to **NULL** to have the method provide the buffer size required to hold the certificate in *pcbCertificate*.</span></span>

</dd> <dt>

<span data-ttu-id="79592-124">*pcbCertificate* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="79592-124">*pcbCertificate* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="79592-125">Tamanho do certificado em bytes.</span><span class="sxs-lookup"><span data-stu-id="79592-125">Size of the certificate in bytes.</span></span> <span data-ttu-id="79592-126">Se *ppbCertificate* for **NULL**, esse valor será definido como o tamanho do certificado.</span><span class="sxs-lookup"><span data-stu-id="79592-126">If *ppbCertificate* is **NULL**, this value will be set to the size of the certificate.</span></span> <span data-ttu-id="79592-127">Se *ppbCertificate* não for **NULL**, esse valor deverá ser definido como o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="79592-127">If *ppbCertificate* is not **NULL**, this value must be set to the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79592-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79592-128">Return value</span></span>

<span data-ttu-id="79592-129">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="79592-129">The method returns an **HRESULT**.</span></span> <span data-ttu-id="79592-130">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="79592-130">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="79592-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="79592-131">Return code</span></span>                                                                          | <span data-ttu-id="79592-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="79592-132">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="79592-133"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79592-133"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="79592-134">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="79592-134">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79592-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79592-135">Requirements</span></span>



| <span data-ttu-id="79592-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="79592-136">Requirement</span></span> | <span data-ttu-id="79592-137">Valor</span><span class="sxs-lookup"><span data-stu-id="79592-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79592-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79592-138">Header</span></span><br/>  | <dl> <span data-ttu-id="79592-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="79592-139"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="79592-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79592-140">Library</span></span><br/> | <dl> <span data-ttu-id="79592-141"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79592-141"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79592-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="79592-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79592-143">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="79592-143">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





