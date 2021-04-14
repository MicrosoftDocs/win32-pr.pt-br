---
title: Controles de contêiner
description: Controles de contêiner
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453732"
---
# <a name="container-controls"></a><span data-ttu-id="8f05d-103">Controles de contêiner</span><span class="sxs-lookup"><span data-stu-id="8f05d-103">Container Controls</span></span>

<span data-ttu-id="8f05d-104">Conforme descrito acima, os controles de contêiner são controles ActiveX que contêm visualmente outros controles.</span><span class="sxs-lookup"><span data-stu-id="8f05d-104">As described above, container controls are ActiveX controls that visually contain other controls.</span></span> <span data-ttu-id="8f05d-105">A arquitetura de controles ActiveX especifica a interface [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para habilitar controles de contêiner.</span><span class="sxs-lookup"><span data-stu-id="8f05d-105">The ActiveX controls architecture specifies the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface to enable container controls.</span></span> <span data-ttu-id="8f05d-106">Os contêineres também podem dar suporte a controles de contêiner sem dar suporte a **ISimpleFrameSite**, embora o comportamento não possa ser garantido.</span><span class="sxs-lookup"><span data-stu-id="8f05d-106">Containers may also support container controls without supporting **ISimpleFrameSite**, although the behavior cannot be guaranteed.</span></span> <span data-ttu-id="8f05d-107">Por esse motivo, existe uma categoria de componente para controles SimpleFrameSite em que a funcionalidade completa dessa interface é necessária.</span><span class="sxs-lookup"><span data-stu-id="8f05d-107">For this reason, a component category exists for SimpleFrameSite controls where the full functionality of this interface is required.</span></span>

<span data-ttu-id="8f05d-108">Para dar suporte a controles de contêiner sem implementar [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), um contêiner de controle ActiveX deve:</span><span class="sxs-lookup"><span data-stu-id="8f05d-108">To support container controls without implementing [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), an ActiveX control container must:</span></span>

-   <span data-ttu-id="8f05d-109">Ative todos os controles em todos os momentos.</span><span class="sxs-lookup"><span data-stu-id="8f05d-109">Activate all controls at all times.</span></span>
-   <span data-ttu-id="8f05d-110">Reparente os controles contidos para o hWnd do controle que o contém.</span><span class="sxs-lookup"><span data-stu-id="8f05d-110">Reparent the contained controls to the hWnd of the containing control.</span></span>
-   <span data-ttu-id="8f05d-111">Permanecerá o pai do controle de contêiner.</span><span class="sxs-lookup"><span data-stu-id="8f05d-111">Remain the parent of the container control.</span></span>

 

 




