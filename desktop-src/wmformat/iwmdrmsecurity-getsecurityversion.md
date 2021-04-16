---
title: Método IWMDRMSecurity GetSecurityVersion (wmdrmsdk. h)
description: O método GetSecurityVersion recupera a versão do subsistema DRM no computador cliente.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Formato de mídia do Windows do método GetSecurityVersion
- Método GetSecurityVersion Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetSecurityVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750876"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a><span data-ttu-id="319a7-106">Método IWMDRMSecurity:: GetSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="319a7-106">IWMDRMSecurity::GetSecurityVersion method</span></span>

<span data-ttu-id="319a7-107">O método **GetSecurityVersion** recupera a versão do subsistema DRM no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="319a7-107">The **GetSecurityVersion** method retrieves the version of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="319a7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="319a7-108">Syntax</span></span>


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a><span data-ttu-id="319a7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="319a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="319a7-110">*pbstrVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="319a7-110">*pbstrVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="319a7-111">Endereço de uma variável que recebe o número de versão do subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="319a7-111">Address of a variable that receives the DRM subsystem version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="319a7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="319a7-112">Return value</span></span>

<span data-ttu-id="319a7-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="319a7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="319a7-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="319a7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="319a7-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="319a7-115">Return code</span></span>                                                                          | <span data-ttu-id="319a7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="319a7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="319a7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="319a7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="319a7-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="319a7-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="319a7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="319a7-119">Remarks</span></span>

<span data-ttu-id="319a7-120">O número de versão é expresso como uma cadeia de caracteres que consiste em quatro números separados por pontos.</span><span class="sxs-lookup"><span data-stu-id="319a7-120">The version number is expressed as a string consisting of four numbers separated by periods.</span></span> <span data-ttu-id="319a7-121">O primeiro número é o número de versão principal, que geralmente é definido como 2.</span><span class="sxs-lookup"><span data-stu-id="319a7-121">The first number is the major version number, which is usually set to 2.</span></span> <span data-ttu-id="319a7-122">O segundo número é o número de versão secundário, variando de 2 a 10.</span><span class="sxs-lookup"><span data-stu-id="319a7-122">The second number is the minor version number, ranging from 2 to 10.</span></span> <span data-ttu-id="319a7-123">O terceiro número é sempre definido como 0.</span><span class="sxs-lookup"><span data-stu-id="319a7-123">The third number is always set to 0.</span></span> <span data-ttu-id="319a7-124">O quarto número é definido como 0 ou 1 e é um valor booliano que indica se o subsistema foi individualizado.</span><span class="sxs-lookup"><span data-stu-id="319a7-124">The fourth number is set to 0 or 1, and is a Boolean value indicating whether the subsystem has been individualized.</span></span> <span data-ttu-id="319a7-125">Por exemplo, um número de versão de "2.4.0.1" indica a quarta versão secundária individual da segunda versão principal.</span><span class="sxs-lookup"><span data-stu-id="319a7-125">For example, a version number of "2.4.0.1" indicates the individualized fourth minor version of the second major version.</span></span>

## <a name="requirements"></a><span data-ttu-id="319a7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="319a7-126">Requirements</span></span>



| <span data-ttu-id="319a7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="319a7-127">Requirement</span></span> | <span data-ttu-id="319a7-128">Valor</span><span class="sxs-lookup"><span data-stu-id="319a7-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="319a7-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="319a7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="319a7-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="319a7-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="319a7-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="319a7-131">Library</span></span><br/> | <dl> <span data-ttu-id="319a7-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="319a7-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="319a7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="319a7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="319a7-134">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="319a7-134">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





