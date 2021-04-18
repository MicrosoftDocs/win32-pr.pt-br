---
description: As \_ constantes de sinalizador de bit LINETRANSFERMODE descrevem diferentes maneiras de resolver solicitações de transferência de chamada.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Constantes de LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781037"
---
# <a name="linetransfermode_-constants"></a><span data-ttu-id="cc6e0-103">\_Constantes LINETRANSFERMODE</span><span class="sxs-lookup"><span data-stu-id="cc6e0-103">LINETRANSFERMODE\_ Constants</span></span>

<span data-ttu-id="cc6e0-104">As constantes de sinalizador de bit **LINETRANSFERMODE \_** descrevem diferentes maneiras de resolver solicitações de transferência de chamada.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-104">The **LINETRANSFERMODE\_** bit-flag constants describe different ways of resolving call transfer requests.</span></span>

<dl> <dt>

<span data-ttu-id="cc6e0-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**\_conferência LINETRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="cc6e0-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc6e0-106">A transferência é resolvida estabelecendo uma conferência de três vias entre o aplicativo, a parte conectada à chamada inicial e a parte conectada à chamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-106">The transfer is resolved by establishing a three-way conference between the application, the party connected to the initial call, and the party connected to the consultation call.</span></span> <span data-ttu-id="cc6e0-107">Uma chamada de conferência é criada quando essa opção é selecionada.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-107">A conference call is created when this option is selected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cc6e0-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**\_transferência LINETRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="cc6e0-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc6e0-109">A transferência é resolvida transferindo a chamada inicial para a chamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-109">The transfer is resolved by transferring the initial call to the consultation call.</span></span> <span data-ttu-id="cc6e0-110">Ambas as chamadas ficarão ociosas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-110">Both calls will become idle to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc6e0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc6e0-111">Remarks</span></span>

<span data-ttu-id="cc6e0-112">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-112">No extensibility.</span></span> <span data-ttu-id="cc6e0-113">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-113">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc6e0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc6e0-114">Requirements</span></span>



| <span data-ttu-id="cc6e0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc6e0-115">Requirement</span></span> | <span data-ttu-id="cc6e0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cc6e0-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cc6e0-117">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cc6e0-117">TAPI version</span></span><br/> | <span data-ttu-id="cc6e0-118">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cc6e0-118">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cc6e0-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc6e0-119">Header</span></span><br/>       | <dl> <span data-ttu-id="cc6e0-120"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc6e0-120"><dt>Tapi.h</dt></span></span> </dl> |



 

 




