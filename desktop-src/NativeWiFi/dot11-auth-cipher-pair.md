---
description: Define um par de algoritmos de autenticação e codificação 802,11 que podem ser habilitados ao mesmo tempo na estação 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: Estrutura de DOT11_AUTH_CIPHER_PAIR (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758183"
---
# <a name="dot11_auth_cipher_pair-structure"></a><span data-ttu-id="f8a61-103">\_Estrutura de \_ par de codificação de DOT11 auth \_</span><span class="sxs-lookup"><span data-stu-id="f8a61-103">DOT11\_AUTH\_CIPHER\_PAIR structure</span></span>

<span data-ttu-id="f8a61-104">A estrutura de **\_ par de \_ codificação \_ de DOT11 auth** define um par de algoritmos de autenticação e codificação 802,11 que pode ser habilitado ao mesmo tempo na estação 802,11.</span><span class="sxs-lookup"><span data-stu-id="f8a61-104">The **DOT11\_AUTH\_CIPHER\_PAIR** structure defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a61-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8a61-105">Syntax</span></span>


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a><span data-ttu-id="f8a61-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f8a61-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8a61-107">**AuthAlgoId**</span><span class="sxs-lookup"><span data-stu-id="f8a61-107">**AuthAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="f8a61-108">Um algoritmo de autenticação que usa um tipo enumerado de [**\_ \_ algoritmo DOT11 auth**](dot11-auth-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="f8a61-108">An authentication algorithm that uses a [**DOT11\_AUTH\_ALGORITHM**](dot11-auth-algorithm.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="f8a61-109">**CipherAlgoId**</span><span class="sxs-lookup"><span data-stu-id="f8a61-109">**CipherAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="f8a61-110">Um algoritmo de codificação que usa um tipo enumerado de [**\_ \_ algoritmo DOT11 Cipher**](dot11-cipher-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="f8a61-110">A cipher algorithm that uses a [**DOT11\_CIPHER\_ALGORITHM**](dot11-cipher-algorithm.md) enumerated type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8a61-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8a61-111">Remarks</span></span>

<span data-ttu-id="f8a61-112">A estrutura de par de codificação de DOT11 \_ auth \_ \_ define um algoritmo de autenticação e codificação que pode ser habilitado junto para conexões de rede de BSS (conjunto de serviços básico).</span><span class="sxs-lookup"><span data-stu-id="f8a61-112">The DOT11\_AUTH\_CIPHER\_PAIR structure defines an authentication and cipher algorithm that can be enabled together for basic service set (BSS) network connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a61-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8a61-113">Requirements</span></span>



| <span data-ttu-id="f8a61-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a61-114">Requirement</span></span> | <span data-ttu-id="f8a61-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f8a61-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a61-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8a61-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a61-117">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f8a61-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f8a61-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8a61-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a61-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8a61-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="f8a61-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f8a61-120">Redistributable</span></span><br/>          | <span data-ttu-id="f8a61-121">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="f8a61-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="f8a61-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8a61-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a61-123"><dt>Wlantypes. h (incluir Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8a61-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8a61-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8a61-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a61-125">**\_Algoritmo de autenticação DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="f8a61-125">**DOT11\_AUTH\_ALGORITHM**</span></span>](dot11-auth-algorithm.md)
</dt> <dt>

[<span data-ttu-id="f8a61-126">**\_Algoritmo de codificação DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="f8a61-126">**DOT11\_CIPHER\_ALGORITHM**</span></span>](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




