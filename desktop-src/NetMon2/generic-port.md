---
description: Contém um número de porta usado para protocolos IP ou IPX.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: União de GENERIC_PORT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920704"
---
# <a name="generic_port-union"></a><span data-ttu-id="45568-103">\_União de porta genérica</span><span class="sxs-lookup"><span data-stu-id="45568-103">GENERIC\_PORT union</span></span>

<span data-ttu-id="45568-104">A estrutura de **\_ porta genérica** contém um número de porta usado para protocolos IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="45568-104">The **GENERIC\_PORT** structure contains a port number used for IP or IPX protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="45568-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45568-105">Syntax</span></span>


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a><span data-ttu-id="45568-106">Membros</span><span class="sxs-lookup"><span data-stu-id="45568-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="45568-107">**IPPort**</span><span class="sxs-lookup"><span data-stu-id="45568-107">**IPPort**</span></span>
</dt> <dd>

<span data-ttu-id="45568-108">Número da porta IP preenchido.</span><span class="sxs-lookup"><span data-stu-id="45568-108">IP port number filled in.</span></span>

</dd> <dt>

<span data-ttu-id="45568-109">**ByteSwappedIPXPort**</span><span class="sxs-lookup"><span data-stu-id="45568-109">**ByteSwappedIPXPort**</span></span>
</dt> <dd>

<span data-ttu-id="45568-110">Número da porta IPX preenchida.</span><span class="sxs-lookup"><span data-stu-id="45568-110">IPX port number filled in.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45568-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45568-111">Requirements</span></span>



| <span data-ttu-id="45568-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="45568-112">Requirement</span></span> | <span data-ttu-id="45568-113">Valor</span><span class="sxs-lookup"><span data-stu-id="45568-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="45568-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45568-114">Minimum supported client</span></span><br/> | <span data-ttu-id="45568-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45568-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="45568-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45568-116">Minimum supported server</span></span><br/> | <span data-ttu-id="45568-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45568-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="45568-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45568-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="45568-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="45568-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




