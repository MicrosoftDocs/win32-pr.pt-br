---
description: Armazena as principais informações sobre uma interface de LAN sem fio gerenciada pelo serviço de configuração sem fio.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: Estrutura de INTF_KEY_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296428"
---
# <a name="intf_key_entry-structure"></a><span data-ttu-id="8af95-103">Estrutura de entrada de \_ chave INTF \_</span><span class="sxs-lookup"><span data-stu-id="8af95-103">INTF\_KEY\_ENTRY structure</span></span>

<span data-ttu-id="8af95-104">\[**INTF \_ A \_ entrada de chave** não tem mais suporte do Windows Vista e do windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8af95-104">\[**INTF\_KEY\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8af95-105">Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante.</span><span class="sxs-lookup"><span data-stu-id="8af95-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="8af95-106">Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="8af95-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="8af95-107">A estrutura de **\_ \_ entrada de chave INTF** armazena as principais informações sobre uma interface de LAN sem fio gerenciada pelo serviço de configuração sem fio.</span><span class="sxs-lookup"><span data-stu-id="8af95-107">The **INTF\_KEY\_ENTRY** structure stores the key information about a wireless LAN interface managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af95-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8af95-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a><span data-ttu-id="8af95-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8af95-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8af95-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="8af95-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="8af95-111">Um ponteiro para o GUID da interface representado como uma cadeia de caracteres Unicode no seguinte formato: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span><span class="sxs-lookup"><span data-stu-id="8af95-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8af95-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8af95-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8af95-113">O arquivo de cabeçalho *wzcsapi. h* não está disponível no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="8af95-113">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8af95-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8af95-114">Requirements</span></span>



| <span data-ttu-id="8af95-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8af95-115">Requirement</span></span> | <span data-ttu-id="8af95-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8af95-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8af95-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8af95-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8af95-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="8af95-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8af95-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8af95-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8af95-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8af95-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8af95-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8af95-121">End of client support</span></span><br/>    | <span data-ttu-id="8af95-122">Windows XP com SP3</span><span class="sxs-lookup"><span data-stu-id="8af95-122">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="8af95-123">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="8af95-123">End of server support</span></span><br/>    | <span data-ttu-id="8af95-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8af95-124">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="8af95-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8af95-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8af95-126"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8af95-126"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af95-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8af95-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af95-128">**\_tabela de chave INTFS \_**</span><span class="sxs-lookup"><span data-stu-id="8af95-128">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="8af95-129">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="8af95-129">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> </dl>

 

 




