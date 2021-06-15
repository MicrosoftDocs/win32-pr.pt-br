---
title: Propriedade FontSize (objeto Balloon)
description: Saiba mais sobre a propriedade de objeto de balão FontSize. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068213"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="a8176-104">Propriedade FontSize (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="a8176-104">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="a8176-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a8176-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a8176-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="a8176-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a8176-107">Retorna ou define o tamanho da fonte com suporte para o balão de palavras para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="a8176-107">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a8176-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="a8176-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a8176-109">*Agent. \* \* \* caracteres* \*  **("**_Characterid_*_"). Pontos de balão. FontSize_* \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="a8176-109">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="a8176-110">Parte</span><span class="sxs-lookup"><span data-stu-id="a8176-110">Part</span></span>     | <span data-ttu-id="a8176-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8176-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="a8176-112">*Faixas*</span><span class="sxs-lookup"><span data-stu-id="a8176-112">*Points*</span></span> | <span data-ttu-id="a8176-113">Um valor inteiro longo que especifica o tamanho da fonte em pontos.</span><span class="sxs-lookup"><span data-stu-id="a8176-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8176-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8176-114">Remarks</span></span>

<span data-ttu-id="a8176-115">A propriedade [**FontSize**](fontsize-property.md) retorna um valor inteiro longo especificando o tamanho da fonte atual em pontos.</span><span class="sxs-lookup"><span data-stu-id="a8176-115">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="a8176-116">O valor máximo para **FontSize** é de 2160 pontos.</span><span class="sxs-lookup"><span data-stu-id="a8176-116">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="a8176-117">O valor padrão das configurações de fonte do balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a8176-117">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a8176-118">Além disso, o usuário pode substituir as configurações de fonte para todos os caracteres na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a8176-118">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




