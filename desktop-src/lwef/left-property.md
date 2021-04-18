---
title: Propriedade Left (objeto characters)
description: Propriedade Left
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105756790"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="e8b08-103">Propriedade Left (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="e8b08-103">Left Property (Characters Object)</span></span>

<span data-ttu-id="e8b08-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e8b08-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e8b08-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="e8b08-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e8b08-106">Retorna ou define a borda esquerda do quadro do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="e8b08-106">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="e8b08-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="e8b08-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e8b08-108">\*Agente \***. Caracteres ("**_characterid_\*_")._ \*  \[  =  *Valor* esquerdo\]</span><span class="sxs-lookup"><span data-stu-id="e8b08-108">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="e8b08-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e8b08-109">Part</span></span>    | <span data-ttu-id="e8b08-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8b08-110">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="e8b08-111">*value*</span><span class="sxs-lookup"><span data-stu-id="e8b08-111">*value*</span></span> | <span data-ttu-id="e8b08-112">Um inteiro longo que especifica a borda esquerda do quadro do caractere.</span><span class="sxs-lookup"><span data-stu-id="e8b08-112">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8b08-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8b08-113">Remarks</span></span>

<span data-ttu-id="e8b08-114">A propriedade **Left** é sempre expressa em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="e8b08-114">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="e8b08-115">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="e8b08-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="e8b08-116">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e8b08-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




