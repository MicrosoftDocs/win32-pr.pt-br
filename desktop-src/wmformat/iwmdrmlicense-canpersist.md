---
title: Método canpersist do IWMDRMLicense (wmdrmsdk. h)
description: O método canpersist consulta se a licença pode persistir em um repositório de licenças local.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Método perpersist Windows Media Format
- Método canpersist Windows Media Format, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método perpersist
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773076"
---
# <a name="iwmdrmlicensecanpersist-method"></a><span data-ttu-id="ee735-106">Método IWMDRMLicense:: perpersist</span><span class="sxs-lookup"><span data-stu-id="ee735-106">IWMDRMLicense::CanPersist method</span></span>

<span data-ttu-id="ee735-107">O método **canpersist** consulta se a licença pode persistir em um repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="ee735-107">The **CanPersist** method queries whether the license can be persisted on in a local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee735-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee735-108">Syntax</span></span>


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a><span data-ttu-id="ee735-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee735-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee735-110">*pfCanPersist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee735-110">*pfCanPersist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-111">VERDADEIRO indica que a licença pode ser persistida.</span><span class="sxs-lookup"><span data-stu-id="ee735-111">TRUE indicates that the license can be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee735-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee735-112">Return value</span></span>

<span data-ttu-id="ee735-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ee735-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ee735-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee735-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ee735-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ee735-115">Return code</span></span>                                                                          | <span data-ttu-id="ee735-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee735-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ee735-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ee735-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ee735-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee735-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee735-119">Remarks</span></span>

<span data-ttu-id="ee735-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ee735-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee735-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee735-121">Requirements</span></span>



| <span data-ttu-id="ee735-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee735-122">Requirement</span></span> | <span data-ttu-id="ee735-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ee735-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee735-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee735-124">Header</span></span><br/> | <dl> <span data-ttu-id="ee735-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee735-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee735-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee735-127">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="ee735-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





