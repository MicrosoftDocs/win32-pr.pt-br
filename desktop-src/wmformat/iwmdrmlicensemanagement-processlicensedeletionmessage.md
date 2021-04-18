---
title: Método IWMDRMLicenseManagement ProcessLicenseDeletionMessage (wmdrmsdk. h)
description: O método ProcessLicenseDeletion exclui uma licença que foi importada para o conteúdo originalmente protegido com outro sistema de proteção de conteúdo.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Formato de mídia do Windows do método ProcessLicenseDeletionMessage
- Método ProcessLicenseDeletionMessage Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método ProcessLicenseDeletionMessage
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798175"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a><span data-ttu-id="1daf2-106">IWMDRMLicenseManagement: método rocessLicenseDeletionMessage de:P</span><span class="sxs-lookup"><span data-stu-id="1daf2-106">IWMDRMLicenseManagement::ProcessLicenseDeletionMessage method</span></span>

<span data-ttu-id="1daf2-107">O método **ProcessLicenseDeletion** exclui uma licença que foi importada para o conteúdo originalmente protegido com outro sistema de proteção de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1daf2-107">The **ProcessLicenseDeletion** method deletes a license that was imported for content originally protected with another content protection system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1daf2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1daf2-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a><span data-ttu-id="1daf2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1daf2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1daf2-110">*bstrDeletionMessage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1daf2-110">*bstrDeletionMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daf2-111">Mensagem que identifica a licença a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="1daf2-111">Message identifying the license to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1daf2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1daf2-112">Return value</span></span>

<span data-ttu-id="1daf2-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1daf2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1daf2-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1daf2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1daf2-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1daf2-115">Return code</span></span>                                                                          | <span data-ttu-id="1daf2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1daf2-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1daf2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1daf2-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1daf2-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1daf2-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1daf2-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1daf2-119">Remarks</span></span>

<span data-ttu-id="1daf2-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1daf2-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="1daf2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1daf2-121">Requirements</span></span>



| <span data-ttu-id="1daf2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1daf2-122">Requirement</span></span> | <span data-ttu-id="1daf2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1daf2-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1daf2-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1daf2-124">Header</span></span><br/> | <dl> <span data-ttu-id="1daf2-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1daf2-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1daf2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1daf2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1daf2-127">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="1daf2-127">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





