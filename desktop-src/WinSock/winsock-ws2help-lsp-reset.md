---
description: Evento de alteração de catálogo Winsock para uma operação de redefinição de catálogo Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761022"
---
# <a name="winsock_ws2help_lsp_reset-event"></a><span data-ttu-id="efcb1-103">\_Evento de \_ \_ redefinição de LSP do Winsock WS2HELP</span><span class="sxs-lookup"><span data-stu-id="efcb1-103">WINSOCK\_WS2HELP\_LSP\_RESET event</span></span>

> [!Note]  
> <span data-ttu-id="efcb1-104">Os provedores de serviço em camadas são preteridos.</span><span class="sxs-lookup"><span data-stu-id="efcb1-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="efcb1-105">A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="efcb1-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="efcb1-106">O evento **Winsock \_ ws2help \_ LSP \_ Reset** é um evento de alteração de catálogo Winsock para uma operação de redefinição de catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="efcb1-106">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is a Winsock catalog change event for a Winsock catalog reset operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="efcb1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efcb1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efcb1-108">*Catálogo*</span><span class="sxs-lookup"><span data-stu-id="efcb1-108">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="efcb1-109">O catálogo do Winsock (32 bits ou 64 bits) que está sendo redefinido.</span><span class="sxs-lookup"><span data-stu-id="efcb1-109">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="efcb1-110">Este é um valor inteiro que é 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="efcb1-110">This is an integer value that is either 32 or 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efcb1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="efcb1-111">Remarks</span></span>

<span data-ttu-id="efcb1-112">O evento **Winsock \_ ws2help \_ LSP \_ Reset** é rastreado para uma operação de LSP (provedor de serviço em camadas) do Winsock quando o catálogo do Winsock é redefinido.</span><span class="sxs-lookup"><span data-stu-id="efcb1-112">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is traced for an Winsock Layered Service Provider (LSP) operation when the Winsock catalog is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="efcb1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efcb1-113">Requirements</span></span>



| <span data-ttu-id="efcb1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="efcb1-114">Requirement</span></span> | <span data-ttu-id="efcb1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="efcb1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="efcb1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efcb1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="efcb1-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efcb1-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="efcb1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efcb1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="efcb1-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efcb1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efcb1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="efcb1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efcb1-121">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="efcb1-121">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="efcb1-122">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="efcb1-122">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="efcb1-123">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="efcb1-123">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="efcb1-124">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="efcb1-124">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
