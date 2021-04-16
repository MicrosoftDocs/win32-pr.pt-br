---
description: Glossário de Monitor de Rede termos que começam com a letra F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 6e6b85cc-83bc-4468-b1cf-3480022a8f12
title: F (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605eb27b95526fa2f3839c06e6f259a2afec55c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779602"
---
# <a name="f-network-monitor"></a><span data-ttu-id="39884-103">F (Monitor de Rede)</span><span class="sxs-lookup"><span data-stu-id="39884-103">F (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="39884-104"><span id="_netmon_filter_blob_gly"></span><span id="_NETMON_FILTER_BLOB_GLY"></span>**BLOB de filtro**</span><span class="sxs-lookup"><span data-stu-id="39884-104"><span id="_netmon_filter_blob_gly"></span><span id="_NETMON_FILTER_BLOB_GLY"></span>**filter BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="39884-105">BLOB (objeto binário grande) usado para restringir a pesquisa de uma NIC (placa de interface de rede).</span><span class="sxs-lookup"><span data-stu-id="39884-105">Binary large object (BLOB) used to restrict the search for a network interface card (NIC).</span></span> <span data-ttu-id="39884-106">Cada entrada no BLOB de filtro deve corresponder a uma entrada equivalente no BLOB do NPP (provedor de pacotes de rede) que representa a NIC.</span><span class="sxs-lookup"><span data-stu-id="39884-106">Each entry in the filter BLOB must match an equivalent entry in the network packet provider (NPP) BLOB that represents the NIC.</span></span> <span data-ttu-id="39884-107">Por exemplo, um aplicativo pode solicitar somente placas Ethernet ou cartões que dão suporte a uma taxa de quadros específica.</span><span class="sxs-lookup"><span data-stu-id="39884-107">For example, an application can request only Ethernet cards, or cards that support a specific frame rate.</span></span> <span data-ttu-id="39884-108">Você pode usar um BLOB de filtro para chamar as funções **GetNPPBlobFromUI** e **GetNPPBlobTable** .</span><span class="sxs-lookup"><span data-stu-id="39884-108">You can use a filter BLOB to call the **GetNPPBlobFromUI** and **GetNPPBlobTable** functions.</span></span>

</dd> <dt>

<span data-ttu-id="39884-109"><span id="_netmon_follow_set_gly"></span><span id="_NETMON_FOLLOW_SET_GLY"></span>**Siga o conjunto**</span><span class="sxs-lookup"><span data-stu-id="39884-109"><span id="_netmon_follow_set_gly"></span><span id="_NETMON_FOLLOW_SET_GLY"></span>**follow set**</span></span>
</dt> <dd>

<span data-ttu-id="39884-110">Um conjunto de protocolos que segue um protocolo.</span><span class="sxs-lookup"><span data-stu-id="39884-110">A protocol set that follows a protocol.</span></span> <span data-ttu-id="39884-111">Monitor de Rede usará o seguinte conjunto de um protocolo se o analisador não puder detectar o próximo protocolo dos dados na captura.</span><span class="sxs-lookup"><span data-stu-id="39884-111">Network Monitor uses the follow set of a protocol if the parser cannot detect the next protocol from the data in the capture.</span></span> <span data-ttu-id="39884-112">Confira também [ *conjunto de entrega*](h.md)</span><span class="sxs-lookup"><span data-stu-id="39884-112">See also [*handoff set*](h.md)</span></span>

</dd> <dt>

<span data-ttu-id="39884-113"><span id="_netmon_frame_gly"></span><span id="_NETMON_FRAME_GLY"></span>**quadro**</span><span class="sxs-lookup"><span data-stu-id="39884-113"><span id="_netmon_frame_gly"></span><span id="_NETMON_FRAME_GLY"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="39884-114">Um pacote de dados que é transmitido como uma unidade em uma rede.</span><span class="sxs-lookup"><span data-stu-id="39884-114">A packet of data that is transmitted as one unit over a network.</span></span> <span data-ttu-id="39884-115">Cada quadro segue a mesma organização básica e contém informações de controle, como sincronização de caracteres, endereços de estações, um valor de verificação de erros e uma quantidade variável de dados.</span><span class="sxs-lookup"><span data-stu-id="39884-115">Each frame follows the same basic organization, and contains control information such as synchronizing characters, station addresses, an error-checking value, and a variable amount of data.</span></span> <span data-ttu-id="39884-116">Também chamado de pacote.</span><span class="sxs-lookup"><span data-stu-id="39884-116">Also called a packet.</span></span>

</dd> <dt>

<span data-ttu-id="39884-117"><span id="_netmon_frame_viewer_window_gly"></span><span id="_NETMON_FRAME_VIEWER_WINDOW_GLY"></span>**janela Visualizador de quadros**</span><span class="sxs-lookup"><span data-stu-id="39884-117"><span id="_netmon_frame_viewer_window_gly"></span><span id="_NETMON_FRAME_VIEWER_WINDOW_GLY"></span>**frame viewer window**</span></span>
</dt> <dd>

<span data-ttu-id="39884-118">Uma janela Monitor de Rede que exibe informações detalhadas sobre quadros individuais.</span><span class="sxs-lookup"><span data-stu-id="39884-118">A Network Monitor window that displays detailed information about individual frames.</span></span> <span data-ttu-id="39884-119">Você pode abrir várias janelas do Visualizador de quadros ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="39884-119">You can open several frame viewer windows at one time.</span></span>

</dd> </dl>

 

 



