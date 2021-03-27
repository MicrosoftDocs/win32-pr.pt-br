---
description: Este tópico fornece informações sobre considerações de segurança relacionadas ao GDI. Este tópico não fornece tudo o que você precisa saber sobre problemas de segurança. Em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Considerações de segurança: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922176"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="20289-105">Considerações de segurança: GDI</span><span class="sxs-lookup"><span data-stu-id="20289-105">Security Considerations: GDI</span></span>

<span data-ttu-id="20289-106">Este tópico fornece informações sobre considerações de segurança relacionadas ao GDI.</span><span class="sxs-lookup"><span data-stu-id="20289-106">This topic provides information about security considerations related to GDI.</span></span> <span data-ttu-id="20289-107">Este tópico não fornece tudo o que você precisa saber sobre problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="20289-107">This topic does not provide all you need to know about security issues.</span></span> <span data-ttu-id="20289-108">Em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.</span><span class="sxs-lookup"><span data-stu-id="20289-108">Instead, use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="20289-109">A GDI geralmente tem poucas preocupações com a segurança porque lida com exibição em vez de entrada.</span><span class="sxs-lookup"><span data-stu-id="20289-109">GDI generally has few security concerns because it deals with display rather than input.</span></span> <span data-ttu-id="20289-110">No entanto, aqui estão alguns problemas que você deve considerar.</span><span class="sxs-lookup"><span data-stu-id="20289-110">However, here are a few issues that you should consider.</span></span>

<span data-ttu-id="20289-111">Os bitmaps, os metaarquivos e as fontes são estruturas complexas que podem se tornar corrompidas.</span><span class="sxs-lookup"><span data-stu-id="20289-111">Bitmaps, metafiles, and fonts are complex structures that could become corrupted.</span></span> <span data-ttu-id="20289-112">É uma boa prática tentar garantir que esses itens sejam corrompidos e de uma fonte confiável.</span><span class="sxs-lookup"><span data-stu-id="20289-112">It is good practice to try to ensure that these items are uncorrupted and from a trustworthy source.</span></span>

<span data-ttu-id="20289-113">Um aplicativo pode especificar o descritor de segurança para algumas das APIs de impressão e spool.</span><span class="sxs-lookup"><span data-stu-id="20289-113">An application can specify the security descriptor for some of the printing and spooling APIs.</span></span> <span data-ttu-id="20289-114">Você deve tomar cuidado ao definir o descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="20289-114">You should take care when setting the security descriptor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20289-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20289-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20289-116">Central de segurança da Microsoft</span><span class="sxs-lookup"><span data-stu-id="20289-116">Microsoft Security Central</span></span>](https://www.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="20289-117">Centro de desenvolvedores de segurança</span><span class="sxs-lookup"><span data-stu-id="20289-117">Security Developer Center</span></span>](https://technet.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="20289-118">TechCenter de segurança</span><span class="sxs-lookup"><span data-stu-id="20289-118">Security TechCenter</span></span>](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



