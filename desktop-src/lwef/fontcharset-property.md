---
title: Propriedade FontCharSet
description: Propriedade FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292677"
---
# <a name="fontcharset-property"></a><span data-ttu-id="4b060-103">Propriedade FontCharSet</span><span class="sxs-lookup"><span data-stu-id="4b060-103">FontCharSet Property</span></span>

<span data-ttu-id="4b060-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b060-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4b060-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="4b060-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4b060-106">Retorna ou define o conjunto de caracteres para a fonte exibida no balão de palavras do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="4b060-106">Returns or sets the character set for the font displayed in the specified character's word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="4b060-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="4b060-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4b060-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). Valor de Balloon. FontCharSet* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="4b060-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontCharSet*\* \[ = *value*\]</span></span>



| <span data-ttu-id="4b060-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4b060-109">Part</span></span>    | <span data-ttu-id="4b060-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b060-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b060-111">*value*</span><span class="sxs-lookup"><span data-stu-id="4b060-111">*value*</span></span> | <span data-ttu-id="4b060-112">Um valor inteiro que especifica o conjunto de caracteres usado pela fonte.</span><span class="sxs-lookup"><span data-stu-id="4b060-112">An integer value that specifies the character set used by the font.</span></span> <span data-ttu-id="4b060-113">A seguir estão algumas configurações comuns para valor: 0 caracteres padrão do Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4b060-113">The following are some common settings for value: 0 Standard Windows characters (ANSI).</span></span><br/> <span data-ttu-id="4b060-114">1 conjunto de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="4b060-114">1 Default character set.</span></span><br/> <span data-ttu-id="4b060-115">2 o conjunto de caracteres do símbolo.</span><span class="sxs-lookup"><span data-stu-id="4b060-115">2 The symbol character set.</span></span><br/> <span data-ttu-id="4b060-116">128 conjunto de caracteres de byte duplo (DBCS) exclusivo para a versão japonesa do Windows.</span><span class="sxs-lookup"><span data-stu-id="4b060-116">128 Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span><br/> <span data-ttu-id="4b060-117">129 conjunto de caracteres de byte duplo (DBCS) exclusivo para a versão coreana do Windows.</span><span class="sxs-lookup"><span data-stu-id="4b060-117">129 Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span><br/> <span data-ttu-id="4b060-118">134 conjunto de caracteres de byte duplo (DBCS) exclusivo para a versão em chinês simplificado do Windows.</span><span class="sxs-lookup"><span data-stu-id="4b060-118">134 Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span><br/> <span data-ttu-id="4b060-119">136 conjunto de caracteres de dois bytes (DBCS) exclusivo para a versão em Chinês tradicional do Windows.</span><span class="sxs-lookup"><span data-stu-id="4b060-119">136 Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span><br/> <span data-ttu-id="4b060-120">255 caracteres estendidos normalmente exibidos por aplicativos do Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="4b060-120">255 Extended characters normally displayed by Microsoft MS-DOS applications.</span></span><br/> <span data-ttu-id="4b060-121">Para outros valores de conjunto de caracteres, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4b060-121">For other character set values, consult the Platform SDK documentation.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b060-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b060-122">Remarks</span></span>

<span data-ttu-id="4b060-123">O valor padrão do conjunto de caracteres do balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4b060-123">The default value for the character set of a character's word balloon is set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4b060-124">Além disso, o usuário pode substituir as configurações de conjunto de caracteres para todos os caracteres na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4b060-124">In addition, the user can override the character-set settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="4b060-125">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="4b060-125">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="4b060-126">Se você estiver usando um caractere que não foi compilado, verifique as propriedades [**NomeDaFonte**](fontname-property.md) e **FontCharSet** do caractere para determinar se elas são apropriadas para sua localidade.</span><span class="sxs-lookup"><span data-stu-id="4b060-126">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and **FontCharSet** properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="4b060-127">Talvez seja necessário definir esses valores antes de usar o método [**Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro da palavra balão.</span><span class="sxs-lookup"><span data-stu-id="4b060-127">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="4b060-128">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4b060-128">See Also</span></span>

[<span data-ttu-id="4b060-129">**Propriedade FontName**</span><span class="sxs-lookup"><span data-stu-id="4b060-129">**FontName property**</span></span>](fontname-property.md)


 

 





