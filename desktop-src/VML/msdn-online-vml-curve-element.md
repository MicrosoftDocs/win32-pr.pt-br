---
title: Elemento de curva de VML
description: Elemento de curva de VML
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b9e04086652bf9dde7d7e7f5ebdea0992f774c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162316"
---
# <a name="vml-curve-element"></a><span data-ttu-id="2005c-103">Elemento de curva de VML</span><span class="sxs-lookup"><span data-stu-id="2005c-103">VML Curve Element</span></span>

<span data-ttu-id="2005c-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2005c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2005c-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="2005c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2005c-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="2005c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2005c-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="2005c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2005c-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2005c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2005c-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2005c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2005c-110">Forma de curva predefinida.</span><span class="sxs-lookup"><span data-stu-id="2005c-110">Predefined curve shape.</span></span>

<span data-ttu-id="2005c-111">A **curva** usa os atributos [para](to-attribute--curve--vml.md), [de](from-attribute--curve--vml.md), [Control1](msdn-online-vml-control1-attribute.md)e [Control2](msdn-online-vml-control2-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2005c-111">**Curve** uses the [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md), and [control2](msdn-online-vml-control2-attribute.md) attributes.</span></span>

<span data-ttu-id="2005c-112">Veja a seguir o código mínimo necessário para produzir uma imagem.</span><span class="sxs-lookup"><span data-stu-id="2005c-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 