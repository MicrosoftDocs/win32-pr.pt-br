---
title: Atributo de cadeia de caracteres VML
description: Atributo de cadeia de caracteres VML
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6c172b4ca1f5049a3e89528a2333378164f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366282"
---
# <a name="vml-string-attribute"></a><span data-ttu-id="8e9d4-103">Atributo de cadeia de caracteres VML</span><span class="sxs-lookup"><span data-stu-id="8e9d4-103">VML String Attribute</span></span>

<span data-ttu-id="8e9d4-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8e9d4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8e9d4-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="8e9d4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8e9d4-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="8e9d4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8e9d4-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="8e9d4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8e9d4-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8e9d4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8e9d4-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8e9d4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8e9d4-110">Define o texto do caminho do texto.</span><span class="sxs-lookup"><span data-stu-id="8e9d4-110">Defines the text of the text path.</span></span> <span data-ttu-id="8e9d4-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8e9d4-111">Read/write.</span></span> <span data-ttu-id="8e9d4-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="8e9d4-112">**String**.</span></span>

<span data-ttu-id="8e9d4-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="8e9d4-113">**Applies To**</span></span>

[<span data-ttu-id="8e9d4-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="8e9d4-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="8e9d4-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="8e9d4-115">**Tag Syntax**</span></span>

<span data-ttu-id="8e9d4-116"><v: *Element* String = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="8e9d4-116"><v: *element* string=" *expression* "></span></span>

<span data-ttu-id="8e9d4-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="8e9d4-117">**Script Syntax**</span></span>

<span data-ttu-id="8e9d4-118">*Element* . String = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="8e9d4-118">*element* .string="*expression*"</span></span>

<span data-ttu-id="8e9d4-119">*expressão* = de *elemento*. String</span><span class="sxs-lookup"><span data-stu-id="8e9d4-119">*expression*=*element*.string</span></span>

<span data-ttu-id="8e9d4-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="8e9d4-120">**Remarks**</span></span>

<span data-ttu-id="8e9d4-121">Você deve atribuir uma cadeia de texto para exibir texto em um caminho de texto.</span><span class="sxs-lookup"><span data-stu-id="8e9d4-121">You must assign a text string to display text on a text path.</span></span>

<span data-ttu-id="8e9d4-122">Atributo padrão da VML</span><span class="sxs-lookup"><span data-stu-id="8e9d4-122">VML Standard Attribute</span></span>

<span data-ttu-id="8e9d4-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="8e9d4-123">**Example**</span></span>

<span data-ttu-id="8e9d4-124">A cadeia de caracteres que será exibida é "texto em VML".</span><span class="sxs-lookup"><span data-stu-id="8e9d4-124">The string that will be displayed is "VML Text".</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 