---
title: Método Encrypt de IWMSecureBuffer (wmdrmsdk. h)
description: O método Encrypt criptografa um ponteiro de dados.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Método Encrypt Windows Media Format
- Método Encrypt Windows Media Format, interface IWMSecureBuffer
- Formato de mídia do Windows da interface IWMSecureBuffer, método Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782415"
---
# <a name="iwmsecurebufferencrypt-method"></a><span data-ttu-id="f16ea-106">Método IWMSecureBuffer:: Encrypt</span><span class="sxs-lookup"><span data-stu-id="f16ea-106">IWMSecureBuffer::Encrypt method</span></span>

<span data-ttu-id="f16ea-107">O método **Encrypt** criptografa um ponteiro de dados.</span><span class="sxs-lookup"><span data-stu-id="f16ea-107">The **Encrypt** method encrypts a data pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16ea-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f16ea-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="f16ea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f16ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f16ea-110">*pSecureChannel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f16ea-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16ea-111">Ponteiro para uma interface de canal segura que contém o ponteiro de dados para criptografar.</span><span class="sxs-lookup"><span data-stu-id="f16ea-111">Pointer to a secure channel interface containing the data pointer to encrypt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f16ea-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f16ea-112">Return value</span></span>

<span data-ttu-id="f16ea-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f16ea-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f16ea-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f16ea-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f16ea-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f16ea-115">Return code</span></span>                                                                          | <span data-ttu-id="f16ea-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f16ea-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f16ea-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f16ea-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f16ea-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f16ea-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f16ea-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f16ea-119">Remarks</span></span>

<span data-ttu-id="f16ea-120">Use este método para criptografar ponteiros de dados para que eles possam ser enviados entre limites de DLL.</span><span class="sxs-lookup"><span data-stu-id="f16ea-120">Use this method to encrypt data pointers so they can be sent across DLL boundaries.</span></span>

## <a name="requirements"></a><span data-ttu-id="f16ea-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f16ea-121">Requirements</span></span>



| <span data-ttu-id="f16ea-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16ea-122">Requirement</span></span> | <span data-ttu-id="f16ea-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f16ea-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f16ea-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f16ea-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f16ea-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16ea-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f16ea-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f16ea-126">Library</span></span><br/> | <dl> <span data-ttu-id="f16ea-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f16ea-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16ea-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f16ea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16ea-129">**Descriptografar**</span><span class="sxs-lookup"><span data-stu-id="f16ea-129">**Decrypt**</span></span>](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[<span data-ttu-id="f16ea-130">**Interface IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="f16ea-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





