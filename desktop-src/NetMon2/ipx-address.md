---
description: A \_ estrutura de Endereço IPX fornece um endereço no nível do protocolo IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Estrutura de IPX_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501594"
---
# <a name="ipx_address-structure"></a><span data-ttu-id="5225c-103">\_Estrutura de Endereço IPX</span><span class="sxs-lookup"><span data-stu-id="5225c-103">IPX\_ADDRESS structure</span></span>

<span data-ttu-id="5225c-104">A estrutura de **\_ Endereço IPX** fornece um endereço no nível do protocolo IPX.</span><span class="sxs-lookup"><span data-stu-id="5225c-104">The **IPX\_ADDRESS** structure provides an address at the IPX protocol level.</span></span>

## <a name="syntax"></a><span data-ttu-id="5225c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5225c-105">Syntax</span></span>


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="5225c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5225c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5225c-107">**Sub-rede**</span><span class="sxs-lookup"><span data-stu-id="5225c-107">**Subnet**</span></span>
</dt> <dd>

<span data-ttu-id="5225c-108">Identificador de sub-rede de rede.</span><span class="sxs-lookup"><span data-stu-id="5225c-108">Network subnet identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5225c-109">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="5225c-109">**Address**</span></span>
</dt> <dd>

<span data-ttu-id="5225c-110">Identificador da NIC da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5225c-110">Subnet NIC identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5225c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5225c-111">Requirements</span></span>



| <span data-ttu-id="5225c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5225c-112">Requirement</span></span> | <span data-ttu-id="5225c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5225c-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5225c-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5225c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5225c-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5225c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5225c-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5225c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5225c-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5225c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5225c-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5225c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5225c-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5225c-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




