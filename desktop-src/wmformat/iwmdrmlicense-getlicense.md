---
title: Método GetLicense do IWMDRMLicense (wmdrmsdk. h)
description: O método GetLicense recupera a licença como dados XML ou XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Método GetLicense Windows Media Format
- Método GetLicense Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows da interface IWMDRMLicense, método GetLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773063"
---
# <a name="iwmdrmlicensegetlicense-method"></a><span data-ttu-id="0480c-106">Método IWMDRMLicense:: GetLicense</span><span class="sxs-lookup"><span data-stu-id="0480c-106">IWMDRMLicense::GetLicense method</span></span>

<span data-ttu-id="0480c-107">O método **GetLicense** recupera a licença como dados XML ou XMR.</span><span class="sxs-lookup"><span data-stu-id="0480c-107">The **GetLicense** method retrieves the license as XML or XMR data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0480c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0480c-108">Syntax</span></span>


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a><span data-ttu-id="0480c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0480c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0480c-110">*ppbLicense* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0480c-110">*ppbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0480c-111">Recebe a licença.</span><span class="sxs-lookup"><span data-stu-id="0480c-111">Receives the license.</span></span>

</dd> <dt>

<span data-ttu-id="0480c-112">*pcbLicense* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0480c-112">*pcbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0480c-113">Recebe o tamanho da licença.</span><span class="sxs-lookup"><span data-stu-id="0480c-113">Receives the size of the license.</span></span>

</dd> <dt>

<span data-ttu-id="0480c-114">*pdwLicenseType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0480c-114">*pdwLicenseType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0480c-115">Recebe o tipo da licença retornada.</span><span class="sxs-lookup"><span data-stu-id="0480c-115">Receives the type of the license returned.</span></span> <span data-ttu-id="0480c-116">Esse valor é definido como uma das constantes na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0480c-116">This value is set to one of the constants in the following table.</span></span>



| <span data-ttu-id="0480c-117">Constante</span><span class="sxs-lookup"><span data-stu-id="0480c-117">Constant</span></span>                  | <span data-ttu-id="0480c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0480c-118">Description</span></span>                            |
|---------------------------|----------------------------------------|
| <span data-ttu-id="0480c-119">tipo de licença do WMDRM \_ \_ \_ XML</span><span class="sxs-lookup"><span data-stu-id="0480c-119">WMDRM\_LICENSE\_TYPE\_XML</span></span> | <span data-ttu-id="0480c-120">A licença recuperada é formatada como XML.</span><span class="sxs-lookup"><span data-stu-id="0480c-120">Retrieved license is formatted as XML.</span></span> |
| <span data-ttu-id="0480c-121">\_XMR do \_ tipo de licença WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="0480c-121">WMDRM\_LICENSE\_TYPE\_XMR</span></span> | <span data-ttu-id="0480c-122">A licença recuperada é formatada como XMR.</span><span class="sxs-lookup"><span data-stu-id="0480c-122">Retrieved license is formatted as XMR.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0480c-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0480c-123">Return value</span></span>

<span data-ttu-id="0480c-124">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0480c-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0480c-125">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0480c-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0480c-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0480c-126">Return code</span></span>                                                                          | <span data-ttu-id="0480c-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="0480c-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0480c-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0480c-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0480c-129">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0480c-129">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0480c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="0480c-130">Remarks</span></span>

<span data-ttu-id="0480c-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0480c-131">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0480c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0480c-132">Requirements</span></span>



| <span data-ttu-id="0480c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0480c-133">Requirement</span></span> | <span data-ttu-id="0480c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="0480c-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0480c-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0480c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="0480c-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0480c-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="0480c-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0480c-137">Library</span></span><br/> | <dl> <span data-ttu-id="0480c-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0480c-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0480c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="0480c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0480c-140">**Getlicenciadoproperty**</span><span class="sxs-lookup"><span data-stu-id="0480c-140">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[<span data-ttu-id="0480c-141">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="0480c-141">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





