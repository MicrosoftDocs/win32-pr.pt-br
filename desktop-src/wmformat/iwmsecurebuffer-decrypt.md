---
title: Método Decrypt IWMSecureBuffer (wmdrmsdk. h)
description: O método Decrypt descriptografa um ponteiro de dados que foi criptografado chamando o método Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Método Decrypt Windows Media Format
- Método Decrypt Windows Media Format, interface IWMSecureBuffer
- IWMSecureBuffer interface formato Windows Media, método Decrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780557"
---
# <a name="iwmsecurebufferdecrypt-method"></a><span data-ttu-id="89ef6-106">IWMSecureBuffer: método ecrypt de:D</span><span class="sxs-lookup"><span data-stu-id="89ef6-106">IWMSecureBuffer::Decrypt method</span></span>

<span data-ttu-id="89ef6-107">O método **Decrypt** descriptografa um ponteiro de dados que foi criptografado chamando o método [**Encrypt**](iwmsecurebuffer-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="89ef6-107">The **Decrypt** method decrypts a data pointer that was encrypted by calling the [**Encrypt**](iwmsecurebuffer-encrypt.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89ef6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89ef6-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="89ef6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89ef6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89ef6-110">*pSecureChannel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89ef6-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ef6-111">Ponteiro para uma interface de canal segura que contém o ponteiro de dados criptografados.</span><span class="sxs-lookup"><span data-stu-id="89ef6-111">Pointer to a secure channel interface containing the encrypted data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89ef6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89ef6-112">Return value</span></span>

<span data-ttu-id="89ef6-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="89ef6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="89ef6-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="89ef6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="89ef6-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="89ef6-115">Return code</span></span>                                                                          | <span data-ttu-id="89ef6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="89ef6-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="89ef6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89ef6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="89ef6-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="89ef6-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89ef6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="89ef6-119">Remarks</span></span>

<span data-ttu-id="89ef6-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="89ef6-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ef6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89ef6-121">Requirements</span></span>



| <span data-ttu-id="89ef6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="89ef6-122">Requirement</span></span> | <span data-ttu-id="89ef6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="89ef6-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89ef6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89ef6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="89ef6-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="89ef6-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="89ef6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89ef6-126">Library</span></span><br/> | <dl> <span data-ttu-id="89ef6-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89ef6-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89ef6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="89ef6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ef6-129">**Encrypt**</span><span class="sxs-lookup"><span data-stu-id="89ef6-129">**Encrypt**</span></span>](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[<span data-ttu-id="89ef6-130">**Interface IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="89ef6-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





