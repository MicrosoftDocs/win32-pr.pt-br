---
title: Propriedade FontName (objeto Balloon)
description: Propriedade FontName
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085090"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="1be3d-103">Propriedade FontName (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="1be3d-103">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="1be3d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1be3d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1be3d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="1be3d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1be3d-106">Retorna ou define a fonte usada no balão de palavras para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="1be3d-106">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="1be3d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="1be3d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1be3d-108">\*Caracteres Agent. \***("**_characterid_\*_"). Fonte Balloon. NomeDaFonte_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="1be3d-108">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="1be3d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1be3d-109">Part</span></span>   | <span data-ttu-id="1be3d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1be3d-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="1be3d-111">*la*</span><span class="sxs-lookup"><span data-stu-id="1be3d-111">*font*</span></span> | <span data-ttu-id="1be3d-112">Um valor de cadeia de caracteres correspondente ao nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="1be3d-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1be3d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1be3d-113">Remarks</span></span>

<span data-ttu-id="1be3d-114">A propriedade [**FontName**](fontname-property.md) define a fonte usada para exibir texto na janela balão de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1be3d-114">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="1be3d-115">O valor padrão das configurações de fonte do balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1be3d-115">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1be3d-116">Além disso, o usuário pode substituir as configurações de fonte para todos os caracteres na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1be3d-116">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="1be3d-117">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="1be3d-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="1be3d-118">Se você estiver usando um caractere que não foi compilado, verifique as propriedades [**NomeDaFonte**](fontname-property.md) e [**FontCharSet**](fontcharset-property.md) do caractere para determinar se elas são apropriadas para sua localidade.</span><span class="sxs-lookup"><span data-stu-id="1be3d-118">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="1be3d-119">Talvez seja necessário definir esses valores antes de usar o método [**Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro da palavra balão.</span><span class="sxs-lookup"><span data-stu-id="1be3d-119">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




