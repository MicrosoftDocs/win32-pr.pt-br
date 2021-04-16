---
title: Método Decrypt IWMDRMDecrypt (wmdrmsdk. h)
description: O método Decrypt descriptografa um buffer de dados no local.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Método Decrypt Windows Media Format
- Método Decrypt Windows Media Format, interface IWMDRMDecrypt
- IWMDRMDecrypt interface formato Windows Media, método Decrypt
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765076"
---
# <a name="iwmdrmdecryptdecrypt-method"></a><span data-ttu-id="986df-106">IWMDRMDecrypt: método ecrypt de:D</span><span class="sxs-lookup"><span data-stu-id="986df-106">IWMDRMDecrypt::Decrypt method</span></span>

<span data-ttu-id="986df-107">O método **Decrypt** descriptografa um buffer de dados no local.</span><span class="sxs-lookup"><span data-stu-id="986df-107">The **Decrypt** method decrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="986df-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="986df-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="986df-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="986df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="986df-110">*pbData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="986df-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="986df-111">Dados a serem descriptografados.</span><span class="sxs-lookup"><span data-stu-id="986df-111">Data to be decrypted.</span></span> <span data-ttu-id="986df-112">Se o método tiver sucesso, esses dados serão descriptografados no retorno.</span><span class="sxs-lookup"><span data-stu-id="986df-112">If the method succeeds, this data is decrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="986df-113">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="986df-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="986df-114">Tamanho dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="986df-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="986df-115">*pWMCryptoData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="986df-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="986df-116">Ponteiro para uma estrutura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contém parâmetros extras.</span><span class="sxs-lookup"><span data-stu-id="986df-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="986df-117">Pode ser **NULL** se o conteúdo foi criptografado usando os parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="986df-117">Can be **NULL** if the content was encrypted using the default parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="986df-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="986df-118">Return value</span></span>

<span data-ttu-id="986df-119">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="986df-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="986df-120">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="986df-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="986df-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="986df-121">Return code</span></span>                                                                          | <span data-ttu-id="986df-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="986df-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="986df-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="986df-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="986df-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="986df-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="986df-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="986df-125">Remarks</span></span>

<span data-ttu-id="986df-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="986df-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="986df-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="986df-127">Requirements</span></span>



| <span data-ttu-id="986df-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="986df-128">Requirement</span></span> | <span data-ttu-id="986df-129">Valor</span><span class="sxs-lookup"><span data-stu-id="986df-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="986df-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="986df-130">Header</span></span><br/> | <dl> <span data-ttu-id="986df-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="986df-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="986df-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="986df-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986df-133">**Interface IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="986df-133">**IWMDRMDecrypt Interface**</span></span>](iwmdrmdecrypt.md)
</dt> <dt>

[<span data-ttu-id="986df-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="986df-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





