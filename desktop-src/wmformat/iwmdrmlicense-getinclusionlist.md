---
title: Método IWMDRMLicense inclusionlist (wmdrmsdk. h)
description: O método getinclusõeslist recupera toda a lista de inclusão para a licença ou cadeia de licença atual.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Método inclusionlist formato de mídia do Windows
- Método getinclusõeslist Windows Media Format, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método getinclusõeslist
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797921"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a><span data-ttu-id="01fd4-106">Método IWMDRMLicense:: inclusionlist</span><span class="sxs-lookup"><span data-stu-id="01fd4-106">IWMDRMLicense::GetInclusionList method</span></span>

<span data-ttu-id="01fd4-107">O método **Getinclusõeslist** recupera toda a lista de inclusão para a licença ou cadeia de licença atual.</span><span class="sxs-lookup"><span data-stu-id="01fd4-107">The **GetInclusionList** method retrieves the entire inclusion list for the current license or license chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="01fd4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01fd4-108">Syntax</span></span>


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a><span data-ttu-id="01fd4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01fd4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fd4-110">*ppGuids* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01fd4-110">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01fd4-111">Recebe uma matriz de GUIDs que identifica as tecnologias incluídas.</span><span class="sxs-lookup"><span data-stu-id="01fd4-111">Receives an array of GUIDs identifying the included technologies.</span></span>

</dd> <dt>

<span data-ttu-id="01fd4-112">*pcGuids* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01fd4-112">*pcGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01fd4-113">Recebe o número de elementos na matriz *ppGuids* .</span><span class="sxs-lookup"><span data-stu-id="01fd4-113">Receives the number of elements in the *ppGuids* array.</span></span> <span data-ttu-id="01fd4-114">A matriz é alocada usando **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="01fd4-114">The array is allocated by using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="01fd4-115">Quando terminar com a lista, libere a memória chamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="01fd4-115">When finished with the list, release the memory by calling **CoTaskMemFree**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fd4-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01fd4-116">Return value</span></span>

<span data-ttu-id="01fd4-117">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="01fd4-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="01fd4-118">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01fd4-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="01fd4-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01fd4-119">Return code</span></span>                                                                          | <span data-ttu-id="01fd4-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="01fd4-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="01fd4-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01fd4-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="01fd4-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="01fd4-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="01fd4-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="01fd4-123">Remarks</span></span>

<span data-ttu-id="01fd4-124">O emissor da licença pode especificar outros sistemas de proteção para os quais o conteúdo criptografado pode ser convertido.</span><span class="sxs-lookup"><span data-stu-id="01fd4-124">The license issuer can specify other protection systems to which the encrypted content may be converted.</span></span> <span data-ttu-id="01fd4-125">A lista de GUIDs recuperados por esse método identifica os sistemas de proteção permitidos.</span><span class="sxs-lookup"><span data-stu-id="01fd4-125">The list of GUIDs retrieved by this method identifies the allowed protection systems.</span></span> <span data-ttu-id="01fd4-126">Ao entrar em um contrato de licença com a Microsoft para obter a biblioteca de stub, você receberá uma lista de sistemas de proteção com suporte no momento e os GUIDs usados para identificá-los.</span><span class="sxs-lookup"><span data-stu-id="01fd4-126">When you enter into a license agreement with Microsoft to get the stub library, you will receive a list of currently supported protection systems and the GUIDs used to identify them.</span></span>

## <a name="requirements"></a><span data-ttu-id="01fd4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01fd4-127">Requirements</span></span>



| <span data-ttu-id="01fd4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="01fd4-128">Requirement</span></span> | <span data-ttu-id="01fd4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="01fd4-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01fd4-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01fd4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="01fd4-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="01fd4-131"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="01fd4-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01fd4-132">Library</span></span><br/> | <dl> <span data-ttu-id="01fd4-133"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01fd4-133"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01fd4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="01fd4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01fd4-135">**Autorização explícita e listas de inclusão**</span><span class="sxs-lookup"><span data-stu-id="01fd4-135">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="01fd4-136">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="01fd4-136">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





