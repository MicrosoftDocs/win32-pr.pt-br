---
title: Estrutura WMDRMCryptoData (wmdrmsdk. h)
description: A estrutura WMDRMCryptoData contém informações sobre o algoritmo criptográfico usado para criptografar e descriptografar conteúdo.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Formato de mídia do Windows da estrutura WMDRMCryptoData
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760493"
---
# <a name="wmdrmcryptodata-structure"></a><span data-ttu-id="d5599-105">Estrutura WMDRMCryptoData</span><span class="sxs-lookup"><span data-stu-id="d5599-105">WMDRMCryptoData structure</span></span>

<span data-ttu-id="d5599-106">A estrutura **WMDRMCryptoData** contém informações sobre o algoritmo criptográfico usado para criptografar e descriptografar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d5599-106">The **WMDRMCryptoData** structure contains information about the cryptographic algorithm used to encrypt and decrypt content.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5599-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5599-107">Syntax</span></span>


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a><span data-ttu-id="d5599-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d5599-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d5599-109">**cryptotype**</span><span class="sxs-lookup"><span data-stu-id="d5599-109">**cryptoType**</span></span>
</dt> <dd>

<span data-ttu-id="d5599-110">Membro da enumeração [**do \_ \_ tipo de criptografia DRM**](drm-crypto-type.md) especificando o tipo de algoritmo criptográfico.</span><span class="sxs-lookup"><span data-stu-id="d5599-110">Member of the [**DRM\_CRYPTO\_TYPE**](drm-crypto-type.md) enumeration specifying the type of cryptographic algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="d5599-111">**qwCounterID**</span><span class="sxs-lookup"><span data-stu-id="d5599-111">**qwCounterID**</span></span>
</dt> <dd>

<span data-ttu-id="d5599-112">Os bits de 64 altos do modo de contador AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d5599-112">The high 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="d5599-113">Esse membro só será usado se o membro **cryptotype** estiver definido como **crypto \_ Type \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="d5599-113">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> <dt>

<span data-ttu-id="d5599-114">**qwOffset**</span><span class="sxs-lookup"><span data-stu-id="d5599-114">**qwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d5599-115">Os poucos 64 bits do modo de contador AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d5599-115">The low 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="d5599-116">Esse membro só será usado se o membro **cryptotype** estiver definido como **crypto \_ Type \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="d5599-116">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5599-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5599-117">Requirements</span></span>



| <span data-ttu-id="d5599-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5599-118">Requirement</span></span> | <span data-ttu-id="d5599-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d5599-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5599-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5599-120">Header</span></span><br/> | <dl> <span data-ttu-id="d5599-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5599-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5599-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5599-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5599-123">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="d5599-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





