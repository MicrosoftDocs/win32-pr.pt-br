---
description: Contém parâmetros de configuração EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: Estrutura de EAPOL_INTF_PARAMS (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780941"
---
# <a name="eapol_intf_params-structure"></a><span data-ttu-id="dfbfe-103">Estrutura de parâmetros de EAPOL \_ INTF \_</span><span class="sxs-lookup"><span data-stu-id="dfbfe-103">EAPOL\_INTF\_PARAMS structure</span></span>

<span data-ttu-id="dfbfe-104">\[**EAPOL \_ Não há mais suporte para \_ params INTF** a partir do Windows Vista e do windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-104">\[**EAPOL\_INTF\_PARAMS** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="dfbfe-105">Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="dfbfe-106">Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="dfbfe-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="dfbfe-107">Contém parâmetros de configuração EAPOL.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-107">Contains EAPOL configuration parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbfe-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfbfe-108">Syntax</span></span>


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a><span data-ttu-id="dfbfe-109">Membros</span><span class="sxs-lookup"><span data-stu-id="dfbfe-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="dfbfe-110">**DW**</span><span class="sxs-lookup"><span data-stu-id="dfbfe-110">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="dfbfe-111">Versão do chamador.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-111">Version of the caller.</span></span> <span data-ttu-id="dfbfe-112">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-112">Default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="dfbfe-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="dfbfe-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="dfbfe-114">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="dfbfe-115">**dwEapFlags**</span><span class="sxs-lookup"><span data-stu-id="dfbfe-115">**dwEapFlags**</span></span>
</dt> <dd>

<span data-ttu-id="dfbfe-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dfbfe-117">**dwEapType**</span><span class="sxs-lookup"><span data-stu-id="dfbfe-117">**dwEapType**</span></span>
</dt> <dd>

<span data-ttu-id="dfbfe-118">O tipo de extensão EAP a ser usado.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-118">The EAP extension type to be used.</span></span> <span data-ttu-id="dfbfe-119">Defina como 0x00000013 para EAP-TLS e 0x00000026 para PEAP.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-119">Set to 0x00000013 for EAP-TLS and 0x00000026 for PEAP.</span></span>

</dd> <dt>

<span data-ttu-id="dfbfe-120">**dwSizeOfSSID**</span><span class="sxs-lookup"><span data-stu-id="dfbfe-120">**dwSizeOfSSID**</span></span>
</dt> <dd>

<span data-ttu-id="dfbfe-121">Tamanho do identificador de rede.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-121">Size of network identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dfbfe-122">**bSSID**</span><span class="sxs-lookup"><span data-stu-id="dfbfe-122">**bSSID**</span></span>
</dt> <dd>

<span data-ttu-id="dfbfe-123">Identificador de rede.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-123">Network identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfbfe-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfbfe-124">Remarks</span></span>

<span data-ttu-id="dfbfe-125">O arquivo de cabeçalho wzcsapi. h não está disponível no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-125">The header file wzcsapi.h is not available in the Windows SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfbfe-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfbfe-126">Requirements</span></span>



| <span data-ttu-id="dfbfe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfbfe-127">Requirement</span></span> | <span data-ttu-id="dfbfe-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dfbfe-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbfe-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfbfe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dfbfe-130">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="dfbfe-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dfbfe-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfbfe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dfbfe-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dfbfe-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dfbfe-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dfbfe-133">End of client support</span></span><br/>    | <span data-ttu-id="dfbfe-134">Windows XP com SP3</span><span class="sxs-lookup"><span data-stu-id="dfbfe-134">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="dfbfe-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="dfbfe-135">End of server support</span></span><br/>    | <span data-ttu-id="dfbfe-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dfbfe-136">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="dfbfe-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfbfe-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfbfe-138"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfbfe-138"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




