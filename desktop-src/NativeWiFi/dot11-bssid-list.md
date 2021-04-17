---
description: Contém uma lista de identificadores básicos do conjunto de serviços (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: Estrutura de DOT11_BSSID_LIST (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813139"
---
# <a name="dot11_bssid_list-structure"></a><span data-ttu-id="cbce7-103">Estrutura da lista de DOT11 \_ BSSID \_</span><span class="sxs-lookup"><span data-stu-id="cbce7-103">DOT11\_BSSID\_LIST structure</span></span>

<span data-ttu-id="cbce7-104">A estrutura de **\_ \_ lista de DOT11 BSSID** contém uma lista de identificadores de BSS (conjunto de serviços básicos).</span><span class="sxs-lookup"><span data-stu-id="cbce7-104">The **DOT11\_BSSID\_LIST** structure contains a list of basic service set (BSS) identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbce7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbce7-105">Syntax</span></span>


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a><span data-ttu-id="cbce7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cbce7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cbce7-107">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="cbce7-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="cbce7-108">Uma estrutura de [**\_ \_ cabeçalho de objeto NDIS**](ndis-object-header.md) que contém o tipo, a versão e as informações de tamanho de uma estrutura de NDIS.</span><span class="sxs-lookup"><span data-stu-id="cbce7-108">An [**NDIS\_OBJECT\_HEADER**](ndis-object-header.md) structure that contains the type, version, and, size information of an NDIS structure.</span></span> <span data-ttu-id="cbce7-109">Para a maioria das estruturas de **\_ \_ lista de DOT11 BSSID** , defina o membro de **tipo** como padrão de  tipo de objeto de **NDIS \_ \_ \_**, defina o membro de revisão para a **lista de DOT11 \_ BSSID \_ \_ revisão \_ 1** e defina o membro de **tamanho** como **sizeof (lista de DOT11 \_ BSSID \_ )**.</span><span class="sxs-lookup"><span data-stu-id="cbce7-109">For most **DOT11\_BSSID\_LIST** structures, set the **Type** member to **NDIS\_OBJECT\_TYPE\_DEFAULT**, set the **Revision** member to **DOT11\_BSSID\_LIST\_REVISION\_1**, and set the **Size** member to **sizeof(DOT11\_BSSID\_LIST)**.</span></span>

</dd> <dt>

<span data-ttu-id="cbce7-110">**uNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="cbce7-110">**uNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="cbce7-111">O número de entradas nesta estrutura.</span><span class="sxs-lookup"><span data-stu-id="cbce7-111">The number of entries in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="cbce7-112">**uTotalNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="cbce7-112">**uTotalNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="cbce7-113">O número total de entradas com suporte.</span><span class="sxs-lookup"><span data-stu-id="cbce7-113">The total number of entries supported.</span></span>

</dd> <dt>

<span data-ttu-id="cbce7-114">**BSSIDs**</span><span class="sxs-lookup"><span data-stu-id="cbce7-114">**BSSIDs**</span></span>
</dt> <dd>

<span data-ttu-id="cbce7-115">Uma lista de identificadores de BSS.</span><span class="sxs-lookup"><span data-stu-id="cbce7-115">A list of BSS identifiers.</span></span> <span data-ttu-id="cbce7-116">Um identificador de BSS é armazenado como um tipo de [**\_ \_ endereço MAC DOT11**](dot11-mac-address-type.md) .</span><span class="sxs-lookup"><span data-stu-id="cbce7-116">A BSS identifier is stored as a [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbce7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbce7-117">Requirements</span></span>



| <span data-ttu-id="cbce7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbce7-118">Requirement</span></span> | <span data-ttu-id="cbce7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cbce7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbce7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbce7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cbce7-121">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="cbce7-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cbce7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbce7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cbce7-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbce7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cbce7-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="cbce7-124">Redistributable</span></span><br/>          | <span data-ttu-id="cbce7-125">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="cbce7-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="cbce7-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbce7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbce7-127"><dt>Windot11. h (incluir Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbce7-127"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbce7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbce7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbce7-129">**\_parâmetros de conexão WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="cbce7-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




