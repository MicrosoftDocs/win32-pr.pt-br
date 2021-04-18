---
description: As \_ constantes de sinalizador de bit LINECALLPRIVILEGE descrevem os tipos de direitos de acesso ou privilégios que um aplicativo com um identificador de chamada pode ter para a chamada correspondente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Constantes de LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759048"
---
# <a name="linecallprivilege_-constants"></a><span data-ttu-id="cd9ad-103">\_Constantes LINECALLPRIVILEGE</span><span class="sxs-lookup"><span data-stu-id="cd9ad-103">LINECALLPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="cd9ad-104">As constantes de sinalizador de bit **LINECALLPRIVILEGE \_** descrevem os tipos de direitos de acesso ou privilégios que um aplicativo com um identificador de chamada pode ter para a chamada correspondente.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-104">The **LINECALLPRIVILEGE\_** bit-flag constants describe the kinds of access rights or privileges an application with a call handle may have to the corresponding call.</span></span>

<dl> <dt>

<span data-ttu-id="cd9ad-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**MONITOR de LINECALLPRIVILEGE \_**</span><span class="sxs-lookup"><span data-stu-id="cd9ad-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cd9ad-106">O aplicativo tem privilégios de monitor para a chamada.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-106">The application has monitor privileges to the call.</span></span> <span data-ttu-id="cd9ad-107">Esses privilégios permitem que o aplicativo monitore as alterações de estado e as informações de consulta e o status sobre a chamada.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-107">These privileges allow the application to monitor state changes and query information and status about the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd9ad-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="cd9ad-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cd9ad-109">O aplicativo não tem privilégios para a chamada.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-109">The application has no privileges to the call.</span></span> <span data-ttu-id="cd9ad-110">O identificador do aplicativo é void e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-110">The application's handle is void and should not be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd9ad-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**proprietário do LINECALLPRIVILEGE \_**</span><span class="sxs-lookup"><span data-stu-id="cd9ad-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cd9ad-112">O aplicativo tem privilégios de proprietário para a chamada.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-112">The application has owner privileges to the call.</span></span> <span data-ttu-id="cd9ad-113">Esses privilégios permitem que o aplicativo manipule a chamada de maneira que afete o estado da chamada.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-113">These privileges allow the application to manipulate the call in ways that affect the state of the call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd9ad-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd9ad-114">Remarks</span></span>

<span data-ttu-id="cd9ad-115">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-115">No extensibility.</span></span> <span data-ttu-id="cd9ad-116">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="cd9ad-117">Quando um identificador de chamada é fornecido pela primeira vez a um aplicativo ou sempre que os privilégios de chamada desse aplicativo são modificados, a mensagem [**\_ callstate de linha**](line-callstate.md) é enviada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-117">When a call handle is first provided to an application or whenever call privileges of that application are modified, the [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="cd9ad-118">Quando um aplicativo passa por uma chamada e, se o aplicativo de recebimento ainda não tiver um identificador com privilégios de proprietário, essa mensagem informará ao aplicativo sobre seus novos privilégios para a chamada.</span><span class="sxs-lookup"><span data-stu-id="cd9ad-118">When an application hands off a call, and if the receiving application does not already have a handle with owner privileges, then this message informs the application about its new privileges to the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9ad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd9ad-119">Requirements</span></span>



| <span data-ttu-id="cd9ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd9ad-120">Requirement</span></span> | <span data-ttu-id="cd9ad-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cd9ad-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cd9ad-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cd9ad-122">TAPI version</span></span><br/> | <span data-ttu-id="cd9ad-123">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cd9ad-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cd9ad-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd9ad-124">Header</span></span><br/>       | <dl> <span data-ttu-id="cd9ad-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ad-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




