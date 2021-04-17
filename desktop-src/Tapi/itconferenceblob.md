---
description: Manipula uma descrição de conferência textual.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interface ITConferenceBlob (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761822"
---
# <a name="itconferenceblob-interface"></a><span data-ttu-id="b96c4-103">Interface ITConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="b96c4-103">ITConferenceBlob interface</span></span>

<span data-ttu-id="b96c4-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b96c4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b96c4-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b96c4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b96c4-106">A interface **ITConferenceBlob** manipula uma descrição de conferência textual.</span><span class="sxs-lookup"><span data-stu-id="b96c4-106">The **ITConferenceBlob** interface manipulates a textual conference description.</span></span> <span data-ttu-id="b96c4-107">A interface destina-se a ser independente do formato e da sintaxe da descrição da conferência.</span><span class="sxs-lookup"><span data-stu-id="b96c4-107">The interface is intended to be independent of the format and syntax of the conference description.</span></span> <span data-ttu-id="b96c4-108">Para manipular aspectos específicos da descrição da conferência, o aplicativo deve consultar outra interface.</span><span class="sxs-lookup"><span data-stu-id="b96c4-108">To manipulate specific aspects of the conference description, the application must query for another interface.</span></span> <span data-ttu-id="b96c4-109">Atualmente, há suporte apenas para descrições de conferências SDP; o aplicativo deve usar **QueryInterface** para [**ITSdp**](itsdp.md) para acessar os vários campos da descrição da conferência SDP.</span><span class="sxs-lookup"><span data-stu-id="b96c4-109">Currently, only SDP conference descriptions are supported; the application must use **QueryInterface** for [**ITSdp**](itsdp.md) to access the various fields of the SDP conference description.</span></span> <span data-ttu-id="b96c4-110">A interface **ITConferenceBlob** é criada chamando **QueryInterface** no [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="b96c4-110">The **ITConferenceBlob** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="b96c4-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b96c4-111">Members</span></span>

<span data-ttu-id="b96c4-112">A interface **ITConferenceBlob** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b96c4-112">The **ITConferenceBlob** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b96c4-113">**ITConferenceBlob** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b96c4-113">**ITConferenceBlob** also has these types of members:</span></span>

-   [<span data-ttu-id="b96c4-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b96c4-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b96c4-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="b96c4-115">Methods</span></span>

<span data-ttu-id="b96c4-116">A interface **ITConferenceBlob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b96c4-116">The **ITConferenceBlob** interface has these methods.</span></span>



| <span data-ttu-id="b96c4-117">Método</span><span class="sxs-lookup"><span data-stu-id="b96c4-117">Method</span></span>                                                             | <span data-ttu-id="b96c4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b96c4-118">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b96c4-119">**obter \_ CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="b96c4-119">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)     | <span data-ttu-id="b96c4-120">Obtém o indicador de [**\_ \_ conjunto de caracteres de blob**](blob-character-set.md) de se os caracteres de blob estão em ASCII, Unicode e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b96c4-120">Gets the [**BLOB\_CHARACTER\_SET**](blob-character-set.md) indicator of whether blob characters are in ASCII, Unicode, and so on.</span></span><br/> |
| [<span data-ttu-id="b96c4-121">**obter \_ ConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="b96c4-121">**get\_ConferenceBlob**</span></span>](itconferenceblob-get-conferenceblob.md) | <span data-ttu-id="b96c4-122">Obtém um ponteiro para o blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="b96c4-122">Gets a pointer to the conference blob.</span></span><br/>                                                                                             |
| [<span data-ttu-id="b96c4-123">**Init**</span><span class="sxs-lookup"><span data-stu-id="b96c4-123">**Init**</span></span>](itconferenceblob-init.md)                              | <span data-ttu-id="b96c4-124">Inicializa o blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="b96c4-124">Initializes the conference blob.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="b96c4-125">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="b96c4-125">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)    | <span data-ttu-id="b96c4-126">Confirma as alterações no blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="b96c4-126">Commits changes to the conference blob.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="b96c4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b96c4-127">Requirements</span></span>



| <span data-ttu-id="b96c4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b96c4-128">Requirement</span></span> | <span data-ttu-id="b96c4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b96c4-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b96c4-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b96c4-130">TAPI version</span></span><br/> | <span data-ttu-id="b96c4-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b96c4-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b96c4-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b96c4-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b96c4-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b96c4-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b96c4-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b96c4-134">Library</span></span><br/>      | <dl> <span data-ttu-id="b96c4-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b96c4-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b96c4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b96c4-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="b96c4-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b96c4-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

