---
description: Evento de alteração de catálogo Winsock para uma operação de desabilitação de LSP (provedor de serviço em camadas).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748863"
---
# <a name="winsock_ws2help_lsp_disable-event"></a><span data-ttu-id="937ed-103">\_Evento de \_ desabilitação de LSP ws2help do Winsock \_</span><span class="sxs-lookup"><span data-stu-id="937ed-103">WINSOCK\_WS2HELP\_LSP\_DISABLE event</span></span>

> [!Note]  
> <span data-ttu-id="937ed-104">Os provedores de serviço em camadas são preteridos.</span><span class="sxs-lookup"><span data-stu-id="937ed-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="937ed-105">A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="937ed-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="937ed-106">O evento **Winsock \_ ws2help \_ LSP \_ Disable** é um evento de alteração de catálogo Winsock para uma operação de desabilitação de LSP (provedor de serviço em camadas).</span><span class="sxs-lookup"><span data-stu-id="937ed-106">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is a Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="937ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="937ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="937ed-108">*Nome do LSP*</span><span class="sxs-lookup"><span data-stu-id="937ed-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="937ed-109">O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="937ed-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="937ed-110">*Catálogo*</span><span class="sxs-lookup"><span data-stu-id="937ed-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="937ed-111">O catálogo Winsock (32 bits ou 64 bits) em que o LSP está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="937ed-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="937ed-112">Este é um valor inteiro que é 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="937ed-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="937ed-113">*Instalador*</span><span class="sxs-lookup"><span data-stu-id="937ed-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="937ed-114">O nome de arquivo do módulo do aplicativo que faz a chamada de desabilitação de LSP.</span><span class="sxs-lookup"><span data-stu-id="937ed-114">The module filename of the application making the LSP disable call.</span></span>

</dd> <dt>

<span data-ttu-id="937ed-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="937ed-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="937ed-116">O valor de GUID do provedor de transporte do Winsock que o LSP está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="937ed-116">The GUID value of the Winsock transport provider that the LSP is being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="937ed-117">*Categoria*</span><span class="sxs-lookup"><span data-stu-id="937ed-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="937ed-118">O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="937ed-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> </dl>

<span data-ttu-id="937ed-119">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="937ed-119">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="937ed-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="937ed-120">Remarks</span></span>

<span data-ttu-id="937ed-121">O evento **Winsock \_ ws2help \_ LSP \_ Disable** é rastreado para uma operação de desabilitação de LSP quando uma entrada de protocolo está desabilitada no catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="937ed-121">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is traced for an LSP disable operation when a protocol entry is disabled in the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="937ed-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="937ed-122">Requirements</span></span>



| <span data-ttu-id="937ed-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="937ed-123">Requirement</span></span> | <span data-ttu-id="937ed-124">Valor</span><span class="sxs-lookup"><span data-stu-id="937ed-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="937ed-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="937ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="937ed-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="937ed-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="937ed-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="937ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="937ed-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="937ed-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="937ed-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="937ed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="937ed-130">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="937ed-130">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="937ed-131">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="937ed-131">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="937ed-132">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="937ed-132">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="937ed-133">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="937ed-133">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
