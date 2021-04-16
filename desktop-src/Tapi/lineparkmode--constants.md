---
description: As \_ constantes de sinalizador de bit LINEPARKMODE descrevem diferentes maneiras de chamadas de estacionamento.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Constantes de LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757959"
---
# <a name="lineparkmode_-constants"></a><span data-ttu-id="e51a6-103">\_Constantes LINEPARKMODE</span><span class="sxs-lookup"><span data-stu-id="e51a6-103">LINEPARKMODE\_ Constants</span></span>

<span data-ttu-id="e51a6-104">As constantes de sinalizador de bit **LINEPARKMODE \_** descrevem diferentes maneiras de chamadas de estacionamento.</span><span class="sxs-lookup"><span data-stu-id="e51a6-104">The **LINEPARKMODE\_** bit-flag constants describe different ways of parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="e51a6-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ direcionado**</span><span class="sxs-lookup"><span data-stu-id="e51a6-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE\_DIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e51a6-106">Especifica o parque de chamada direcionada.</span><span class="sxs-lookup"><span data-stu-id="e51a6-106">Specifies directed call park.</span></span> <span data-ttu-id="e51a6-107">O endereço em que a chamada será estacionada deve ser fornecido para a opção.</span><span class="sxs-lookup"><span data-stu-id="e51a6-107">The address where the call is to be parked must be supplied to the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e51a6-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE não \_ direcionado**</span><span class="sxs-lookup"><span data-stu-id="e51a6-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE\_NONDIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e51a6-109">Especifica o parque de chamada não direcionado.</span><span class="sxs-lookup"><span data-stu-id="e51a6-109">Specifies nondirected call park.</span></span> <span data-ttu-id="e51a6-110">O endereço em que a chamada está estacionada é selecionado pelo comutador e fornecido pelo comutador para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e51a6-110">The address where the call is parked is selected by the switch and provided by the switch to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e51a6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e51a6-111">Remarks</span></span>

<span data-ttu-id="e51a6-112">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="e51a6-112">No extensibility.</span></span> <span data-ttu-id="e51a6-113">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="e51a6-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="e51a6-114">As **\_ constantes LINEPARKMODE** são usadas durante o estacionamento de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="e51a6-114">The **LINEPARKMODE\_ constants** are used when parking a call.</span></span> <span data-ttu-id="e51a6-115">Consulte os recursos de dispositivo de endereço de uma linha para descobrir qual modo de estacionamento está disponível.</span><span class="sxs-lookup"><span data-stu-id="e51a6-115">Consult a line's address device capabilities to find out which park mode is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="e51a6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e51a6-116">Requirements</span></span>



| <span data-ttu-id="e51a6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e51a6-117">Requirement</span></span> | <span data-ttu-id="e51a6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e51a6-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e51a6-119">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e51a6-119">TAPI version</span></span><br/> | <span data-ttu-id="e51a6-120">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e51a6-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e51a6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e51a6-121">Header</span></span><br/>       | <dl> <span data-ttu-id="e51a6-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e51a6-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




