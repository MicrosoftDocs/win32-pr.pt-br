---
description: A estrutura MACFRAME é uma União dos protocolos iniciais mais comuns.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: MACFRAME Union (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769304"
---
# <a name="macframe-union"></a><span data-ttu-id="b390f-103">MACFRAME Union</span><span class="sxs-lookup"><span data-stu-id="b390f-103">MACFRAME union</span></span>

<span data-ttu-id="b390f-104">A estrutura **MACFRAME** é uma União dos protocolos iniciais mais comuns.</span><span class="sxs-lookup"><span data-stu-id="b390f-104">The **MACFRAME** structure is a union of the most common initial protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="b390f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b390f-105">Syntax</span></span>


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a><span data-ttu-id="b390f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b390f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b390f-107">**MacHeader**</span><span class="sxs-lookup"><span data-stu-id="b390f-107">**MacHeader**</span></span>
</dt> <dd>

<span data-ttu-id="b390f-108">Ponteiro genérico para um quadro.</span><span class="sxs-lookup"><span data-stu-id="b390f-108">Generic pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="b390f-109">**Ethernet**</span><span class="sxs-lookup"><span data-stu-id="b390f-109">**Ethernet**</span></span>
</dt> <dd>

<span data-ttu-id="b390f-110">Ponteiro Ethernet para um quadro.</span><span class="sxs-lookup"><span data-stu-id="b390f-110">Ethernet pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="b390f-111">**Tokenring**</span><span class="sxs-lookup"><span data-stu-id="b390f-111">**Tokenring**</span></span>
</dt> <dd>

<span data-ttu-id="b390f-112">Ponteiro de token ring para um quadro.</span><span class="sxs-lookup"><span data-stu-id="b390f-112">Token ring pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="b390f-113">**FDDI**</span><span class="sxs-lookup"><span data-stu-id="b390f-113">**Fddi**</span></span>
</dt> <dd>

<span data-ttu-id="b390f-114">Ponteiro FDDI para um quadro.</span><span class="sxs-lookup"><span data-stu-id="b390f-114">FDDI pointer to a frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b390f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b390f-115">Remarks</span></span>

<span data-ttu-id="b390f-116">Essa estrutura é usada com mais frequência como uma sobreposição.</span><span class="sxs-lookup"><span data-stu-id="b390f-116">This structure is most frequently used as an overlay.</span></span> <span data-ttu-id="b390f-117">Para tornar as propriedades do primeiro protocolo acessíveis, converta o quadro como o mesmo tipo do protocolo.</span><span class="sxs-lookup"><span data-stu-id="b390f-117">To make the properties of the first protocol accessible, cast the frame as the same type as the protocol.</span></span>

## <a name="requirements"></a><span data-ttu-id="b390f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b390f-118">Requirements</span></span>



| <span data-ttu-id="b390f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b390f-119">Requirement</span></span> | <span data-ttu-id="b390f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b390f-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b390f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b390f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b390f-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b390f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b390f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b390f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b390f-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b390f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b390f-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b390f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b390f-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b390f-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




