---
description: As \_ constantes de sinalizador de bit LINEADDRESSSHARING descrevem várias maneiras como um endereço pode ser compartilhado entre as linhas.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Constantes de LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783363"
---
# <a name="lineaddresssharing_-constants"></a><span data-ttu-id="c2273-103">\_Constantes LINEADDRESSSHARING</span><span class="sxs-lookup"><span data-stu-id="c2273-103">LINEADDRESSSHARING\_ Constants</span></span>

<span data-ttu-id="c2273-104">As constantes de sinalizador de bit **LINEADDRESSSHARING \_** descrevem várias maneiras como um endereço pode ser compartilhado entre as linhas.</span><span class="sxs-lookup"><span data-stu-id="c2273-104">The **LINEADDRESSSHARING\_** bit-flag constants describe various ways an address can be shared between lines.</span></span>

<dl> <dt>

<span data-ttu-id="c2273-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ privado**</span><span class="sxs-lookup"><span data-stu-id="c2273-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2273-106">O endereço é privado para a linha do usuário; Ele não está atribuído a nenhuma outra estação.</span><span class="sxs-lookup"><span data-stu-id="c2273-106">The address is private to the user's line; it is not assigned to any other station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2273-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**</span><span class="sxs-lookup"><span data-stu-id="c2273-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING\_BRIDGEDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2273-108">O endereço é ponte para uma ou mais estações.</span><span class="sxs-lookup"><span data-stu-id="c2273-108">The address is bridged to one or more other stations.</span></span> <span data-ttu-id="c2273-109">A primeira linha para ativar uma chamada na linha terá acesso exclusivo ao endereço e às chamadas que podem existir nele.</span><span class="sxs-lookup"><span data-stu-id="c2273-109">The first line to activate a call on the line will have exclusive access to the address and calls that may exist on it.</span></span> <span data-ttu-id="c2273-110">Outras linhas não poderão usar o endereço de ponte enquanto estiverem em uso.</span><span class="sxs-lookup"><span data-stu-id="c2273-110">Other lines will not be able to use the bridged address while it is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2273-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**</span><span class="sxs-lookup"><span data-stu-id="c2273-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING\_BRIDGEDNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2273-112">O endereço é ponte com uma ou mais estações.</span><span class="sxs-lookup"><span data-stu-id="c2273-112">The address is bridged with one or more other stations.</span></span> <span data-ttu-id="c2273-113">A primeira linha para ativar uma chamada na linha terá acesso exclusivo apenas à chamada correspondente.</span><span class="sxs-lookup"><span data-stu-id="c2273-113">The first line to activate a call on the line will have exclusive access to only the corresponding call.</span></span> <span data-ttu-id="c2273-114">Outros aplicativos que usam o endereço resultarão em aparências de chamada novas e separadas.</span><span class="sxs-lookup"><span data-stu-id="c2273-114">Other applications that use the address will result in new and separate call appearances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2273-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**</span><span class="sxs-lookup"><span data-stu-id="c2273-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING\_BRIDGEDSHARED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2273-116">O endereço é ponte com uma ou mais linhas.</span><span class="sxs-lookup"><span data-stu-id="c2273-116">The address is bridged with one or more other lines.</span></span> <span data-ttu-id="c2273-117">Todas as partes com ponte podem compartilhar em chamadas no endereço, que, em seguida, funciona como uma conferência.</span><span class="sxs-lookup"><span data-stu-id="c2273-117">All bridged parties can share in calls on the address, which then functions as a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2273-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ monitorado**</span><span class="sxs-lookup"><span data-stu-id="c2273-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING\_MONITORED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2273-119">Esse é um endereço cujo status ocioso/ocupado é disponibilizado para esta linha.</span><span class="sxs-lookup"><span data-stu-id="c2273-119">This is an address whose idle/busy status is made available to this line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2273-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2273-120">Remarks</span></span>

<span data-ttu-id="c2273-121">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="c2273-121">No extensibility.</span></span> <span data-ttu-id="c2273-122">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="c2273-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="c2273-123">A maneira como um endereço é compartilhado entre as linhas pode afetar o comportamento desse endereço.</span><span class="sxs-lookup"><span data-stu-id="c2273-123">The way in which an address is shared across lines can affect the behavior of that address.</span></span> <span data-ttu-id="c2273-124">[**Linha \_ As mensagens CALLstate**](line-callstate.md) e [**line \_ addressstate**](line-addressstate.md) são enviadas para o aplicativo em resposta às atividades pelas estações de pontes.</span><span class="sxs-lookup"><span data-stu-id="c2273-124">[**LINE\_CALLSTATE**](line-callstate.md) and [**LINE\_ADDRESSSTATE**](line-addressstate.md) messages are sent to the application in response to activities by the bridging stations.</span></span> <span data-ttu-id="c2273-125">É por meio dessas mensagens que um aplicativo pode acompanhar o status do endereço.</span><span class="sxs-lookup"><span data-stu-id="c2273-125">It is through these messages that an application can track the status of the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2273-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2273-126">Requirements</span></span>



| <span data-ttu-id="c2273-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2273-127">Requirement</span></span> | <span data-ttu-id="c2273-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c2273-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c2273-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c2273-129">TAPI version</span></span><br/> | <span data-ttu-id="c2273-130">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c2273-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c2273-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2273-131">Header</span></span><br/>       | <dl> <span data-ttu-id="c2273-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2273-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2273-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2273-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2273-134">**Endereço de LINHAstate \_**</span><span class="sxs-lookup"><span data-stu-id="c2273-134">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="c2273-135">**chamada de LINHAstate \_**</span><span class="sxs-lookup"><span data-stu-id="c2273-135">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> </dl>

 

 




