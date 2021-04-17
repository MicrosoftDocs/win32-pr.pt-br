---
description: As \_ constantes LINECARDOPTION definem os valores usados no membro dwOptions da estrutura LINECARDENTRY retornada como parte da estrutura LINETRANSLATECAPS retornada por lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Constantes de LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754734"
---
# <a name="linecardoption_-constants"></a><span data-ttu-id="ac7c8-103">\_Constantes LINECARDOPTION</span><span class="sxs-lookup"><span data-stu-id="ac7c8-103">LINECARDOPTION\_ Constants</span></span>

<span data-ttu-id="ac7c8-104">As **\_ constantes LINECARDOPTION** definem os valores usados no membro **dwOptions** da estrutura [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) retornada como parte da estrutura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retornada por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="ac7c8-104">The **LINECARDOPTION\_constants** define values used in the **dwOptions** member of the [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span> <span data-ttu-id="ac7c8-105">As **\_ constantes LINECARDOPTION** t têm os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ac7c8-105">The **LINECARDOPTION\_constants** t has the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ac7c8-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ oculto**</span><span class="sxs-lookup"><span data-stu-id="ac7c8-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION\_HIDDEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac7c8-107">Este cartão de chamada foi ocultado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-107">This calling card has been hidden by the user.</span></span> <span data-ttu-id="ac7c8-108">Ele não é mostrado pelo auxiliar de discagem na lista principal de cartões de chamada disponíveis, mas será mostrado na lista de cartões dos quais as regras de discagem podem ser copiadas.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-108">It is not shown by Dial Helper in the main listing of available calling cards, but will be shown in the list of cards from which dialing rules can be copied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac7c8-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ predefinido**</span><span class="sxs-lookup"><span data-stu-id="ac7c8-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION\_PREDEFINED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac7c8-110">Esse cartão de chamada é uma das definições de cartão de chamada predefinidas incluídas com a telefonia pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-110">This calling card is one of the predefined calling card definitions included with Telephony by Microsoft.</span></span> <span data-ttu-id="ac7c8-111">Ele não pode ser removido totalmente usando o auxiliar de discagem; Se o usuário tentar removê-lo, ele ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-111">It cannot be removed entirely using Dial Helper; if the user attempts to remove it, it will become HIDDEN.</span></span> <span data-ttu-id="ac7c8-112">Portanto, ele continua acessível para cópia de regras de discagem.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-112">It thus continues to be accessible for copying of dialing rules.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac7c8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac7c8-113">Remarks</span></span>

<span data-ttu-id="ac7c8-114">Não extensível.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-114">Not extensible.</span></span> <span data-ttu-id="ac7c8-115">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7c8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac7c8-116">Requirements</span></span>



| <span data-ttu-id="ac7c8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac7c8-117">Requirement</span></span> | <span data-ttu-id="ac7c8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ac7c8-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac7c8-119">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ac7c8-119">TAPI version</span></span><br/> | <span data-ttu-id="ac7c8-120">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ac7c8-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ac7c8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac7c8-121">Header</span></span><br/>       | <dl> <span data-ttu-id="ac7c8-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c8-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




