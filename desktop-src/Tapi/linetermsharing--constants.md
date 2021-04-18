---
description: As \_ constantes de sinalizador de bit LINETERMSHARING descrevem diferentes maneiras em que um terminal pode ser compartilhado entre dispositivos de linha, endereços ou chamadas.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Constantes de LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760334"
---
# <a name="linetermsharing_-constants"></a><span data-ttu-id="cf73e-103">\_Constantes LINETERMSHARING</span><span class="sxs-lookup"><span data-stu-id="cf73e-103">LINETERMSHARING\_ Constants</span></span>

<span data-ttu-id="cf73e-104">As constantes de sinalizador de bit **LINETERMSHARING \_** descrevem diferentes maneiras em que um terminal pode ser compartilhado entre dispositivos de linha, endereços ou chamadas.</span><span class="sxs-lookup"><span data-stu-id="cf73e-104">The **LINETERMSHARING\_** bit-flag constants describe different ways in which a terminal can be shared between line devices, addresses, or calls.</span></span>

<dl> <dt>

<span data-ttu-id="cf73e-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ privado**</span><span class="sxs-lookup"><span data-stu-id="cf73e-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cf73e-106">O dispositivo de terminal é privado para um dispositivo de linha única.</span><span class="sxs-lookup"><span data-stu-id="cf73e-106">The terminal device is private to a single line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf73e-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**</span><span class="sxs-lookup"><span data-stu-id="cf73e-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING\_SHAREDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cf73e-108">O dispositivo de terminal pode ser usado por várias linhas.</span><span class="sxs-lookup"><span data-stu-id="cf73e-108">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="cf73e-109">As solicitações de [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) dos vários terminais acabam sendo mescladas ou enconferênciadas no terminal.</span><span class="sxs-lookup"><span data-stu-id="cf73e-109">The [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) requests of the various terminals end up being merged or conferenced at the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf73e-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**</span><span class="sxs-lookup"><span data-stu-id="cf73e-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING\_SHAREDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cf73e-111">O dispositivo de terminal pode ser usado por várias linhas.</span><span class="sxs-lookup"><span data-stu-id="cf73e-111">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="cf73e-112">O último dispositivo de linha para fazer um [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) ou [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) para o terminal para um determinado modo de terminal terá uma conexão exclusiva com o terminal para esse modo.</span><span class="sxs-lookup"><span data-stu-id="cf73e-112">The last line device to do a [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) or [**TSPI\_lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) to the terminal for a given terminal mode will have exclusive connection to the terminal for that mode.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf73e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf73e-113">Remarks</span></span>

<span data-ttu-id="cf73e-114">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="cf73e-114">No extensibility.</span></span> <span data-ttu-id="cf73e-115">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="cf73e-115">All 32 bits are reserved.</span></span>

<span data-ttu-id="cf73e-116">Essas constantes descrevem as classes de fluxo de controle e de informações que podem ser roteadas diretamente entre um dispositivo de linha e um dispositivo de terminal (como um conjunto de telefone).</span><span class="sxs-lookup"><span data-stu-id="cf73e-116">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf73e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf73e-117">Requirements</span></span>



| <span data-ttu-id="cf73e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf73e-118">Requirement</span></span> | <span data-ttu-id="cf73e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cf73e-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cf73e-120">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cf73e-120">TAPI version</span></span><br/> | <span data-ttu-id="cf73e-121">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cf73e-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cf73e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf73e-122">Header</span></span><br/>       | <dl> <span data-ttu-id="cf73e-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf73e-123"><dt>Tapi.h</dt></span></span> </dl> |



 

