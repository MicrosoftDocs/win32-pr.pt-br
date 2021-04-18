---
title: Método Encrypt de IWMDRMEncrypt (wmdrmsdk. h)
description: O método Encrypt criptografa um buffer de dados no local.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Método Encrypt Windows Media Format
- Método Encrypt Windows Media Format, interface IWMDRMEncrypt
- Formato de mídia do Windows da interface IWMDRMEncrypt, método Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787756"
---
# <a name="iwmdrmencryptencrypt-method"></a><span data-ttu-id="f6722-106">Método IWMDRMEncrypt:: Encrypt</span><span class="sxs-lookup"><span data-stu-id="f6722-106">IWMDRMEncrypt::Encrypt method</span></span>

<span data-ttu-id="f6722-107">O método **Encrypt** criptografa um buffer de dados no local.</span><span class="sxs-lookup"><span data-stu-id="f6722-107">The **Encrypt** method encrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6722-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6722-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="f6722-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6722-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6722-110">*pbData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f6722-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6722-111">Dados a serem criptografados.</span><span class="sxs-lookup"><span data-stu-id="f6722-111">Data to encrypt.</span></span> <span data-ttu-id="f6722-112">Se o método tiver sucesso, os dados serão criptografados no retorno.</span><span class="sxs-lookup"><span data-stu-id="f6722-112">If the method succeeds, the data is encrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="f6722-113">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6722-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6722-114">Tamanho dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="f6722-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f6722-115">*pWMCryptoData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6722-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6722-116">Ponteiro para uma estrutura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contém parâmetros extras.</span><span class="sxs-lookup"><span data-stu-id="f6722-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="f6722-117">Defina como **nulo** para usar os valores de criptografia padrão.</span><span class="sxs-lookup"><span data-stu-id="f6722-117">Set to **NULL** to use the default encryption values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6722-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6722-118">Return value</span></span>

<span data-ttu-id="f6722-119">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f6722-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f6722-120">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6722-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f6722-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f6722-121">Return code</span></span>                                                                          | <span data-ttu-id="f6722-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6722-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f6722-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f6722-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f6722-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f6722-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6722-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6722-125">Remarks</span></span>

<span data-ttu-id="f6722-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f6722-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6722-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6722-127">Requirements</span></span>



| <span data-ttu-id="f6722-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6722-128">Requirement</span></span> | <span data-ttu-id="f6722-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f6722-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6722-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6722-130">Header</span></span><br/> | <dl> <span data-ttu-id="f6722-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6722-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6722-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6722-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6722-133">**Interface IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="f6722-133">**IWMDRMEncrypt Interface**</span></span>](iwmdrmencrypt.md)
</dt> <dt>

[<span data-ttu-id="f6722-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="f6722-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





