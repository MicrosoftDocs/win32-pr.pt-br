---
title: Propriedade Left (objeto characters)
description: Saiba mais sobre a propriedade de objeto caracteres à esquerda. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988932"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="c3a83-104">Propriedade Left (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="c3a83-104">Left Property (Characters Object)</span></span>

<span data-ttu-id="c3a83-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3a83-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c3a83-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="c3a83-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c3a83-107">Retorna ou define a borda esquerda do quadro do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="c3a83-107">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="c3a83-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="c3a83-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c3a83-109">\*Agente \***. Caracteres ("**_characterid_\*_")._ \*  \[  =  *Valor* esquerdo\]</span><span class="sxs-lookup"><span data-stu-id="c3a83-109">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="c3a83-110">Parte</span><span class="sxs-lookup"><span data-stu-id="c3a83-110">Part</span></span>    | <span data-ttu-id="c3a83-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3a83-111">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="c3a83-112">*value*</span><span class="sxs-lookup"><span data-stu-id="c3a83-112">*value*</span></span> | <span data-ttu-id="c3a83-113">Um inteiro longo que especifica a borda esquerda do quadro do caractere.</span><span class="sxs-lookup"><span data-stu-id="c3a83-113">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3a83-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a83-114">Remarks</span></span>

<span data-ttu-id="c3a83-115">A propriedade **Left** é sempre expressa em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="c3a83-115">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="c3a83-116">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="c3a83-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="c3a83-117">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c3a83-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




