---
description: Contém a tabela de informações de chave para todas as interfaces de LAN sem fio gerenciadas pelo serviço de configuração sem fio.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: Estrutura de INTFS_KEY_TABLE (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811827"
---
# <a name="intfs_key_table-structure"></a><span data-ttu-id="582b4-103">Estrutura de tabela de \_ chave INTFS \_</span><span class="sxs-lookup"><span data-stu-id="582b4-103">INTFS\_KEY\_TABLE structure</span></span>

<span data-ttu-id="582b4-104">\[**INTFS \_ A \_ tabela de chave** não tem mais suporte a partir do Windows Vista e do windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="582b4-104">\[**INTFS\_KEY\_TABLE** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="582b4-105">Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante.</span><span class="sxs-lookup"><span data-stu-id="582b4-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="582b4-106">Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="582b4-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="582b4-107">A estrutura da **\_ \_ tabela de chave INTFS** contém a tabela de informações de chave para todas as interfaces de LAN sem fio gerenciadas pelo serviço de configuração sem fio.</span><span class="sxs-lookup"><span data-stu-id="582b4-107">The **INTFS\_KEY\_TABLE** structure contains the table of key information for all wireless LAN interfaces managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="582b4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="582b4-108">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a><span data-ttu-id="582b4-109">Membros</span><span class="sxs-lookup"><span data-stu-id="582b4-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="582b4-110">**dwNumIntfs**</span><span class="sxs-lookup"><span data-stu-id="582b4-110">**dwNumIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="582b4-111">Número total de interfaces.</span><span class="sxs-lookup"><span data-stu-id="582b4-111">Total number of interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="582b4-112">**pIntfs**</span><span class="sxs-lookup"><span data-stu-id="582b4-112">**pIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="582b4-113">Ponteiro para a estrutura de [**\_ \_ entrada de chave INTF**](intf-key-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="582b4-113">Pointer to the [**INTF\_KEY\_ENTRY**](intf-key-entry.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="582b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="582b4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="582b4-115">O arquivo de cabeçalho *wzcsapi. h* não está disponível no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="582b4-115">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="582b4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="582b4-116">Requirements</span></span>



| <span data-ttu-id="582b4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="582b4-117">Requirement</span></span> | <span data-ttu-id="582b4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="582b4-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="582b4-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="582b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="582b4-120">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="582b4-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="582b4-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="582b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="582b4-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="582b4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="582b4-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="582b4-123">End of client support</span></span><br/>    | <span data-ttu-id="582b4-124">Windows XP com SP3</span><span class="sxs-lookup"><span data-stu-id="582b4-124">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="582b4-125">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="582b4-125">End of server support</span></span><br/>    | <span data-ttu-id="582b4-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="582b4-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="582b4-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="582b4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="582b4-128"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="582b4-128"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




