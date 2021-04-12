---
description: A estrutura de \_ endereços IP de Vines \_ é um endereço IP em uma rede de Vines.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Estrutura de VINES_IP_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296908"
---
# <a name="vines_ip_address-structure"></a><span data-ttu-id="4d0f0-103">Estrutura de \_ endereços IP de Vines \_</span><span class="sxs-lookup"><span data-stu-id="4d0f0-103">VINES\_IP\_ADDRESS structure</span></span>

<span data-ttu-id="4d0f0-104">A estrutura de **\_ \_ endereços IP de Vines** é um endereço IP em uma rede de Vines.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-104">The **VINES\_IP\_ADDRESS** structure is an IP address on a Vines network.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d0f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d0f0-105">Syntax</span></span>


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="4d0f0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4d0f0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d0f0-107">**Com e/o**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-107">**NetID**</span></span>
</dt> <dd>

<span data-ttu-id="4d0f0-108">O identificador de um computador específico em uma sub-rede específica.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-108">The identifier of a specific machine on a specific subnet.</span></span>

</dd> <dt>

<span data-ttu-id="4d0f0-109">**SubnetID**</span><span class="sxs-lookup"><span data-stu-id="4d0f0-109">**SubnetID**</span></span>
</dt> <dd>

<span data-ttu-id="4d0f0-110">O identificador de uma sub-rede específica em toda a rede.</span><span class="sxs-lookup"><span data-stu-id="4d0f0-110">The identifier of a specific subnet on the whole network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d0f0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d0f0-111">Requirements</span></span>



| <span data-ttu-id="4d0f0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d0f0-112">Requirement</span></span> | <span data-ttu-id="4d0f0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4d0f0-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d0f0-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d0f0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4d0f0-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d0f0-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4d0f0-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d0f0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4d0f0-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d0f0-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4d0f0-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4d0f0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d0f0-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d0f0-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




