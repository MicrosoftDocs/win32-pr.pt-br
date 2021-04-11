---
title: Evento de indicador
description: Evento de indicador
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159651"
---
# <a name="bookmark-event"></a><span data-ttu-id="22fc3-103">Evento de indicador</span><span class="sxs-lookup"><span data-stu-id="22fc3-103">Bookmark Event</span></span>

<span data-ttu-id="22fc3-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22fc3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="22fc3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="22fc3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="22fc3-106">Ocorre quando um indicador em uma cadeia de caracteres de texto de fala que seu aplicativo definiu é ativado.</span><span class="sxs-lookup"><span data-stu-id="22fc3-106">Occurs when a bookmark in a speech text string that your application defined is activated.</span></span>

</dd> <dt>

<span data-ttu-id="22fc3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="22fc3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="22fc3-108"> Indicador de *subagente* \_  **(ByVal** *BookmarkID\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="22fc3-108">**Sub** *agent*\_**Bookmark** **(ByVal** *BookmarkID\*\*\*)*\*</span></span>



| <span data-ttu-id="22fc3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="22fc3-109">Part</span></span>         | <span data-ttu-id="22fc3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="22fc3-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="22fc3-111">*BookmarkID*</span><span class="sxs-lookup"><span data-stu-id="22fc3-111">*BookmarkID*</span></span> | <span data-ttu-id="22fc3-112">Um inteiro longo que identifica o número do indicador.</span><span class="sxs-lookup"><span data-stu-id="22fc3-112">A Long integer identifying the bookmark number.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="22fc3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="22fc3-113">Remarks</span></span>

<span data-ttu-id="22fc3-114">Para especificar um evento de indicador, use o método [**Speak**](speak-method.md) com uma marca **mrk** no texto fornecido.</span><span class="sxs-lookup"><span data-stu-id="22fc3-114">To specify a bookmark event, use the [**Speak**](speak-method.md) method with a **Mrk** tag in your supplied text.</span></span> <span data-ttu-id="22fc3-115">Para obter mais informações sobre marcas, consulte marcas de saída de fala.</span><span class="sxs-lookup"><span data-stu-id="22fc3-115">For more information about tags, see Speech Output Tags.</span></span>

 

 




