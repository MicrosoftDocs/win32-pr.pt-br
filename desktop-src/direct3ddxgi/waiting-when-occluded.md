---
description: Os aplicativos podem esperar um evento quando a renderização na tela é desnecessária (ou seja, enquanto eles são obstruído).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Aguardando um evento quando a renderização é desnecessária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789529"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a><span data-ttu-id="3f147-103">Aguardando um evento quando a renderização é desnecessária</span><span class="sxs-lookup"><span data-stu-id="3f147-103">Waiting on an event when rendering is unnecessary</span></span>

<span data-ttu-id="3f147-104">Os aplicativos podem esperar um evento quando a renderização na tela é desnecessária (ou seja, enquanto eles são obstruído).</span><span class="sxs-lookup"><span data-stu-id="3f147-104">Apps can wait on an event when rendering to the screen is unnecessary (that is, while they are occluded).</span></span> <span data-ttu-id="3f147-105">Quando o Gerenciador de Janelas da Área de Trabalho (DWM) ou um aplicativo é obstruídodo, nenhuma renderização é necessária e o sistema operacional pode permanecer em Estados de energia menores por períodos mais longos.</span><span class="sxs-lookup"><span data-stu-id="3f147-105">When the Desktop Window Manager (DWM) or an app is occluded, no rendering is necessary and the operating system can stay in lower power states for longer periods of time.</span></span> <span data-ttu-id="3f147-106">Isso economiza energia e estende a vida útil da bateria.</span><span class="sxs-lookup"><span data-stu-id="3f147-106">This saves power and extends battery life.</span></span>

<span data-ttu-id="3f147-107">Um aplicativo pode aguardar um evento quando:</span><span class="sxs-lookup"><span data-stu-id="3f147-107">An app can wait on an event when:</span></span>

-   <span data-ttu-id="3f147-108">Todos os monitores estão desligados.</span><span class="sxs-lookup"><span data-stu-id="3f147-108">All the monitors are off.</span></span>
-   <span data-ttu-id="3f147-109">A sessão em que o aplicativo é executado está desconectada.</span><span class="sxs-lookup"><span data-stu-id="3f147-109">The session that the app runs in is disconnected.</span></span>
-   <span data-ttu-id="3f147-110">O aplicativo é executado em tela inteira exclusivamente em uma única configuração de monitor.</span><span class="sxs-lookup"><span data-stu-id="3f147-110">The app runs in full screen exclusively on a single monitor configuration.</span></span>
-   <span data-ttu-id="3f147-111">O aplicativo é executado em uma área de trabalho diferente da área de trabalho ativa e não tem permissão para renderizar no desktop ativo.</span><span class="sxs-lookup"><span data-stu-id="3f147-111">The app runs on a different desktop than the active desktop and does not have permission to render on the active desktop.</span></span>

<span data-ttu-id="3f147-112">O sistema operacional dispara o evento quando o aplicativo é capaz de renderizar novamente.</span><span class="sxs-lookup"><span data-stu-id="3f147-112">The operating system triggers the event when the app is able to render again.</span></span> <span data-ttu-id="3f147-113">O evento não é removido durante uma atualização de driver ou um processo de TDR (detecção de tempo limite e recuperação), no entanto, ele é limpo quando o novo adaptador e os monitores se tornam ativos.</span><span class="sxs-lookup"><span data-stu-id="3f147-113">The event is not cleared during a driver upgrade, or timeout detection and recovery (TDR) procession, however it is cleared when the new adapter and monitors become active.</span></span>

<span data-ttu-id="3f147-114">Se você quiser que seu aplicativo seja notificado sobre alterações de status do oclusão, o aplicativo deverá se registrar para essas alterações.</span><span class="sxs-lookup"><span data-stu-id="3f147-114">If you want your app to be notified about changes of occlusion status, the app must register for these changes.</span></span> <span data-ttu-id="3f147-115">Um aplicativo pode ser registrado para ser notificado sobre alterações de status de oclusão por meio de uma mensagem em uma janela ou por meio de sinalização de evento.</span><span class="sxs-lookup"><span data-stu-id="3f147-115">An app can register to be notified about changes of occlusion status through a message to a window or through event signaling.</span></span> <span data-ttu-id="3f147-116">Para se registrar para receber mensagens de notificação em uma janela sobre alterações de status de oclusão, um aplicativo chama o método [**IDXGIFactory2:: RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) .</span><span class="sxs-lookup"><span data-stu-id="3f147-116">To register to receive notification messages to a window about occlusion status changes, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) method.</span></span> <span data-ttu-id="3f147-117">Para se registrar para receber a notificação de alterações de status de oclusão por meio de sinalização de evento, um aplicativo chama o método [**IDXGIFactory2:: RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) .</span><span class="sxs-lookup"><span data-stu-id="3f147-117">To register to receive notification of occlusion status changes via event signaling, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) method.</span></span> <span data-ttu-id="3f147-118">Os dois métodos retornam um ponteiro para um valor de chave que o aplicativo pode usar para cancelar o registro da notificação.</span><span class="sxs-lookup"><span data-stu-id="3f147-118">Both methods return a pointer to a key value that the app can use to unregister the notification.</span></span> <span data-ttu-id="3f147-119">Para cancelar o registro da notificação, o aplicativo passa esse valor de chave para o método [**IDXGIFactory2:: UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3f147-119">To unregister the notification, the app passes this key value to the [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f147-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f147-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f147-121">Aprimoramentos de DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="3f147-121">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



