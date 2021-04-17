---
description: As \_ constantes LINETSPIOPTION descrevem os provedores de serviço de pedidos que devem ser chamados.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Constantes de LINETSPIOPTION_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780118"
---
# <a name="linetspioption_-constants"></a><span data-ttu-id="2e254-103">\_Constantes LINETSPIOPTION</span><span class="sxs-lookup"><span data-stu-id="2e254-103">LINETSPIOPTION\_ Constants</span></span>

<span data-ttu-id="2e254-104">As **\_ constantes LINETSPIOPTION** descrevem os provedores de serviço de pedidos que devem ser chamados.</span><span class="sxs-lookup"><span data-stu-id="2e254-104">The **LINETSPIOPTION\_ constants** describes the order service providers should be called.</span></span>

<dl> <dt>

<span data-ttu-id="2e254-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**</span><span class="sxs-lookup"><span data-stu-id="2e254-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION\_NONREENTRANT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e254-106">A TAPI deve chamar funções neste provedor de serviços, uma de cada vez; Ele deve aguardar a conclusão de cada função (mas não para que as funções assíncronas sejam concluídas) antes de chamar a mesma ou outra função, seja na mesma ou em um thread diferente, no mesmo ou em um processador diferente.</span><span class="sxs-lookup"><span data-stu-id="2e254-106">TAPI should call functions in this service provider one at a time; it should wait from each function to return (but not for asynchronous functions to complete) before calling the same or another function, either on the same or a different thread, on the same or a different processor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e254-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e254-107">Requirements</span></span>



| <span data-ttu-id="2e254-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e254-108">Requirement</span></span> | <span data-ttu-id="2e254-109">Valor</span><span class="sxs-lookup"><span data-stu-id="2e254-109">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2e254-110">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="2e254-110">TAPI version</span></span><br/> | <span data-ttu-id="2e254-111">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2e254-111">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2e254-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e254-112">Header</span></span><br/>       | <dl> <span data-ttu-id="2e254-113"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e254-113"><dt>Tspi.h</dt></span></span> </dl> |



 

 




