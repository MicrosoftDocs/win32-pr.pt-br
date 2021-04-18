---
description: Inicia o hash de um fluxo de dados.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: Função A_SHAInit (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811062"
---
# <a name="a_shainit-function"></a><span data-ttu-id="b8d22-103">Uma \_ função SHAInit</span><span class="sxs-lookup"><span data-stu-id="b8d22-103">A\_SHAInit function</span></span>

<span data-ttu-id="b8d22-104">Inicia o hash de um fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="b8d22-104">Initiates the hashing of a stream of data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8d22-105">Syntax</span></span>


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a><span data-ttu-id="b8d22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8d22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d22-107">*Contexto* \[ do entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b8d22-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d22-108">O contexto do SHA.</span><span class="sxs-lookup"><span data-stu-id="b8d22-108">The SHA context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d22-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8d22-109">Return value</span></span>

<span data-ttu-id="b8d22-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b8d22-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d22-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8d22-111">Remarks</span></span>

<span data-ttu-id="b8d22-112">Essa função é muito semelhante a SHAInit, mas é chamada diretamente da biblioteca, em vez de ser roteada pela infraestrutura de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b8d22-112">This function is very similar to SHAInit, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="b8d22-113">Para obter mais informações, consulte [provedores do Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="b8d22-113">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d22-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8d22-114">Requirements</span></span>



| <span data-ttu-id="b8d22-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8d22-115">Requirement</span></span> | <span data-ttu-id="b8d22-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b8d22-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d22-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8d22-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b8d22-118"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8d22-118"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="b8d22-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8d22-119">Library</span></span><br/> | <dl> <span data-ttu-id="b8d22-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8d22-120"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="b8d22-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b8d22-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8d22-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8d22-122"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
