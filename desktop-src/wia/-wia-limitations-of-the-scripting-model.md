---
description: 'Saiba mais sobre: limitações do modelo de script'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitações do modelo de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757450"
---
# <a name="limitations-of-the-scripting-model"></a><span data-ttu-id="bae18-103">Limitações do modelo de script</span><span class="sxs-lookup"><span data-stu-id="bae18-103">Limitations of the Scripting Model</span></span>

> [!Note]  
> <span data-ttu-id="bae18-104">Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="bae18-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="bae18-105">Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="bae18-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="bae18-106">O modelo de script da aquisição de imagens do Windows (WIA) expõe um subconjunto da funcionalidade WIA.</span><span class="sxs-lookup"><span data-stu-id="bae18-106">The Windows Image Acquisition (WIA) scripting model exposes a subset of WIA functionality.</span></span> <span data-ttu-id="bae18-107">A tabela a seguir fornece descrições das limitações do modelo de script.</span><span class="sxs-lookup"><span data-stu-id="bae18-107">The following table provides descriptions of the limitations of the scripting model.</span></span> 

| <span data-ttu-id="bae18-108">Funcionalidade WIA</span><span class="sxs-lookup"><span data-stu-id="bae18-108">WIA Functionality</span></span>               | <span data-ttu-id="bae18-109">Limitação de modelo de script</span><span class="sxs-lookup"><span data-stu-id="bae18-109">Scripting Model Limitation</span></span>                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae18-110">Suprimindo a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="bae18-110">Suppressing the user interface</span></span>  | <span data-ttu-id="bae18-111">Não é possível suprimir a interface do usuário para definir propriedades de dispositivo/transferência.</span><span class="sxs-lookup"><span data-stu-id="bae18-111">Cannot suppress the user interface for setting device/transfer properties.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="bae18-112">Definir propriedades</span><span class="sxs-lookup"><span data-stu-id="bae18-112">Setting properties</span></span>              | <span data-ttu-id="bae18-113">Não é possível definir (gravar) nenhuma propriedade de dispositivo ou item.</span><span class="sxs-lookup"><span data-stu-id="bae18-113">Cannot set (write) any device or item properties.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="bae18-114">Registrando para eventos de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="bae18-114">Registering for callback events</span></span> | <span data-ttu-id="bae18-115">Só pode receber notificação para três eventos especificados: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)e [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="bae18-115">Can only receive notification for three specified events: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md), and [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span></span> |
| <span data-ttu-id="bae18-116">Tratando erros</span><span class="sxs-lookup"><span data-stu-id="bae18-116">Handling errors</span></span>                 | <span data-ttu-id="bae18-117">Não é possível manipular erros WIA.</span><span class="sxs-lookup"><span data-stu-id="bae18-117">Cannot handle WIA errors.</span></span>                                                                                                                                                                                                                                                |



 

 

 
