---
title: Interfaces de vídeo Direct3D
description: Este tópico lista as interfaces de vídeo do Direct3D que estão disponíveis no Direct3D 9Ex e que têm suporte no Windows 7 e em versões posteriores dos sistemas operacionais cliente Windows e no Windows Server 2008 R2 e em versões posteriores dos sistemas operacionais Windows Server.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454119"
---
# <a name="direct3d-video-interfaces"></a><span data-ttu-id="5c6c2-103">Interfaces de vídeo Direct3D</span><span class="sxs-lookup"><span data-stu-id="5c6c2-103">Direct3D Video Interfaces</span></span>

<span data-ttu-id="5c6c2-104">Este tópico lista as interfaces de vídeo do Direct3D que estão disponíveis no Direct3D 9Ex e que têm suporte no Windows 7 e em versões posteriores dos sistemas operacionais cliente Windows e no Windows Server 2008 R2 e em versões posteriores dos sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5c6c2-104">This topic lists the Direct3D video interfaces that are available in Direct3D 9Ex and that are supported on Windows 7 and later versions of Windows client operating systems and on Windows Server 2008 R2 and later versions of Windows server operating systems.</span></span> <span data-ttu-id="5c6c2-105">Você pode usar essas interfaces e seus métodos para obter os recursos de proteção de conteúdo de vídeo do driver de gráficos e os recursos de hardware de sobreposição de um dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5c6c2-105">You can use these interfaces and their methods to obtain the video content protection capabilities of the graphics driver and the overlay hardware capabilities of a Direct3D device.</span></span> <span data-ttu-id="5c6c2-106">Você também pode usar essas interfaces e seus métodos para proteger o conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5c6c2-106">You can also use these interfaces and their methods to protect video content.</span></span> <span data-ttu-id="5c6c2-107">Essas interfaces e seus métodos são definidos em D3d9. h e descritos na seção [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .</span><span class="sxs-lookup"><span data-stu-id="5c6c2-107">These interfaces and their methods are defined in D3d9.h and described in the [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) section.</span></span>



| <span data-ttu-id="5c6c2-108">Interface</span><span class="sxs-lookup"><span data-stu-id="5c6c2-108">Interface</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="5c6c2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c6c2-109">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6c2-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span><span class="sxs-lookup"><span data-stu-id="5c6c2-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span></span><br/>           | <span data-ttu-id="5c6c2-111">Consulta a sobreposição de recursos de hardware de um dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5c6c2-111">Queries the overlay hardware capabilities of a Direct3D device.</span></span><br/>                                                     |
| <span data-ttu-id="5c6c2-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span><span class="sxs-lookup"><span data-stu-id="5c6c2-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span></span><br/> | <span data-ttu-id="5c6c2-113">Fornece um canal de comunicação com o driver de gráficos ou o tempo de execução do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5c6c2-113">Provides a communication channel with the graphics driver or the Direct3D runtime.</span></span><br/>                                  |
| <span data-ttu-id="5c6c2-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span><span class="sxs-lookup"><span data-stu-id="5c6c2-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span></span><br/>                                    | <span data-ttu-id="5c6c2-115">Representa uma sessão criptográfica que é usada para acessar uma superfície protegida.</span><span class="sxs-lookup"><span data-stu-id="5c6c2-115">Represents a cryptographic session that is used to access a protected surface.</span></span><br/>                                      |
| <span data-ttu-id="5c6c2-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span><span class="sxs-lookup"><span data-stu-id="5c6c2-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span></span><br/>                                              | <span data-ttu-id="5c6c2-117">Permite que um aplicativo use a proteção de conteúdo e os serviços de criptografia que são implementados por um driver de gráficos.</span><span class="sxs-lookup"><span data-stu-id="5c6c2-117">Enables an application to use content protection and encryption services that are implemented by a graphics driver.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5c6c2-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c6c2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c6c2-119">Efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="5c6c2-119">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="5c6c2-120">Guia de programação para Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5c6c2-120">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

