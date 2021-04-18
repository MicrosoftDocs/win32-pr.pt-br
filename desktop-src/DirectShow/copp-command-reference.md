---
description: Referência de comando COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Referência de comando COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778494"
---
# <a name="copp-command-reference"></a><span data-ttu-id="fde48-103">Referência de comando COPP</span><span class="sxs-lookup"><span data-stu-id="fde48-103">COPP Command Reference</span></span>

<span data-ttu-id="fde48-104">Esta seção descreve os comandos de COPP (protocolo de proteção de saída) certificados.</span><span class="sxs-lookup"><span data-stu-id="fde48-104">This section describes the Certified Output Protection Protocol (COPP) commands.</span></span> <span data-ttu-id="fde48-105">Os comandos a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="fde48-105">The following commands are defined.</span></span>



| <span data-ttu-id="fde48-106">Comando</span><span class="sxs-lookup"><span data-stu-id="fde48-106">Command</span></span>              | <span data-ttu-id="fde48-107">GUID</span><span class="sxs-lookup"><span data-stu-id="fde48-107">GUID</span></span>                             |
|----------------------|----------------------------------|
| <span data-ttu-id="fde48-108">Definir nível de proteção</span><span class="sxs-lookup"><span data-stu-id="fde48-108">Set Protection Level</span></span> | <span data-ttu-id="fde48-109">**COPPSetProtectionLevel de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="fde48-109">**DXVA\_COPPSetProtectionLevel**</span></span> |
| <span data-ttu-id="fde48-110">Definir sinalização</span><span class="sxs-lookup"><span data-stu-id="fde48-110">Set Signaling</span></span>        | <span data-ttu-id="fde48-111">**COPPSetSignaling de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="fde48-111">**DXVA\_COPPSetSignaling**</span></span>       |



 

<span data-ttu-id="fde48-112">Comando definir nível de proteção</span><span class="sxs-lookup"><span data-stu-id="fde48-112">Set Protection Level Command</span></span>

<span data-ttu-id="fde48-113">Define o nível de proteção para um mecanismo de proteção de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="fde48-113">Sets the protection level for a specified output protection mechanism.</span></span> <span data-ttu-id="fde48-114">Dependendo do conector, pode ser possível aplicar mais de um mecanismo de proteção no mesmo conector, com configurações diferentes para cada mecanismo.</span><span class="sxs-lookup"><span data-stu-id="fde48-114">Depending on the connector, it might be possible to apply more than one protection mechanism on the same connector, with different settings for each mechanism.</span></span>

<span data-ttu-id="fde48-115">**GUID**: DXVA \_ COPPSetProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="fde48-115">**GUID**: DXVA\_COPPSetProtectionLevel</span></span>

<span data-ttu-id="fde48-116">**Dados de entrada**: uma estrutura de [**DXVA \_ COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .</span><span class="sxs-lookup"><span data-stu-id="fde48-116">**Input data**: A [**DXVA\_COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) structure.</span></span>

<span data-ttu-id="fde48-117">Definir comando de sinalização</span><span class="sxs-lookup"><span data-stu-id="fde48-117">Set Signaling Command</span></span>

<span data-ttu-id="fde48-118">Especifica informações sobre o sinal de vídeo diferente do nível de proteção.</span><span class="sxs-lookup"><span data-stu-id="fde48-118">Specifies information about the video signal other than the protection level.</span></span>

<span data-ttu-id="fde48-119">Para o CGMS-A, determinados padrões de proteção exigem que o sinal televsion contenha informações sobre a taxa de proporção e outras informações nos mesmos pacotes VBI de forma de onda que os bits CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="fde48-119">For CGMS-A, certain protection standards require that the televsion signal contains information about the aspect ratio and other information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="fde48-120">As televisões podem exibir inadequadamente se as informações de taxa de proporção não estiverem consistentes com o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fde48-120">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="fde48-121">O aplicativo pode usar esse comando para especificar a taxa de proporção para que o driver de gráficos possa gerar os pacotes VBI corretos.</span><span class="sxs-lookup"><span data-stu-id="fde48-121">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

<span data-ttu-id="fde48-122">Esse comando também é projetado para ser extensível se forem necessárias informações de sinal adicionais em padrões futuros.</span><span class="sxs-lookup"><span data-stu-id="fde48-122">This command is also designed to be extensible if additional signal information is required in future standards.</span></span>

<span data-ttu-id="fde48-123">**GUID**: DXVA \_ COPPSetSignaling</span><span class="sxs-lookup"><span data-stu-id="fde48-123">**GUID**: DXVA\_COPPSetSignaling</span></span>

<span data-ttu-id="fde48-124">**Dados de entrada**: uma estrutura de [**DXVA \_ COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="fde48-124">**Input data**: A [**DXVA\_COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fde48-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fde48-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fde48-126">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="fde48-126">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



