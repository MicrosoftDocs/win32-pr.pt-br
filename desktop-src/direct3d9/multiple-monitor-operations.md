---
description: 'Quando um dispositivo é redefinido com êxito (IDirect3DDevice9:: Reset) ou criado (IDirect3D9:: CreateDevice) em operações de tela inteira, o objeto do Direct3D que criou o dispositivo é marcado como proprietário de todos os adaptadores nesse sistema.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Operações de Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105762477"
---
# <a name="multiple-monitor-operations-direct3d-9"></a><span data-ttu-id="67a18-103">Operações de Multiple-Monitor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="67a18-103">Multiple-Monitor Operations (Direct3D 9)</span></span>

<span data-ttu-id="67a18-104">Quando um dispositivo é redefinido com êxito ([**IDirect3DDevice9:: Reset**](/windows/desktop/api)) ou criado ([**IDirect3D9:: CreateDevice**](/windows/desktop/api)) em operações de tela inteira, o objeto do Direct3D que criou o dispositivo é marcado como proprietário de todos os adaptadores nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="67a18-104">When a device is successfully reset ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) or created ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) in full-screen operations, the Direct3D object that created the device is marked as owning all adapters on that system.</span></span> <span data-ttu-id="67a18-105">Esse estado é conhecido como modo exclusivo e o objeto Direct3D possui modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="67a18-105">This state is known as exclusive mode, and the Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="67a18-106">Modo exclusivo significa que os dispositivos criados por qualquer outro objeto do Direct3D não podem assumir operações de tela inteira nem alocar memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="67a18-106">Exclusive mode means that devices created by any other Direct3D object can neither assume full-screen operations nor allocate video memory.</span></span> <span data-ttu-id="67a18-107">Além disso, quando um objeto do Direct3D assume um modo exclusivo, todos os dispositivos diferentes daquele que foi colocado em tela inteira são colocados no estado perdido.</span><span class="sxs-lookup"><span data-stu-id="67a18-107">In addition, when a Direct3D object assumes exclusive mode, all devices other than the one that went full-screen are placed in lost state.</span></span> <span data-ttu-id="67a18-108">Para obter detalhes, consulte [dispositivos perdidos (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="67a18-108">For details, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="67a18-109">Juntamente com o modo exclusivo, o objeto do Direct3D é informado da janela de foco que o dispositivo usará.</span><span class="sxs-lookup"><span data-stu-id="67a18-109">Along with exclusive mode, the Direct3D object is informed of the focus window that the device will use.</span></span> <span data-ttu-id="67a18-110">O modo exclusivo é liberado quando o dispositivo de tela inteira final de Propriedade do objeto do Direct3D é redefinido para o modo de janela ou destruído.</span><span class="sxs-lookup"><span data-stu-id="67a18-110">Exclusive mode is released when the final full-screen device owned by that Direct3D object is either reset to windowed mode or destroyed.</span></span>

<span data-ttu-id="67a18-111">Os dispositivos podem ser divididos em duas categorias quando um objeto do Direct3D possui um modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="67a18-111">Devices can be divided into two categories when a Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="67a18-112">A primeira categoria de dispositivos tem as seguintes características.</span><span class="sxs-lookup"><span data-stu-id="67a18-112">The first category of devices have the following characteristics.</span></span>

-   <span data-ttu-id="67a18-113">Eles são criados pelo mesmo objeto do Direct3D que criou o dispositivo que está em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="67a18-113">They are created by the same Direct3D object that created the device that is full-screen.</span></span>
-   <span data-ttu-id="67a18-114">Eles têm a mesma janela de foco que o dispositivo que está em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="67a18-114">They have the same focus window as the device that is full-screen.</span></span>
-   <span data-ttu-id="67a18-115">Eles representam um adaptador diferente de qualquer dispositivo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="67a18-115">They represent a different adapter from any full-screen device.</span></span>

<span data-ttu-id="67a18-116">Os dispositivos nessa categoria não têm restrições sobre sua capacidade de redefinição ou criação, e eles não são colocados no estado perdido.</span><span class="sxs-lookup"><span data-stu-id="67a18-116">Devices in this category have no restrictions concerning their ability to be reset or created, and they are not placed in lost state.</span></span> <span data-ttu-id="67a18-117">Os dispositivos nessa categoria podem até mesmo ser colocados no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="67a18-117">Devices in this category can even be put into full-screen mode.</span></span>

<span data-ttu-id="67a18-118">Dispositivos que não estão na primeira categoria – dispositivos criados por outro objeto do Direct3D, criados com uma janela de foco diferente e criados para um adaptador com um dispositivo que já está em tela inteira-não podem ser redefinidos e permanecer no estado perdido até que o modo exclusivo seja perdido.</span><span class="sxs-lookup"><span data-stu-id="67a18-118">Devices that do not fall in the first category - devices created by another Direct3D object, created with a different focus window, and created for an adapter with a device that is already full-screen - cannot be reset and remain in lost state until the exclusive mode is lost.</span></span> <span data-ttu-id="67a18-119">Como resultado, um aplicativo de vários monitores pode posicionar vários dispositivos no modo de tela inteira, mas somente se todos esses dispositivos forem para adaptadores diferentes, foram criados pelo mesmo objeto do Direct3D e compartilham a mesma janela de foco.</span><span class="sxs-lookup"><span data-stu-id="67a18-119">As a result, a multiple-monitor application can place several devices in full-screen mode, but only if all these devices are for different adapters, were created by the same Direct3D object, and share the same focus window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67a18-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67a18-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a18-121">Apresentando uma cena</span><span class="sxs-lookup"><span data-stu-id="67a18-121">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 



