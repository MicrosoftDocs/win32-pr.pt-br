---
description: A TAPI 3 envolve vários objetos que são independentes de seus cinco objetos principais da TAPI (TAPI, endereço, chamada, CallHub e terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Objetos Stand-Alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828331"
---
# <a name="stand-alone-objects"></a><span data-ttu-id="8e0a9-103">Objetos Stand-Alone</span><span class="sxs-lookup"><span data-stu-id="8e0a9-103">Stand-Alone Objects</span></span>

<span data-ttu-id="8e0a9-104">A TAPI 3 envolve vários objetos que são independentes de seus cinco objetos principais da TAPI (TAPI, endereço, chamada, CallHub e terminal).</span><span class="sxs-lookup"><span data-stu-id="8e0a9-104">TAPI 3 involves a number of objects that are independent of its five main TAPI objects (TAPI, Address, Call, CallHub, and Terminal).</span></span> <span data-ttu-id="8e0a9-105">[Interfaces de evento](./event-interfaces.md) e [interfaces de enumerador](enumerator-interfaces.md) são objetos autônomos e são resumidas separadamente.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-105">[Event Interfaces](./event-interfaces.md) and [Enumerator Interfaces](enumerator-interfaces.md) are stand-alone objects, and are summarized separately.</span></span> <span data-ttu-id="8e0a9-106">Veja a seguir um resumo das interfaces autônomas que não são de evento e não do enumerador.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-106">The following summarizes non-event and non-enumerator stand-alone interfaces.</span></span>



| <span data-ttu-id="8e0a9-107">Interface</span><span class="sxs-lookup"><span data-stu-id="8e0a9-107">Interface</span></span>                                             | <span data-ttu-id="8e0a9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e0a9-108">Description</span></span>                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e0a9-109">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-109">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | <span data-ttu-id="8e0a9-110">Fornece métodos para permitir que aplicativos cliente de automação, como Visual Basic, recuperem informações de coleção.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-110">Provides methods to allow Automation client applications such as Visual Basic to retrieve collection information.</span></span>                                                                                             |
| [<span data-ttu-id="8e0a9-111">**ITCollection2**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-111">**ITCollection2**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | <span data-ttu-id="8e0a9-112">Estende o [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) fornecendo métodos adicionais para modificar coleções.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-112">Extends [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) by providing additional methods for modifying collections.</span></span>                                                                                                       |
| [<span data-ttu-id="8e0a9-113">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-113">**IDispatch**</span></span>](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | <span data-ttu-id="8e0a9-114">Interface COM padrão para implementar a automação.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-114">Standard COM interface for implementing Automation.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="8e0a9-115">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-115">**IUnknown**</span></span>](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | <span data-ttu-id="8e0a9-116">Interface COM padrão para obter ponteiros para interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-116">Standard COM interface for getting pointers to object interfaces.</span></span>                                                                                                                                             |
| [<span data-ttu-id="8e0a9-117">**ITDispatchMapper**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-117">**ITDispatchMapper**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | <span data-ttu-id="8e0a9-118">Permite que um aplicativo recupere o ponteiro de expedição de outra interface em um objeto, dado um ponteiro atual do [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) .</span><span class="sxs-lookup"><span data-stu-id="8e0a9-118">Allows an application to retrieve the dispatch pointer of another interface on an object, given a current [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) pointer.</span></span> <span data-ttu-id="8e0a9-119">Útil para algumas linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-119">Useful for some scripting languages.</span></span> |
| [<span data-ttu-id="8e0a9-120">**ITRequest**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-120">**ITRequest**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | <span data-ttu-id="8e0a9-121">Fornece métodos que permitem que um aplicativo TAPI 3 Use [telefonia assistida](assisted-telephony-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8e0a9-121">Provides methods that allow a TAPI 3 application to use [Assisted Telephony](assisted-telephony-overview.md).</span></span>                                                                                                |



 



| <span data-ttu-id="8e0a9-122">Interface</span><span class="sxs-lookup"><span data-stu-id="8e0a9-122">Interface</span></span>                                  | <span data-ttu-id="8e0a9-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e0a9-123">Description</span></span>                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e0a9-124">**ITMediaControl**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-124">**ITMediaControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | <span data-ttu-id="8e0a9-125">Inicia, interrompe e pausa as ações atuais, como uma reprodução.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-125">Starts, stops, and pauses current actions, such as a playback.</span></span>                                                                                                             |
| [<span data-ttu-id="8e0a9-126">**ITMediaPlayback**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-126">**ITMediaPlayback**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | <span data-ttu-id="8e0a9-127">Fornece métodos específicos de reprodução que permitem que um aplicativo execute essas operações como definir a lista de arquivos para reproduzir e alterar a velocidade de reprodução.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-127">Provides playback-specific methods that allow an application to perform such operations as setting the list of files to play and changing the playback speed.</span></span>              |
| [<span data-ttu-id="8e0a9-128">**ITMediaRecord**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-128">**ITMediaRecord**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | <span data-ttu-id="8e0a9-129">Fornece métodos específicos de gravação que permitem que um aplicativo execute essas operações como definir os nomes dos arquivos para registrar e alterar a duração de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-129">Provides recording-specific methods that allow an application to perform such operations as setting the names of files to record and changing the duration of a recording.</span></span> |



 



| <span data-ttu-id="8e0a9-130">Interface</span><span class="sxs-lookup"><span data-stu-id="8e0a9-130">Interface</span></span>                                                  | <span data-ttu-id="8e0a9-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e0a9-131">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e0a9-132">**ITScriptableAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-132">**ITScriptableAudioFormat**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | <span data-ttu-id="8e0a9-133">Recupera o formato de áudio do ou define o formato de áudio para um controle.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-133">Retrieves the audio format from, or sets the audio format for, a track.</span></span>                                                                                             |
| [<span data-ttu-id="8e0a9-134">**ITStaticAudioTerminal**</span><span class="sxs-lookup"><span data-stu-id="8e0a9-134">**ITStaticAudioTerminal**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | <span data-ttu-id="8e0a9-135">Fornece métodos em objetos de terminal de áudio estáticos que são necessários para dar suporte a dispositivos de telefone.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-135">Provides methods on static audio terminal objects that are needed to support phone devices.</span></span> <span data-ttu-id="8e0a9-136">A TAPI 3,1 MSPs deve expor essa interface em todos os terminais de áudio estáticos.</span><span class="sxs-lookup"><span data-stu-id="8e0a9-136">TAPI 3.1 MSPs must expose this interface on all static audio terminals.</span></span> |



 

 

 
