---
description: Evento de alteração de catálogo Winsock para uma operação de remoção de LSP (provedor de serviço em camadas).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797572"
---
# <a name="winsock_ws2help_lsp_remove-event"></a><span data-ttu-id="711b5-103">\_Evento de \_ remoção de LSP ws2help do Winsock \_</span><span class="sxs-lookup"><span data-stu-id="711b5-103">WINSOCK\_WS2HELP\_LSP\_REMOVE event</span></span>

> [!Note]  
> <span data-ttu-id="711b5-104">Os provedores de serviço em camadas são preteridos.</span><span class="sxs-lookup"><span data-stu-id="711b5-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="711b5-105">A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="711b5-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="711b5-106">O evento **Winsock \_ ws2help \_ LSP \_ Remove** é um evento de alteração de catálogo Winsock para uma operação de remoção de LSP (provedor de serviço em camadas).</span><span class="sxs-lookup"><span data-stu-id="711b5-106">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is a Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="711b5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="711b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711b5-108">*Nome do LSP*</span><span class="sxs-lookup"><span data-stu-id="711b5-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="711b5-109">O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="711b5-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> <dt>

<span data-ttu-id="711b5-110">*Catálogo*</span><span class="sxs-lookup"><span data-stu-id="711b5-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="711b5-111">O catálogo Winsock (32 bits ou 64 bits) em que o LSP está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="711b5-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="711b5-112">Este é um valor inteiro que é 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="711b5-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="711b5-113">*Instalador*</span><span class="sxs-lookup"><span data-stu-id="711b5-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="711b5-114">O nome de arquivo do módulo do aplicativo que faz a chamada de remoção de LSP.</span><span class="sxs-lookup"><span data-stu-id="711b5-114">The module filename of the application making the LSP remove call.</span></span>

</dd> <dt>

<span data-ttu-id="711b5-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="711b5-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="711b5-116">O valor de GUID do provedor de transporte do Winsock do qual o LSP está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="711b5-116">The GUID value of the Winsock transport provider that the LSP is being removed from.</span></span>

</dd> <dt>

<span data-ttu-id="711b5-117">*Categoria*</span><span class="sxs-lookup"><span data-stu-id="711b5-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="711b5-118">O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="711b5-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="711b5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="711b5-119">Remarks</span></span>

<span data-ttu-id="711b5-120">O evento **Winsock \_ ws2help \_ LSP \_ Remove** é rastreado para uma operação de remoção de LSP quando uma entrada de protocolo é removida do catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="711b5-120">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is traced for an LSP removal operation when a protocol entry is removed from the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="711b5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="711b5-121">Requirements</span></span>



| <span data-ttu-id="711b5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="711b5-122">Requirement</span></span> | <span data-ttu-id="711b5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="711b5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="711b5-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="711b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="711b5-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="711b5-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="711b5-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="711b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="711b5-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="711b5-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="711b5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="711b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711b5-129">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="711b5-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="711b5-130">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="711b5-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="711b5-131">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="711b5-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="711b5-132">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="711b5-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
