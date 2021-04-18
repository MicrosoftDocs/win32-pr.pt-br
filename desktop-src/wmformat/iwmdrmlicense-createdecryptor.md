---
title: Método createdescriptografar IWMDRMLicense (wmdrmsdk. h)
description: O método createdecryptr cria um objeto de descriptografia usando as configurações da licença atual.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Método createdescriptografar formato de mídia do Windows
- Método createdescriptografar formato de mídia do Windows, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método createdescriptografar
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755266"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a><span data-ttu-id="9b737-106">Método IWMDRMLicense:: createdecryptr</span><span class="sxs-lookup"><span data-stu-id="9b737-106">IWMDRMLicense::CreateDecryptor method</span></span>

<span data-ttu-id="9b737-107">O método **Createdecryptr** cria um objeto de descriptografia usando as configurações da licença atual.</span><span class="sxs-lookup"><span data-stu-id="9b737-107">The **CreateDecryptor** method creates a decryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b737-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b737-108">Syntax</span></span>


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="9b737-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b737-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b737-110">*ppDecryptor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b737-110">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b737-111">Recebe um ponteiro para a interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) do objeto recém-criado.</span><span class="sxs-lookup"><span data-stu-id="9b737-111">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b737-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b737-112">Return value</span></span>

<span data-ttu-id="9b737-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9b737-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9b737-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b737-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9b737-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9b737-115">Return code</span></span>                                                                                                | <span data-ttu-id="9b737-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b737-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="9b737-117"><dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="9b737-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="9b737-118">Uma lista de revogação de conteúdo atualizada é necessária.</span><span class="sxs-lookup"><span data-stu-id="9b737-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="9b737-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9b737-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="9b737-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9b737-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="9b737-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b737-121">Remarks</span></span>

<span data-ttu-id="9b737-122">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9b737-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b737-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b737-123">Requirements</span></span>



| <span data-ttu-id="9b737-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b737-124">Requirement</span></span> | <span data-ttu-id="9b737-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9b737-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b737-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b737-126">Header</span></span><br/> | <dl> <span data-ttu-id="9b737-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b737-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b737-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b737-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b737-129">**Createcriptografer**</span><span class="sxs-lookup"><span data-stu-id="9b737-129">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[<span data-ttu-id="9b737-130">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="9b737-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





