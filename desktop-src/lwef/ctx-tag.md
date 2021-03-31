---
title: Marca de CTX
description: Marca de CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005758"
---
# <a name="ctx-tag"></a><span data-ttu-id="53ad6-103">Marca de CTX</span><span class="sxs-lookup"><span data-stu-id="53ad6-103">Ctx Tag</span></span>

<span data-ttu-id="53ad6-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53ad6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="53ad6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="53ad6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="53ad6-106">Define o contexto do texto de saída.</span><span class="sxs-lookup"><span data-stu-id="53ad6-106">Sets the context of the output text.</span></span>

</dd> <dt>

<span data-ttu-id="53ad6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="53ad6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="53ad6-108">\\**CTX** = *cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="53ad6-108">\\**Ctx**=*string*</span></span>\\



| <span data-ttu-id="53ad6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="53ad6-109">Part</span></span>     | <span data-ttu-id="53ad6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="53ad6-110">Description</span></span>                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53ad6-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="53ad6-111">*string*</span></span> | <span data-ttu-id="53ad6-112">Uma cadeia de caracteres que especifica o contexto do texto a seguir, que determina como os símbolos ou as abreviações são falados.</span><span class="sxs-lookup"><span data-stu-id="53ad6-112">A string specifying the context of the text that follows, which determines how symbols or abbreviations are spoken.</span></span><br/> <span data-ttu-id="53ad6-113">**"Endereço"**    Endereços e/ou números de telefone.</span><span class="sxs-lookup"><span data-stu-id="53ad6-113">**"Address"**    Addresses and/or phone numbers.</span></span><br/> <span data-ttu-id="53ad6-114">**"Email"**    Email.</span><span class="sxs-lookup"><span data-stu-id="53ad6-114">**"E-mail"**    Electronic mail.</span></span><br/> <span data-ttu-id="53ad6-115">O contexto **"desconhecido"** (padrão) é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="53ad6-115">**"Unknown"**    (Default) Context is unknown.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="53ad6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="53ad6-116">Remarks</span></span>

<span data-ttu-id="53ad6-117">Essa marca só tem suporte para a saída gerada por TTS.</span><span class="sxs-lookup"><span data-stu-id="53ad6-117">This tag is supported only for TTS-generated output.</span></span> <span data-ttu-id="53ad6-118">O intervalo de valores para o parâmetro pode variar dependendo do mecanismo de TTS instalado.</span><span class="sxs-lookup"><span data-stu-id="53ad6-118">The range of values for the parameter may vary depending on the installed TTS engine.</span></span>

 

 





