---
title: Método IWMDRMLicense PersistLicense (wmdrmsdk. h)
description: O método PersistLicense salva a licença atual do repositório temporário no armazenamento de licença local permanente.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Formato de mídia do Windows do método PersistLicense
- Método PersistLicense Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método PersistLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771549"
---
# <a name="iwmdrmlicensepersistlicense-method"></a><span data-ttu-id="39c1e-106">IWMDRMLicense: método ersistLicense de:P</span><span class="sxs-lookup"><span data-stu-id="39c1e-106">IWMDRMLicense::PersistLicense method</span></span>

<span data-ttu-id="39c1e-107">O método **PersistLicense** salva a licença atual do repositório temporário no armazenamento de licença local permanente.</span><span class="sxs-lookup"><span data-stu-id="39c1e-107">The **PersistLicense** method saves the current license from the temporary store into the permanent local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c1e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39c1e-108">Syntax</span></span>


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a><span data-ttu-id="39c1e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39c1e-109">Parameters</span></span>

<span data-ttu-id="39c1e-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="39c1e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39c1e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39c1e-111">Return value</span></span>

<span data-ttu-id="39c1e-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="39c1e-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="39c1e-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="39c1e-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="39c1e-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="39c1e-114">Return code</span></span>                                                                          | <span data-ttu-id="39c1e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="39c1e-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="39c1e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="39c1e-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="39c1e-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="39c1e-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39c1e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="39c1e-118">Remarks</span></span>

<span data-ttu-id="39c1e-119">Se a licença atual não estiver no repositório temporário, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="39c1e-119">If the current license is not in the temporary store, this method will fail.</span></span>

<span data-ttu-id="39c1e-120">Você pode chamar [**cancontinue**](iwmdrmlicense-canpersist.md) para consultar se a licença tem permissão para ser persistente.</span><span class="sxs-lookup"><span data-stu-id="39c1e-120">You can call [**CanPersist**](iwmdrmlicense-canpersist.md) to query whether the license is allowed to be persisted.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c1e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c1e-121">Requirements</span></span>



| <span data-ttu-id="39c1e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c1e-122">Requirement</span></span> | <span data-ttu-id="39c1e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="39c1e-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39c1e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39c1e-124">Header</span></span><br/> | <dl> <span data-ttu-id="39c1e-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c1e-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c1e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="39c1e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c1e-127">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="39c1e-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





