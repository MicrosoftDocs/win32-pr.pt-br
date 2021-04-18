---
description: Computa o hash final dos dados inseridos pela função MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: Função A_SHAFinal (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756158"
---
# <a name="a_shafinal-function"></a><span data-ttu-id="6e5da-103">Uma \_ função SHAFinal</span><span class="sxs-lookup"><span data-stu-id="6e5da-103">A\_SHAFinal function</span></span>

<span data-ttu-id="6e5da-104">Computa o hash final dos dados inseridos pela função MD5Update.</span><span class="sxs-lookup"><span data-stu-id="6e5da-104">Computes the final hash of the data entered by the MD5Update function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5da-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e5da-105">Syntax</span></span>


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a><span data-ttu-id="6e5da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e5da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e5da-107">*Contexto* \[ do entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6e5da-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e5da-108">O contexto do SHA.</span><span class="sxs-lookup"><span data-stu-id="6e5da-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="6e5da-109">*Resultado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6e5da-109">*Result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e5da-110">A tabela de hash resultante.</span><span class="sxs-lookup"><span data-stu-id="6e5da-110">The resulting hash table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e5da-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e5da-111">Return value</span></span>

<span data-ttu-id="6e5da-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6e5da-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e5da-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e5da-113">Remarks</span></span>

<span data-ttu-id="6e5da-114">Essa função é muito semelhante a SHAFinal, mas é chamada diretamente da biblioteca, em vez de ser roteada pela infraestrutura de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6e5da-114">This function is very similar to SHAFinal, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="6e5da-115">Para obter mais informações, consulte [provedores do Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="6e5da-115">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5da-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e5da-116">Requirements</span></span>



| <span data-ttu-id="6e5da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e5da-117">Requirement</span></span> | <span data-ttu-id="6e5da-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6e5da-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5da-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e5da-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6e5da-120"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e5da-120"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="6e5da-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e5da-121">Library</span></span><br/> | <dl> <span data-ttu-id="6e5da-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e5da-122"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e5da-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6e5da-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="6e5da-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e5da-124"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
