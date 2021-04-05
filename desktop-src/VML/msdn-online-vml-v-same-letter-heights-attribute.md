---
title: VML V-atributo de altura da mesma letra
description: VML V-atributo de altura da mesma letra
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641215"
---
# <a name="vml-v-same-letter-heights-attribute"></a><span data-ttu-id="a08da-103">VML V-atributo de altura da mesma letra</span><span class="sxs-lookup"><span data-stu-id="a08da-103">VML V-Same-Letter-Heights Attribute</span></span>

<span data-ttu-id="a08da-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a08da-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a08da-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a08da-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a08da-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a08da-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a08da-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a08da-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a08da-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a08da-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a08da-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a08da-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a08da-110">Determina se todas as letras terão a mesma altura, independentemente do caso inicial.</span><span class="sxs-lookup"><span data-stu-id="a08da-110">Determines whether all letters will be the same height regardless of initial case.</span></span> <span data-ttu-id="a08da-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a08da-111">Read/write.</span></span> <span data-ttu-id="a08da-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a08da-112">**VgTriState**.</span></span>

<span data-ttu-id="a08da-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a08da-113">**Applies To**</span></span>

[<span data-ttu-id="a08da-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a08da-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a08da-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a08da-115">**Tag Syntax**</span></span>

<span data-ttu-id="a08da-116"><v: *elemento* Style = "v-mesma-Letter-altura: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a08da-116"><v: *element* style="v-same-letter-heights: *expression* "></span></span>

<span data-ttu-id="a08da-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="a08da-117">**Script Syntax**</span></span>

<span data-ttu-id="a08da-118">*elemento* . Style. v-mesma letra-altura = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="a08da-118">*element* .style.v-same-letter-heights="*expression*"</span></span>

<span data-ttu-id="a08da-119">*expressão* = de *elemento*. Style. v-mesma letra-altura</span><span class="sxs-lookup"><span data-stu-id="a08da-119">*expression*=*element*.style.v-same-letter-heights</span></span>

<span data-ttu-id="a08da-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a08da-120">**Remarks**</span></span>

<span data-ttu-id="a08da-121">Se **for true**, as letras minúsculas serão esticadas para a altura das letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="a08da-121">If **True**, the lowercase letters are stretched to the height of the uppercase letters.</span></span> <span data-ttu-id="a08da-122">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="a08da-122">The default value is **False**.</span></span>

<span data-ttu-id="a08da-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="a08da-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="a08da-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a08da-124">**Example**</span></span>

<span data-ttu-id="a08da-125">Todas as letras terão a mesma altura, independentemente do caso.</span><span class="sxs-lookup"><span data-stu-id="a08da-125">All letters will be the same height, regardless of case.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 