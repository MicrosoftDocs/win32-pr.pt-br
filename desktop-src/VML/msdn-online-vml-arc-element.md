---
title: Elemento de arco da VML
description: Elemento de arco da VML
ms.assetid: 46b5b78a-9a69-432b-9008-0ce7a658b9dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd35d59349e10f38495807ceb3f08dc254c117e2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294447"
---
# <a name="vml-arc-element"></a><span data-ttu-id="02cca-103">Elemento de arco da VML</span><span class="sxs-lookup"><span data-stu-id="02cca-103">VML Arc Element</span></span>

<span data-ttu-id="02cca-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="02cca-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="02cca-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="02cca-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="02cca-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="02cca-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="02cca-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="02cca-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="02cca-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="02cca-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="02cca-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="02cca-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="02cca-110">Forma de arco predefinida.</span><span class="sxs-lookup"><span data-stu-id="02cca-110">Predefined arc shape.</span></span>

<span data-ttu-id="02cca-111">O **arco** usa os atributos [StartAngle](msdn-online-vml-startangle-attribute.md) e [ângulo](msdn-online-vml-endangle-attribute.md) de fim.</span><span class="sxs-lookup"><span data-stu-id="02cca-111">**Arc** uses the [startangle](msdn-online-vml-startangle-attribute.md) and [endangle](msdn-online-vml-endangle-attribute.md) attributes.</span></span>

<span data-ttu-id="02cca-112">Veja a seguir o código mínimo necessário para produzir uma imagem.</span><span class="sxs-lookup"><span data-stu-id="02cca-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:arc
   style="top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```





 

 