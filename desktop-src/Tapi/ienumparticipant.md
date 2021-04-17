---
description: 'A interface IEnumParticipant fornece métodos de enumeração de padrão COM para a interface ITParticipant. O método ITParticipantControl:: EnumerateParticipants retorna um ponteiro para IEnumParticipant.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interface IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783369"
---
# <a name="ienumparticipant-interface"></a><span data-ttu-id="95899-104">Interface IEnumParticipant</span><span class="sxs-lookup"><span data-stu-id="95899-104">IEnumParticipant interface</span></span>

<span data-ttu-id="95899-105">\[O **IEnumParticipant** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="95899-105">\[**IEnumParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="95899-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="95899-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="95899-107">A interface **IEnumParticipant** fornece métodos de enumeração de padrão com para a interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="95899-107">The **IEnumParticipant** interface provides COM-standard enumeration methods for the [**ITParticipant**](itparticipant.md) interface.</span></span> <span data-ttu-id="95899-108">O método [**ITParticipantControl:: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) retorna um ponteiro para **IEnumParticipant**.</span><span class="sxs-lookup"><span data-stu-id="95899-108">The [**ITParticipantControl::EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method returns a pointer to **IEnumParticipant**.</span></span>

<span data-ttu-id="95899-109">A interface **IEnumParticipant** está oculta das linguagens de Visual Basic e script.</span><span class="sxs-lookup"><span data-stu-id="95899-109">The **IEnumParticipant** interface is hidden from Visual Basic and scripting languages.</span></span>

## <a name="members"></a><span data-ttu-id="95899-110">Membros</span><span class="sxs-lookup"><span data-stu-id="95899-110">Members</span></span>

<span data-ttu-id="95899-111">A interface **IEnumParticipant** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="95899-111">The **IEnumParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="95899-112">**IEnumParticipant** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="95899-112">**IEnumParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="95899-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="95899-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="95899-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="95899-114">Methods</span></span>

<span data-ttu-id="95899-115">A interface **IEnumParticipant** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="95899-115">The **IEnumParticipant** interface has these methods.</span></span>



| <span data-ttu-id="95899-116">Método</span><span class="sxs-lookup"><span data-stu-id="95899-116">Method</span></span>                                  | <span data-ttu-id="95899-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="95899-117">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95899-118">**8i**</span><span class="sxs-lookup"><span data-stu-id="95899-118">**Clone**</span></span>](ienumparticipant-clone.md) | <span data-ttu-id="95899-119">Cria outro enumerador que contém o mesmo estado de enumeração do atual.</span><span class="sxs-lookup"><span data-stu-id="95899-119">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="95899-120">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="95899-120">**Next**</span></span>](ienumparticipant-next.md)   | <span data-ttu-id="95899-121">Obtém o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="95899-121">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="95899-122">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="95899-122">**Reset**</span></span>](ienumparticipant-reset.md) | <span data-ttu-id="95899-123">Redefine para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="95899-123">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="95899-124">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="95899-124">**Skip**</span></span>](ienumparticipant-skip.md)   | <span data-ttu-id="95899-125">Ignora o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="95899-125">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="95899-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95899-126">Requirements</span></span>



| <span data-ttu-id="95899-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="95899-127">Requirement</span></span> | <span data-ttu-id="95899-128">Valor</span><span class="sxs-lookup"><span data-stu-id="95899-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95899-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="95899-129">TAPI version</span></span><br/> | <span data-ttu-id="95899-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="95899-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="95899-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95899-131">Header</span></span><br/>       | <dl> <span data-ttu-id="95899-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="95899-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="95899-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95899-133">Library</span></span><br/>      | <dl> <span data-ttu-id="95899-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95899-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="95899-135">DLL</span><span class="sxs-lookup"><span data-stu-id="95899-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="95899-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95899-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="95899-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="95899-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95899-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="95899-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

