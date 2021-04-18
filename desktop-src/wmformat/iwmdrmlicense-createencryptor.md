---
title: Método createencryptr IWMDRMLicense (wmdrmsdk. h)
description: O método createencryptr cria um objeto de criptografador usando as configurações da licença atual.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Método createencryptr formato de mídia do Windows
- Método createencryptr formato de mídia do Windows, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método createencryptr
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796210"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a><span data-ttu-id="77807-106">Método IWMDRMLicense:: createencryptr</span><span class="sxs-lookup"><span data-stu-id="77807-106">IWMDRMLicense::CreateEncryptor method</span></span>

<span data-ttu-id="77807-107">O método **Createencryptr** cria um objeto de criptografador usando as configurações da licença atual.</span><span class="sxs-lookup"><span data-stu-id="77807-107">The **CreateEncryptor** method creates an encryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="77807-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77807-108">Syntax</span></span>


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a><span data-ttu-id="77807-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77807-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77807-110">*ppEncryptor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="77807-110">*ppEncryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77807-111">Recebe um ponteiro para a interface [**IWMDRMEncrypt**](iwmdrmencrypt.md) do objeto recém-criado.</span><span class="sxs-lookup"><span data-stu-id="77807-111">Receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77807-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77807-112">Return value</span></span>

<span data-ttu-id="77807-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="77807-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="77807-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="77807-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="77807-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="77807-115">Return code</span></span>                                                                                                | <span data-ttu-id="77807-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="77807-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="77807-117"><dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="77807-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="77807-118">Uma lista de revogação de conteúdo atualizada é necessária.</span><span class="sxs-lookup"><span data-stu-id="77807-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="77807-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="77807-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="77807-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="77807-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="77807-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="77807-121">Remarks</span></span>

<span data-ttu-id="77807-122">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="77807-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="77807-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77807-123">Requirements</span></span>



| <span data-ttu-id="77807-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="77807-124">Requirement</span></span> | <span data-ttu-id="77807-125">Valor</span><span class="sxs-lookup"><span data-stu-id="77807-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77807-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77807-126">Header</span></span><br/> | <dl> <span data-ttu-id="77807-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="77807-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77807-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="77807-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77807-129">**Createdescriptografar**</span><span class="sxs-lookup"><span data-stu-id="77807-129">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[<span data-ttu-id="77807-130">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="77807-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





