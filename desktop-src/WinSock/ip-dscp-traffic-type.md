---
description: A tabela a seguir descreve \_ \_ as opções de soquete do tipo de tráfego IP DSCP \_ .
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748730"
---
# <a name="ip_dscp_traffic_type"></a><span data-ttu-id="edde5-103">\_tipo de \_ tráfego IP DSCP \_</span><span class="sxs-lookup"><span data-stu-id="edde5-103">IP\_DSCP\_TRAFFIC\_TYPE</span></span>

<span data-ttu-id="edde5-104">A tabela a seguir descreve \_ \_ as opções de soquete do tipo de tráfego IP DSCP \_ .</span><span class="sxs-lookup"><span data-stu-id="edde5-104">The following table describes IP\_DSCP\_TRAFFIC\_TYPE Socket Options.</span></span>

<dl> <span data-ttu-id="edde5-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_tipo de \_ tráfego IP DSCP \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="edde5-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP\_DSCP\_TRAFFIC\_TYPE**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="edde5-106">Opção</span><span class="sxs-lookup"><span data-stu-id="edde5-106">Option</span></span>              | <span data-ttu-id="edde5-107">Obter</span><span class="sxs-lookup"><span data-stu-id="edde5-107">Get</span></span> | <span data-ttu-id="edde5-108">Definir</span><span class="sxs-lookup"><span data-stu-id="edde5-108">Set</span></span> | <span data-ttu-id="edde5-109">Tipo de optval</span><span class="sxs-lookup"><span data-stu-id="edde5-109">Optval Type</span></span> | <span data-ttu-id="edde5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="edde5-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edde5-111">\_tipo de tráfego DSCP \_</span><span class="sxs-lookup"><span data-stu-id="edde5-111">DSCP\_TRAFFIC\_TYPE</span></span> | <span data-ttu-id="edde5-112">Sim</span><span class="sxs-lookup"><span data-stu-id="edde5-112">Yes</span></span> | <span data-ttu-id="edde5-113">Sim</span><span class="sxs-lookup"><span data-stu-id="edde5-113">Yes</span></span> | <span data-ttu-id="edde5-114">DWORD</span><span class="sxs-lookup"><span data-stu-id="edde5-114">DWORD</span></span>       | <span data-ttu-id="edde5-115">Ao definir esse valor como valores definidos no **\_ \_ tipo de tráfego DSCP**, um aplicativo poderá solicitar que seus pacotes de rede sejam tratados de acordo com o tipo de serviço que está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="edde5-115">By setting this value to values defined in **DSCP\_TRAFFIC\_TYPE**, an application will be able to ask its network packets to be treated according to the type of service being requested.</span></span> <span data-ttu-id="edde5-116">Chamadas semelhantes a [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) podem ser usadas para obter a configuração atual para o tipo de tráfego solicitado no soquete especificado</span><span class="sxs-lookup"><span data-stu-id="edde5-116">Similarly calls to [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) can be used to obtain the current setting for the type of traffic requested on the given socket</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="edde5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edde5-117">Requirements</span></span>



| <span data-ttu-id="edde5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="edde5-118">Requirement</span></span> | <span data-ttu-id="edde5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="edde5-119">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="edde5-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="edde5-120">End of client support</span></span><br/> | <span data-ttu-id="edde5-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="edde5-121">Windows 10</span></span><br/>                                                          |
| <span data-ttu-id="edde5-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="edde5-122">End of server support</span></span><br/> | <span data-ttu-id="edde5-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="edde5-123">Windows Server 2016</span></span><br/>                                                 |
| <span data-ttu-id="edde5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="edde5-124">Header</span></span><br/>                | <dl> <span data-ttu-id="edde5-125"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="edde5-125"><dt>N/A</dt></span></span> </dl> |



 

 




