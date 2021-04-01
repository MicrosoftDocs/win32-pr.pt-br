---
description: A figura a seguir mostra a relação entre os aplicativos de especialista e analisador e outros componentes da arquitetura de Monitor de Rede.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Arquitetura de expert e parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089977"
---
# <a name="expert-and-parser-architecture"></a><span data-ttu-id="6b3aa-103">Arquitetura de expert e parser</span><span class="sxs-lookup"><span data-stu-id="6b3aa-103">Expert and Parser Architecture</span></span>

<span data-ttu-id="6b3aa-104">A figura a seguir mostra a relação entre os aplicativos de [especialista](experts.md) e [analisador](parsers.md) e outros componentes da arquitetura de monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-104">The following figure shows the relationship between [expert](experts.md) and [parser](parsers.md) applications and other components of the Network Monitor architecture.</span></span>

![a relação entre aplicativos de especialista e analisador](images/nm-arch1.png)

<span data-ttu-id="6b3aa-106">O tráfego de rede é coletado, como quadros individuais, do driver NDIS.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-106">The network traffic is collected, as individual frames, from the NDIS driver.</span></span> <span data-ttu-id="6b3aa-107">O driver de Monitor de Rede (Nmnt.sys), em seguida, roteia os quadros para um NPP (provedor de pacotes de rede), que captura os dados e os coloca em um ou mais arquivos de captura.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which captures the data and places it in one or more capture files.</span></span> <span data-ttu-id="6b3aa-108">O NPP é uma coleção de interfaces COM usadas para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="6b3aa-109">Nesse caso, a interface [**IDelaydC**](idelaydc.md) é usada para executar uma captura atrasada.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-109">In this case, the [**IDelaydC**](idelaydc.md) interface is used to perform a delayed capture.</span></span>

> [!Note]  
> <span data-ttu-id="6b3aa-110">O NPP é usado para capturas atrasadas e em tempo real.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="6b3aa-111">Para capturas em tempo real, a interface [**IRTC**](irtc.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-111">For real-time captures, the [**IRTC**](irtc.md) interface is used.</span></span>

 

<span data-ttu-id="6b3aa-112">Quando os quadros de rede são armazenados no arquivo de captura e o arquivo é acessível, os especialistas e analisadores podem usar a interface do usuário do Monitor de Rede e as funções Monitor de Rede fornecidas no Nmapi.dll para analisar os dados.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-112">When the network frames are stored in the capture file and the file is accessible, experts and parsers can use the Network Monitor UI and the Network Monitor functions provided in Nmapi.dll to analyze the data.</span></span> <span data-ttu-id="6b3aa-113">Os arquivos de captura não estarão acessíveis até que a captura seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-113">Capture files are not accessible until the capture is complete.</span></span>

 

 



