---
description: Para estabelecer uma conexão entre um cliente e um servidor usando o protocolo SMB da Microsoft, primeiro você deve determinar o dialeto com o nível mais alto de funcionalidade que o cliente e o servidor dão suporte.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Dialetos do protocolo SMB da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461062"
---
# <a name="microsoft-smb-protocol-dialects"></a><span data-ttu-id="22a17-103">Dialetos do protocolo SMB da Microsoft</span><span class="sxs-lookup"><span data-stu-id="22a17-103">Microsoft SMB Protocol Dialects</span></span>

<span data-ttu-id="22a17-104">A lista de pacotes de mensagens do protocolo SMB da Microsoft cresceu ao longo dos anos para acomodar a funcionalidade crescente do protocolo SMB da Microsoft e, agora, os números nos centenas.</span><span class="sxs-lookup"><span data-stu-id="22a17-104">The list of Microsoft SMB Protocol message packets has grown over the years to accommodate the increasing functionality of Microsoft SMB Protocol, and now numbers in the hundreds.</span></span> <span data-ttu-id="22a17-105">Cada estágio de seu crescimento é marcado por um conjunto de pacotes padrão, ou dialeto.</span><span class="sxs-lookup"><span data-stu-id="22a17-105">Each stage of its growth is marked by a standard packet set, or dialect.</span></span> <span data-ttu-id="22a17-106">Cada dialeto é identificado por uma cadeia de caracteres padrão, como "PC NETWORK PROGRAM 1,0", "MICROSOFT NETWORKs 3,0", "DOS LANMAN 2,1" ou "NT LM 0,12".</span><span class="sxs-lookup"><span data-stu-id="22a17-106">Each dialect is identified by a standard string such as "PC NETWORK PROGRAM 1.0", "MICROSOFT NETWORKS 3.0", "DOS LANMAN 2.1", or "NT LM 0.12".</span></span> <span data-ttu-id="22a17-107">A primeira cadeia de caracteres identifica o primeiro dialeto de SMB e a última cadeia de caracteres identifica CIFS, o primeiro dialeto do protocolo SMB da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="22a17-107">The first string identifies the first dialect of SMB, and the last string identifies CIFS, the first dialect of Microsoft SMB Protocol.</span></span>

<span data-ttu-id="22a17-108">A maioria dos clientes Windows dá suporte a pelo menos seis dialetos diferentes do protocolo SMB da Microsoft, portanto, uma das primeiras etapas para estabelecer uma conexão entre um cliente e um servidor usando o protocolo SMB da Microsoft é determinar o dialeto com o nível mais alto de funcionalidade que o cliente e o servidor têm suporte.</span><span class="sxs-lookup"><span data-stu-id="22a17-108">Most Windows clients support at least six different dialects of Microsoft SMB Protocol, so one of the first steps in establishing a connection between a client and a server using Microsoft SMB Protocol is to determine the dialect with the highest level of functionality that both the client and server support.</span></span> <span data-ttu-id="22a17-109">Esse processo é conhecido como "negociar o dialeto".</span><span class="sxs-lookup"><span data-stu-id="22a17-109">This process is known as "negotiating the dialect."</span></span> <span data-ttu-id="22a17-110">As cadeias de caracteres de dialeto mencionadas acima estão incluídas nos pacotes de solicitação de negociação de dialeto e resposta para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="22a17-110">The dialect strings mentioned above are included in the dialect negotiation request and response packets for this purpose.</span></span>

 

 



