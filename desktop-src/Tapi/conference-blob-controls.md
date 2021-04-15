---
description: O diagrama a seguir ilustra os principais objetos envolvidos nos controles de blob de conferência TAPI 3. As interfaces mostradas são vinculadas às páginas de referência relevantes.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Controles de blob de conferência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502046"
---
# <a name="conference-blob-controls"></a><span data-ttu-id="25a7c-104">Controles de blob de conferência</span><span class="sxs-lookup"><span data-stu-id="25a7c-104">Conference Blob Controls</span></span>

<span data-ttu-id="25a7c-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="25a7c-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="25a7c-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="25a7c-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="25a7c-107">O diagrama a seguir ilustra os principais objetos envolvidos nos controles de blob de conferência TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="25a7c-107">The following diagram illustrates the main objects involved in TAPI 3 conference blob controls.</span></span> <span data-ttu-id="25a7c-108">As interfaces mostradas são vinculadas às páginas de referência relevantes.</span><span class="sxs-lookup"><span data-stu-id="25a7c-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![controles e interfaces de blob de conferência](images/rendblob.png)

<span data-ttu-id="25a7c-110">O blob de conferência contém informações específicas do provedor em um objeto de conferência.</span><span class="sxs-lookup"><span data-stu-id="25a7c-110">The conference blob contains provider-specific information on a conference object.</span></span> <span data-ttu-id="25a7c-111">Um ponteiro para o blob de interface [**ITConferenceBlob**](itconferenceblob.md) é obtido fazendo um QueryInterface no [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span><span class="sxs-lookup"><span data-stu-id="25a7c-111">A pointer to the [**ITConferenceBlob**](itconferenceblob.md) interface blob is obtained by doing a QueryInterface on [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span></span> <span data-ttu-id="25a7c-112">A interface **ITConferenceBlob** fornece métodos para a manipulação básica de um blob de conferência genérico.</span><span class="sxs-lookup"><span data-stu-id="25a7c-112">The **ITConferenceBlob** interface provides methods for basic manipulation of a generic conference blob.</span></span> <span data-ttu-id="25a7c-113">Um aplicativo que usa blobs de conferência não SDP deve implementar seus próprios métodos para a manipulação de detalhes.</span><span class="sxs-lookup"><span data-stu-id="25a7c-113">An application using non-SDP conference blobs must implement its own methods for detail manipulation.</span></span>

<span data-ttu-id="25a7c-114">A reunião fornece a interface [**ITSdp**](itsdp.md) para manipular blobs de conferência SDP.</span><span class="sxs-lookup"><span data-stu-id="25a7c-114">Rendezvous provides the [**ITSdp**](itsdp.md) interface for manipulating SDP conference blobs.</span></span> <span data-ttu-id="25a7c-115">O SDP é um protocolo para descrever as sessões de multimídia e suas informações de agendamento relacionadas.</span><span class="sxs-lookup"><span data-stu-id="25a7c-115">The SDP is a protocol for describing multimedia sessions and their related scheduling information.</span></span> <span data-ttu-id="25a7c-116">Para obter informações adicionais sobre o protocolo SDP, localize Internet Engineering Task Force (IETF) RFC 2327 intitulado "SDP: Session description protocol".</span><span class="sxs-lookup"><span data-stu-id="25a7c-116">For additional information on the SDP protocol, locate Internet Engineering Task Force (IETF) RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="25a7c-117">Se a interface **ITSDP** existir para um determinado blob de conferência, você poderá obter um ponteiro para ele fazendo um **QueryInterface** no [**ITConferenceBlob**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="25a7c-117">If the **ITSDP** interface exists for a given conference blob, you can obtain a pointer to it by doing a **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

<span data-ttu-id="25a7c-118">Para BLOBs de conferência SDP, as interfaces [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)e [**ITMedia**](itmedia.md) permitem um controle detalhado do tempo de conferência do SDP e das características de mídia.</span><span class="sxs-lookup"><span data-stu-id="25a7c-118">For SDP conference blobs, the [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md), and [**ITMedia**](itmedia.md) interfaces allow detailed control of SDP conference time and media characteristics.</span></span>

 

 



