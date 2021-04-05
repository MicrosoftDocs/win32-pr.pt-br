---
description: Lidando com Ejetações de disco
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Lidando com Ejetações de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825472"
---
# <a name="handling-disc-ejections"></a><span data-ttu-id="41549-103">Lidando com Ejetações de disco</span><span class="sxs-lookup"><span data-stu-id="41549-103">Handling Disc Ejections</span></span>

<span data-ttu-id="41549-104">Quando o usuário ejeta um DVD da unidade, o navegador de DVD envia ao aplicativo uma \_ \_ mensagem ejetada no DVD do EC \_ .</span><span class="sxs-lookup"><span data-stu-id="41549-104">When the user ejects a DVD from the drive, the DVD Navigator sends your application an EC\_DVD\_DISC\_EJECTED message.</span></span> <span data-ttu-id="41549-105">O aplicativo pode ignorar essa mensagem com segurança e permitir que o navegador de DVD gerencie o estado do grafo.</span><span class="sxs-lookup"><span data-stu-id="41549-105">The application can safely ignore this message and let the DVD Navigator manage the graph's state.</span></span> <span data-ttu-id="41549-106">Um aplicativo também pode manipular o \_ \_ método ejetado do disco DVD EC \_ para implementar o comportamento personalizado quando um disco é ejetado.</span><span class="sxs-lookup"><span data-stu-id="41549-106">An application can also handle the EC\_DVD\_DISC\_EJECTED method to implement custom behavior when a disc is ejected.</span></span> <span data-ttu-id="41549-107">Se você tratar a mensagem, deverá definir o sinalizador DVD \_ ResetOnStop como **true** com o método [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e, em seguida, chamar [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) antes de fechar o aplicativo ou reproduzir outro disco.</span><span class="sxs-lookup"><span data-stu-id="41549-107">If you handle the message, you must set the DVD\_ResetOnStop flag to **TRUE** with the [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method and then call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) before closing the application or playing another disc.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41549-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41549-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41549-109">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="41549-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



