---
description: A interface ITAttributeList fornece métodos para obter e definir atributos não interpretados.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interface ITAttributeList (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761963"
---
# <a name="itattributelist-interface"></a><span data-ttu-id="8c7c4-103">Interface ITAttributeList</span><span class="sxs-lookup"><span data-stu-id="8c7c4-103">ITAttributeList interface</span></span>

<span data-ttu-id="8c7c4-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8c7c4-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8c7c4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8c7c4-106">A interface **ITAttributeList** fornece métodos para obter e definir atributos não interpretados.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-106">The **ITAttributeList** interface supplies methods for getting and setting of uninterpreted attributes.</span></span> <span data-ttu-id="8c7c4-107">Sobre a posição das cadeias de caracteres de atributo em um pacote de protocolo de descritor de sessão (SDP, consulte RFC 2327), os métodos pressupõem que todas as cadeias de caracteres de atributo existam logo antes que os atributos de mídia sejam especificados e depois de todos os atributos comuns.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-107">Regarding the position of the attribute strings in a Session Descriptor Protocol (SDP, see RFC 2327) packet, the methods assume that all attribute strings exist just before the media attributes are specified and after all the common attributes.</span></span> <span data-ttu-id="8c7c4-108">A interface **ITAttributeList** é criada chamando **QueryInterface** no [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="8c7c4-108">The **ITAttributeList** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="8c7c4-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8c7c4-109">Members</span></span>

<span data-ttu-id="8c7c4-110">A interface **ITAttributeList** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8c7c4-110">The **ITAttributeList** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8c7c4-111">**ITAttributeList** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8c7c4-111">**ITAttributeList** also has these types of members:</span></span>

-   [<span data-ttu-id="8c7c4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8c7c4-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8c7c4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8c7c4-113">Methods</span></span>

<span data-ttu-id="8c7c4-114">A interface **ITAttributeList** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-114">The **ITAttributeList** interface has these methods.</span></span>



| <span data-ttu-id="8c7c4-115">Método</span><span class="sxs-lookup"><span data-stu-id="8c7c4-115">Method</span></span>                                                          | <span data-ttu-id="8c7c4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c7c4-116">Description</span></span>                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="8c7c4-117">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="8c7c4-117">**Add**</span></span>](itattributelist-add.md)                              | <span data-ttu-id="8c7c4-118">Adiciona o atributo no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-118">Adds the attribute at the specified index.</span></span><br/>   |
| [<span data-ttu-id="8c7c4-119">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="8c7c4-119">**Delete**</span></span>](itattributelist-delete.md)                        | <span data-ttu-id="8c7c4-120">Exclui o atributo no índice especificado</span><span class="sxs-lookup"><span data-stu-id="8c7c4-120">Deletes the attribute at the specified index</span></span><br/> |
| [<span data-ttu-id="8c7c4-121">**obter \_ atributolist**</span><span class="sxs-lookup"><span data-stu-id="8c7c4-121">**get\_AttributeList**</span></span>](itattributelist-get-attributelist.md) | <span data-ttu-id="8c7c4-122">Obtém a lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-122">Gets the list of attributes.</span></span><br/>                 |
| [<span data-ttu-id="8c7c4-123">**obter \_ contagem**</span><span class="sxs-lookup"><span data-stu-id="8c7c4-123">**get\_Count**</span></span>](itattributelist-get-count.md)                 | <span data-ttu-id="8c7c4-124">Obtém o número de atributos.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-124">Gets the number of attributes.</span></span><br/>               |
| [<span data-ttu-id="8c7c4-125">**obter \_ Item**</span><span class="sxs-lookup"><span data-stu-id="8c7c4-125">**get\_Item**</span></span>](itattributelist-get-item.md)                   | <span data-ttu-id="8c7c4-126">Obtém o atributo especificado pelo índice.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-126">Gets the attribute specified by the index.</span></span><br/>   |
| [<span data-ttu-id="8c7c4-127">**colocar \_ atributolist**</span><span class="sxs-lookup"><span data-stu-id="8c7c4-127">**put\_AttributeList**</span></span>](itattributelist-put-attributelist.md) | <span data-ttu-id="8c7c4-128">Define a lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="8c7c4-128">Sets the list of attributes.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="8c7c4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c7c4-129">Requirements</span></span>



| <span data-ttu-id="8c7c4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c7c4-130">Requirement</span></span> | <span data-ttu-id="8c7c4-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8c7c4-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7c4-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8c7c4-132">TAPI version</span></span><br/> | <span data-ttu-id="8c7c4-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8c7c4-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8c7c4-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c7c4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8c7c4-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c7c4-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c7c4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c7c4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="8c7c4-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c7c4-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8c7c4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8c7c4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="8c7c4-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c7c4-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

