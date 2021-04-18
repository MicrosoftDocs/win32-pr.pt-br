---
description: As \_ constantes de sinalizador de bit LINEGENERATETERM descrevem as condições sob as quais a geração de dígito ou Tom é encerrada.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Constantes de LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800021"
---
# <a name="linegenerateterm_-constants"></a><span data-ttu-id="6b109-103">\_Constantes LINEGENERATETERM</span><span class="sxs-lookup"><span data-stu-id="6b109-103">LINEGENERATETERM\_ Constants</span></span>

<span data-ttu-id="6b109-104">As constantes de sinalizador de bit **LINEGENERATETERM \_** descrevem as condições sob as quais a geração de dígito ou Tom é encerrada.</span><span class="sxs-lookup"><span data-stu-id="6b109-104">The **LINEGENERATETERM\_** bit-flag constants describe the conditions under which digit or tone generation is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="6b109-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM \_ cancelar**</span><span class="sxs-lookup"><span data-stu-id="6b109-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6b109-106">A solicitação de geração de dígitos ou tons foi cancelada por este aplicativo, por outro aplicativo ou porque a chamada foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="6b109-106">The digit or tone generation request was canceled by this application, by another application, or because the call terminated.</span></span> <span data-ttu-id="6b109-107">Esse valor também pode ser retornado quando a geração de dígitos ou tons não pode ser concluída devido a uma falha interna do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="6b109-107">This value can also be returned when digit or tone generation cannot be completed due to internal failure of the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b109-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="6b109-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM\_DONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6b109-109">O número solicitado de dígitos ou os tons solicitados foram gerados para a duração solicitada.</span><span class="sxs-lookup"><span data-stu-id="6b109-109">The requested number of digits or requested tones have been generated for the requested duration.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b109-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b109-110">Remarks</span></span>

<span data-ttu-id="6b109-111">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="6b109-111">No extensibility.</span></span> <span data-ttu-id="6b109-112">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="6b109-112">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b109-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b109-113">Requirements</span></span>



| <span data-ttu-id="6b109-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b109-114">Requirement</span></span> | <span data-ttu-id="6b109-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6b109-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6b109-116">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="6b109-116">TAPI version</span></span><br/> | <span data-ttu-id="6b109-117">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6b109-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6b109-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b109-118">Header</span></span><br/>       | <dl> <span data-ttu-id="6b109-119"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b109-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




