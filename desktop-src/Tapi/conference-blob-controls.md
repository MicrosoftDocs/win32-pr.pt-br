---
description: O diagrama a seguir ilustra os principais objetos envolvidos nos controles de blob de conferência TAPI 3. As interfaces mostradas são vinculadas às páginas de referência relevantes.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Controles de blob de conferência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1361951fcb830676e36acb4ec397832629dc5745983c654317a457a0d66ac336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867984"
---
# <a name="conference-blob-controls"></a>Controles de blob de conferência

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O diagrama a seguir ilustra os principais objetos envolvidos nos controles de blob de conferência TAPI 3. As interfaces mostradas são vinculadas às páginas de referência relevantes.

![controles e interfaces de blob de conferência](images/rendblob.png)

O blob de conferência contém informações específicas do provedor em um objeto de conferência. Um ponteiro para o blob de interface [**ITConferenceBlob**](itconferenceblob.md) é obtido fazendo um QueryInterface no [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference). A interface **ITConferenceBlob** fornece métodos para a manipulação básica de um blob de conferência genérico. Um aplicativo que usa blobs de conferência não SDP deve implementar seus próprios métodos para a manipulação de detalhes.

A reunião fornece a interface [**ITSdp**](itsdp.md) para manipular blobs de conferência SDP. O SDP é um protocolo para descrever as sessões de multimídia e suas informações de agendamento relacionadas. Para obter informações adicionais sobre o protocolo SDP, localize Internet Engineering Task Force (IETF) RFC 2327 intitulado "SDP: Session description protocol". Se a interface **ITSDP** existir para um determinado blob de conferência, você poderá obter um ponteiro para ele fazendo um **QueryInterface** no [**ITConferenceBlob**](itconferenceblob.md).

Para BLOBs de conferência SDP, as interfaces [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)e [**ITMedia**](itmedia.md) permitem um controle detalhado do tempo de conferência do SDP e das características de mídia.

 

 



