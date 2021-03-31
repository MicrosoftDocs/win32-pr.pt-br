---
description: Os NPPs (provedores de pacotes de rede) expõem as interfaces IDelaydC, IESP, IRTC e IStats.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Selecionando uma interface NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827859"
---
# <a name="selecting-an-npp-interface"></a><span data-ttu-id="06936-103">Selecionando uma interface NPP</span><span class="sxs-lookup"><span data-stu-id="06936-103">Selecting an NPP Interface</span></span>

<span data-ttu-id="06936-104">Os NPPs (provedores de pacotes de rede) expõem as interfaces [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md)e [**IStats**](istats.md) .</span><span class="sxs-lookup"><span data-stu-id="06936-104">Network packet providers (NPPs) expose the [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md), and [**IStats**](istats.md) interfaces.</span></span> <span data-ttu-id="06936-105">Cada uma dessas interfaces fornece métodos semelhantes para conectar o NPP à rede, capturar o tráfego de rede e coletar informações estatísticas sobre os dados capturados.</span><span class="sxs-lookup"><span data-stu-id="06936-105">Each of these interfaces provides similar methods for connecting the NPP to the network, capturing network traffic, and collecting statistical information about the captured data.</span></span> <span data-ttu-id="06936-106">Para escolher a interface a ser usada, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="06936-106">To choose which interface to use, refer to the following table.</span></span>

> [!Note]  
> <span data-ttu-id="06936-107">Ao conectar um NPP à rede com uma dessas interfaces, você só pode usar os métodos fornecidos por essa interface.</span><span class="sxs-lookup"><span data-stu-id="06936-107">When you connect an NPP to the network with one of these interfaces, you can only use the methods provided by that interface.</span></span> <span data-ttu-id="06936-108">Por exemplo, se você se conectar à rede usando a interface [**IRTC**](irtc.md) e, em seguida, tentar iniciar uma captura com [**IDelaydC**](idelaydc.md), sua chamada para iniciar a captura falhará e um código de erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="06936-108">For example, if you connect to the network using the [**IRTC**](irtc.md) interface and then try to start a capture with [**IDelaydC**](idelaydc.md), your call to start the capture will fail, and an error code will be returned.</span></span>

 



| <span data-ttu-id="06936-109">Interface</span><span class="sxs-lookup"><span data-stu-id="06936-109">Interface</span></span>                    | <span data-ttu-id="06936-110">Quando usar</span><span class="sxs-lookup"><span data-stu-id="06936-110">When to use</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06936-111">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="06936-111">**IDelaydC**</span></span>](idelaydc.md) | <span data-ttu-id="06936-112">Use para capturar o tráfego de rede e armazená-lo em um arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="06936-112">Use to capture network traffic and store it in a capture file.</span></span> <span data-ttu-id="06936-113">Essa interface é usada pela interface do usuário do Monitor de Rede e outros aplicativos NPP, que exigem o armazenamento de informações de rede capturadas.</span><span class="sxs-lookup"><span data-stu-id="06936-113">This interface is used by the Network Monitor UI and other NPP applications, which require storing captured network information.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="06936-114">**IESP**</span><span class="sxs-lookup"><span data-stu-id="06936-114">**IESP**</span></span>](iesp.md)         | <span data-ttu-id="06936-115">Usado para fornecer estatísticas aprimoradas em um formato de arquivo ESP especial.</span><span class="sxs-lookup"><span data-stu-id="06936-115">Used to provide enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="06936-116">Essa interface é usada por aplicativos NPP que exigem as estatísticas aprimoradas fornecidas pelo formato ESP.</span><span class="sxs-lookup"><span data-stu-id="06936-116">This interface is used by NPP applications that require the enhanced statistics provided by the ESP format.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="06936-117">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="06936-117">**IRTC**</span></span>](irtc.md)         | <span data-ttu-id="06936-118">Use para capturar o tráfego de rede em tempo real e disparar eventos quando eles ocorrerem.</span><span class="sxs-lookup"><span data-stu-id="06936-118">Use to capture real-time network traffic and to trigger events when they occur.</span></span> <span data-ttu-id="06936-119">Essa interface é usada por aplicativos NPP que exigem capturas em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="06936-119">This interface is used by NPP applications that require run-time captures.</span></span> <span data-ttu-id="06936-120">Observe que essa interface não fornece as estatísticas que as outras interfaces NPP fornecem, nem permite que você insira quadros no tráfego de rede capturado.</span><span class="sxs-lookup"><span data-stu-id="06936-120">Note that this interface does not provide the statistics that the other NPP interfaces provide, nor does it allow you to insert frames into the captured network traffic.</span></span><br/> |
| [<span data-ttu-id="06936-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="06936-121">**IStats**</span></span>](istats.md)     | <span data-ttu-id="06936-122">Use para recuperar estatísticas de captura, mas não os quadros capturados.</span><span class="sxs-lookup"><span data-stu-id="06936-122">Use to retrieve capture statistics but not the captured frames.</span></span>                                                                                                                                                                                                                                                                                 |



 

 

 




