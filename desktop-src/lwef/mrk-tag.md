---
title: Marca de mrk
description: Marca de mrk
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635905"
---
# <a name="mrk-tag"></a><span data-ttu-id="7acd7-103">Marca de mrk</span><span class="sxs-lookup"><span data-stu-id="7acd7-103">Mrk Tag</span></span>

<span data-ttu-id="7acd7-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7acd7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7acd7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="7acd7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7acd7-106">Define um indicador no texto falado.</span><span class="sxs-lookup"><span data-stu-id="7acd7-106">Defines a bookmark in the spoken text.</span></span>

</dd> <dt>

<span data-ttu-id="7acd7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="7acd7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7acd7-108">**\\Mrk =***número***\\**</span><span class="sxs-lookup"><span data-stu-id="7acd7-108">**\\Mrk=***number***\\**</span></span>



| <span data-ttu-id="7acd7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7acd7-109">Part</span></span>     | <span data-ttu-id="7acd7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7acd7-110">Description</span></span>                                        |
|----------|----------------------------------------------------|
| <span data-ttu-id="7acd7-111">*number*</span><span class="sxs-lookup"><span data-stu-id="7acd7-111">*number*</span></span> | <span data-ttu-id="7acd7-112">Um valor inteiro longo que identifica o indicador.</span><span class="sxs-lookup"><span data-stu-id="7acd7-112">A Long integer value that identifies the bookmark.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="7acd7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7acd7-113">Remarks</span></span>

<span data-ttu-id="7acd7-114">Quando o servidor processa um indicador, ele gera um evento de indicador.</span><span class="sxs-lookup"><span data-stu-id="7acd7-114">When the server processes a bookmark, it generates a bookmark event.</span></span> <span data-ttu-id="7acd7-115">Você deve especificar um número maior que zero (0) e não igual a 2147483647 ou 2147483646.</span><span class="sxs-lookup"><span data-stu-id="7acd7-115">You must specify a number greater than zero (0) and not equal to 2147483647 or 2147483646.</span></span>

 

 




