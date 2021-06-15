---
title: Propriedade FontName (objeto Balloon)
description: Saiba mais sobre a propriedade de objeto Balão FontName. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47e14935f913ce81b5faed5a49c3d731a73532f
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068262"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="b76b4-104">Propriedade FontName (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="b76b4-104">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="b76b4-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b76b4-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b76b4-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b76b4-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b76b4-107">Retorna ou define a fonte usada no balão de palavras para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="b76b4-107">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="b76b4-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b76b4-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b76b4-109">*agent.\***Characters("**_CharacterID_*_"). Fonte Balloon.FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="b76b4-109">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="b76b4-110">Parte</span><span class="sxs-lookup"><span data-stu-id="b76b4-110">Part</span></span>   | <span data-ttu-id="b76b4-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b76b4-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="b76b4-112">*Fonte*</span><span class="sxs-lookup"><span data-stu-id="b76b4-112">*font*</span></span> | <span data-ttu-id="b76b4-113">Um valor de cadeia de caracteres correspondente ao nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="b76b4-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b76b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b76b4-114">Remarks</span></span>

<span data-ttu-id="b76b4-115">A [**propriedade FontName**](fontname-property.md) define a fonte usada para exibir texto na janela de balão de palavra de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b76b4-115">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="b76b4-116">O valor padrão para as configurações de fonte do balão de palavra de um caractere é definido no Editor de Caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b76b4-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="b76b4-117">Além disso, o usuário pode substituir as configurações de fonte para todos os caracteres na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b76b4-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="b76b4-118">Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="b76b4-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="b76b4-119">Se você estiver usando um caractere que não compilou, verifique as propriedades [**FontName**](fontname-property.md) e [**FontCharSet**](fontcharset-property.md) do caractere para determinar se elas são apropriadas para sua localidade.</span><span class="sxs-lookup"><span data-stu-id="b76b4-119">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="b76b4-120">Talvez seja necessário definir esses valores antes de usar o [**método Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro da palavra balão.</span><span class="sxs-lookup"><span data-stu-id="b76b4-120">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




