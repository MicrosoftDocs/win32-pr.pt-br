---
title: Atributo TableLimits de VML
description: Atributo TableLimits de VML
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641169"
---
# <a name="vml-tablelimits-attribute"></a><span data-ttu-id="5d108-103">Atributo TableLimits de VML</span><span class="sxs-lookup"><span data-stu-id="5d108-103">VML TableLimits Attribute</span></span>

<span data-ttu-id="5d108-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5d108-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5d108-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="5d108-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5d108-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="5d108-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5d108-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="5d108-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5d108-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5d108-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5d108-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5d108-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5d108-110">Lista de valores de altura mínima para cada linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="5d108-110">List of minimum height values for each row in a table.</span></span> <span data-ttu-id="5d108-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5d108-111">Read/write.</span></span> <span data-ttu-id="5d108-112">**VgLengthArray**.</span><span class="sxs-lookup"><span data-stu-id="5d108-112">**VgLengthArray**.</span></span>

<span data-ttu-id="5d108-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="5d108-113">**Applies To**</span></span>

[<span data-ttu-id="5d108-114">Forma</span><span class="sxs-lookup"><span data-stu-id="5d108-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="5d108-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="5d108-115">**Tag Syntax**</span></span>

<span data-ttu-id="5d108-116"><v: *Element* o:tablelimits = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="5d108-116"><v: *element* o:tablelimits=" *expression* "></span></span>

<span data-ttu-id="5d108-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="5d108-117">**Remarks**</span></span>

<span data-ttu-id="5d108-118">Usado pelo Microsoft PowerPoint para tabelas nativas.</span><span class="sxs-lookup"><span data-stu-id="5d108-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="5d108-119">O valor padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5d108-119">Default value is **Null**.</span></span>

<span data-ttu-id="5d108-120">Embora o valor seja armazenado em uma forma, o atributo só é útil quando a tabela é composta de formas agrupadas.</span><span class="sxs-lookup"><span data-stu-id="5d108-120">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.</span></span> <span data-ttu-id="5d108-121">Quando o texto é adicionado às células da tabela, a altura da linha pode aumentar.</span><span class="sxs-lookup"><span data-stu-id="5d108-121">When text is added to table cells, the row height may increase.</span></span> <span data-ttu-id="5d108-122">O atributo **TableLimits** armazena a altura da linha original para que, se o texto for excluído, a altura da linha não fique abaixo do valor original.</span><span class="sxs-lookup"><span data-stu-id="5d108-122">The **TableLimits** attribute stores the original row height so that if text is deleted, the row height will not fall below the original value.</span></span>

<span data-ttu-id="5d108-123">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="5d108-123">*Microsoft Office Extensions Attribute*</span></span>

 

 