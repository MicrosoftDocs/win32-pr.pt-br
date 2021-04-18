---
description: As \_ constantes de sinalizador de bit PHONEPRIVILEGE descrevem as várias maneiras em que um dispositivo de telefone pode ser aberto.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Constantes de PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760149"
---
# <a name="phoneprivilege_-constants"></a><span data-ttu-id="6a7e0-103">\_Constantes PHONEPRIVILEGE</span><span class="sxs-lookup"><span data-stu-id="6a7e0-103">PHONEPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="6a7e0-104">As constantes de sinalizador de bit **PHONEPRIVILEGE \_** descrevem as várias maneiras em que um dispositivo de telefone pode ser aberto.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-104">The **PHONEPRIVILEGE\_** bit-flag constants describe the various ways in which a phone device can be opened.</span></span>

<dl> <dt>

<span data-ttu-id="6a7e0-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**MONITOR de PHONEPRIVILEGE \_**</span><span class="sxs-lookup"><span data-stu-id="6a7e0-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a7e0-106">Um aplicativo que abre um dispositivo de telefone com o privilégio de monitor é informado sobre eventos e alterações de estado que ocorrem no telefone.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-106">An application that opens a phone device with the monitor privilege is informed about events and state changes occurring on the phone.</span></span> <span data-ttu-id="6a7e0-107">O aplicativo não pode invocar nenhuma operação no dispositivo de telefone que alteraria seu estado, portanto, somente as operações de status podem ser invocadas.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-107">The application cannot invoke any operations on the phone device that would change its state, so only status operations can be invoked.</span></span> <span data-ttu-id="6a7e0-108">Vários aplicativos podem monitorar um dispositivo de telefone em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-108">Multiple applications can monitor a phone device at any given time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a7e0-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**proprietário do PHONEPRIVILEGE \_**</span><span class="sxs-lookup"><span data-stu-id="6a7e0-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a7e0-110">Um aplicativo que abre um dispositivo de telefone com o privilégio de proprietário tem permissão para alterar o estado das lâmpadas, do toque, da exibição, da Hookswitch e dos blocos de dados do telefone.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-110">An application that opens a phone device with the owner privilege is allowed to change the state of the lamps, ringer, display, hookswitch, and data blocks of the phone.</span></span> <span data-ttu-id="6a7e0-111">Abrir um dispositivo de telefone no modo de proprietário também fornece o monitoramento do dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-111">Opening a phone device in owner mode also provides monitoring of the phone device.</span></span> <span data-ttu-id="6a7e0-112">Somente um aplicativo pode ser o proprietário de um dispositivo de telefone em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-112">Only one application is allowed to be the owner of a phone device at any given time.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a7e0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a7e0-113">Remarks</span></span>

<span data-ttu-id="6a7e0-114">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-114">No extensibility.</span></span> <span data-ttu-id="6a7e0-115">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="6a7e0-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a7e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a7e0-116">Requirements</span></span>



| <span data-ttu-id="6a7e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a7e0-117">Requirement</span></span> | <span data-ttu-id="6a7e0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6a7e0-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6a7e0-119">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="6a7e0-119">TAPI version</span></span><br/> | <span data-ttu-id="6a7e0-120">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6a7e0-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6a7e0-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a7e0-121">Header</span></span><br/>       | <dl> <span data-ttu-id="6a7e0-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a7e0-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




