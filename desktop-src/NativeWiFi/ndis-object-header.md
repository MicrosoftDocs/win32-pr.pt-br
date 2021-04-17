---
description: Empacota o tipo de objeto, a versão e as informações de tamanho necessárias em muitas estruturas do NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: Estrutura de NDIS_OBJECT_HEADER (Ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762052"
---
# <a name="ndis_object_header-structure"></a><span data-ttu-id="3b0f8-103">Estrutura de cabeçalho de \_ objeto NDIS \_</span><span class="sxs-lookup"><span data-stu-id="3b0f8-103">NDIS\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="3b0f8-104">A estrutura de **\_ \_ cabeçalho do objeto NDIS** empacota o tipo de objeto, a versão e as informações de tamanho necessárias em muitas estruturas do NDIS 6,0.</span><span class="sxs-lookup"><span data-stu-id="3b0f8-104">The **NDIS\_OBJECT\_HEADER** structure packages the object type, version, and size information that is required in many NDIS 6.0 structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0f8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b0f8-105">Syntax</span></span>


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="3b0f8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3b0f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b0f8-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3b0f8-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="3b0f8-108">Especifica o tipo de objeto NDIS que uma estrutura descreve.</span><span class="sxs-lookup"><span data-stu-id="3b0f8-108">Specifies the type of NDIS object that a structure describes.</span></span>

</dd> <dt>

<span data-ttu-id="3b0f8-109">**Revisão**</span><span class="sxs-lookup"><span data-stu-id="3b0f8-109">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="3b0f8-110">Especifica o número de revisão dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="3b0f8-110">Specifies the revision number of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="3b0f8-111">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="3b0f8-111">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3b0f8-112">Especifica o tamanho total, em bytes, da estrutura NDIS que contém o **cabeçalho do \_ objeto \_ NDIS**.</span><span class="sxs-lookup"><span data-stu-id="3b0f8-112">Specifies the total size, in bytes, of the NDIS structure that contains the **NDIS\_OBJECT\_HEADER**.</span></span> <span data-ttu-id="3b0f8-113">Esse tamanho inclui o tamanho do membro **do \_ \_ cabeçalho do objeto NDIS** e todos os outros membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="3b0f8-113">This size includes the size of the **NDIS\_OBJECT\_HEADER** member and all other members of the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b0f8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b0f8-114">Requirements</span></span>



| <span data-ttu-id="3b0f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b0f8-115">Requirement</span></span> | <span data-ttu-id="3b0f8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3b0f8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0f8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b0f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0f8-118">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="3b0f8-118">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b0f8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b0f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0f8-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b0f8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3b0f8-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3b0f8-121">Redistributable</span></span><br/>          | <span data-ttu-id="3b0f8-122">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="3b0f8-122">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="3b0f8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b0f8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b0f8-124"><dt>Ntddndis. h (incluir Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b0f8-124"><dt>Ntddndis.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b0f8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b0f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0f8-126">**Lista de DOT11 \_ BSSID \_**</span><span class="sxs-lookup"><span data-stu-id="3b0f8-126">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> </dl>

 

 




