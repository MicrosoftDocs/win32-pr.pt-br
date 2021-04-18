---
title: Repositórios online exclusivos
description: Repositórios online exclusivos
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Armazenamentos online do Windows Media Player, exclusivo
- lojas online, exclusivo
- tipos 1 lojas online, exclusivo
- tipo 2 lojas online, exclusivo
- repositórios online exclusivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105813162"
---
# <a name="exclusive-online-stores"></a><span data-ttu-id="d511e-108">Repositórios online exclusivos</span><span class="sxs-lookup"><span data-stu-id="d511e-108">Exclusive Online Stores</span></span>

<span data-ttu-id="d511e-109">Com o Windows Media Player 11, um aplicativo que incorpora o controle Player remotamente pode especificar um repositório online exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d511e-109">With Windows Media Player 11, an application that embeds the Player control remotely can specify an exclusive online store.</span></span> <span data-ttu-id="d511e-110">Nesse caso, o seletor de serviço no Windows Media Player é desabilitado e apenas o repositório online especificado está disponível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="d511e-110">In that case, the service selector in Windows Media Player is disabled, and only the specified online store is available to the user.</span></span> <span data-ttu-id="d511e-111">Além disso, o Windows Media Player adota a cor especificada pelo elemento **Color** do documento de informações do repositório online exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d511e-111">Also, Windows Media Player adopts the color specified by the **Color** element of the exclusive online store's ServiceInfo document.</span></span>

<span data-ttu-id="d511e-112">Para especificar um repositório online exclusivo, um aplicativo deve acrescentar ExclusiveService:*KeyName* ao final da cadeia de caracteres que ele retorna de [IWMPRemoteMediaServices:: getservicetype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span><span class="sxs-lookup"><span data-stu-id="d511e-112">To specify an exclusive online store, an application must append ExclusiveService:*keyname* to the end of the string that it returns from [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span></span> <span data-ttu-id="d511e-113">Por exemplo, suponha que o Proseware seja o nome da chave fornecida para uma loja online específica.</span><span class="sxs-lookup"><span data-stu-id="d511e-113">For example, suppose Proseware is the key name given to a particular online store.</span></span> <span data-ttu-id="d511e-114">Se **Getservicetype** retornar a cadeia de caracteres "Remote ExclusiveService: Proseware", o Proseware será a única loja online disponível no controle player incorporado remotamente.</span><span class="sxs-lookup"><span data-stu-id="d511e-114">If **GetServiceType** returns the string "Remote ExclusiveService:Proseware", then Proseware will be the only online store available in the remotely embedded Player control.</span></span>

<span data-ttu-id="d511e-115">Um aplicativo pode limitar o Windows Media Player a um repositório online exclusivo somente se o Windows Media Player ainda não estiver em execução quando o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="d511e-115">An application can limit Windows Media Player to an exclusive online store only if Windows Media Player is not already running when the application is launched.</span></span> <span data-ttu-id="d511e-116">É responsabilidade do aplicativo informar ao usuário que ele deve fechar o Windows Media Player antes de executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d511e-116">It is the application's responsibility to inform the user that he or she must close Windows Media Player before running the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d511e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d511e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d511e-118">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="d511e-118">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d511e-119">**Estabelecer comunicação remota do controle do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="d511e-119">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




