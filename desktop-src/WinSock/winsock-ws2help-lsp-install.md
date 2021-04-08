---
description: Evento de alteração de catálogo Winsock para uma operação de instalação do LSP (provedor de serviço em camadas).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: WINSOCK_WS2HELP_LSP_INSTALL evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922285"
---
# <a name="winsock_ws2help_lsp_install-event"></a><span data-ttu-id="69066-103">\_Evento de \_ instalação de LSP do Winsock WS2HELP \_</span><span class="sxs-lookup"><span data-stu-id="69066-103">WINSOCK\_WS2HELP\_LSP\_INSTALL event</span></span>

> [!Note]  
> <span data-ttu-id="69066-104">Os provedores de serviço em camadas são preteridos.</span><span class="sxs-lookup"><span data-stu-id="69066-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="69066-105">A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="69066-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="69066-106">O evento de **instalação do Winsock \_ ws2help \_ LSP \_** é um evento de alteração de catálogo do Winsock para uma operação de instalação do LSP (provedor de serviço em camadas).</span><span class="sxs-lookup"><span data-stu-id="69066-106">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is a Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="69066-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69066-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69066-108">*Nome do LSP*</span><span class="sxs-lookup"><span data-stu-id="69066-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="69066-109">O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="69066-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> <dt>

<span data-ttu-id="69066-110">*Catálogo*</span><span class="sxs-lookup"><span data-stu-id="69066-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="69066-111">O catálogo do Winsock (32 bits ou 64 bits) em que o LSP está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="69066-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="69066-112">Este é um valor inteiro que é 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="69066-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="69066-113">*Instalador*</span><span class="sxs-lookup"><span data-stu-id="69066-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="69066-114">O nome de arquivo do módulo do aplicativo que faz a chamada de instalação de LSP.</span><span class="sxs-lookup"><span data-stu-id="69066-114">The module filename of the application making the LSP install call.</span></span>

</dd> <dt>

<span data-ttu-id="69066-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="69066-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="69066-116">O valor de GUID do provedor de transporte do Winsock no qual o LSP está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="69066-116">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span>

</dd> <dt>

<span data-ttu-id="69066-117">*Categoria*</span><span class="sxs-lookup"><span data-stu-id="69066-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="69066-118">O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="69066-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69066-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="69066-119">Remarks</span></span>

<span data-ttu-id="69066-120">O evento de **instalação do Winsock \_ ws2help \_ LSP \_** é rastreado para uma operação de instalação de LSP quando uma entrada de protocolo é instalada no catálogo do Winsock.</span><span class="sxs-lookup"><span data-stu-id="69066-120">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is traced for an LSP install operation when a protocol entry is installed into the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="69066-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69066-121">Requirements</span></span>



| <span data-ttu-id="69066-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="69066-122">Requirement</span></span> | <span data-ttu-id="69066-123">Valor</span><span class="sxs-lookup"><span data-stu-id="69066-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69066-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69066-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69066-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69066-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="69066-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69066-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69066-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69066-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69066-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="69066-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69066-129">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="69066-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="69066-130">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="69066-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="69066-131">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="69066-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="69066-132">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="69066-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
