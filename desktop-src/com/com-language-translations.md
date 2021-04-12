---
title: Traduções de linguagem COM
description: Os componentes criados com o uso do Component Object Model (COM) podem ser reutilizados em aplicativos escritos em qualquer linguagem de programação que ofereça suporte a COM. Isso ocorre porque o COM é um padrão binário e, como tal, é independente de linguagem.
ms.assetid: 89e74768-b7bd-4ab6-9129-9e677a9c14ca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f622b83b998402e82d6cf20975331645362c55e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363674"
---
# <a name="com-language-translations"></a><span data-ttu-id="ff890-104">Traduções de linguagem COM</span><span class="sxs-lookup"><span data-stu-id="ff890-104">COM Language Translations</span></span>

<span data-ttu-id="ff890-105">Os componentes criados com o uso do Component Object Model (COM) podem ser reutilizados em aplicativos escritos em qualquer linguagem de programação que ofereça suporte a COM.</span><span class="sxs-lookup"><span data-stu-id="ff890-105">Components created using the Component Object Model (COM) can be reused in applications written in any programming language that supports COM.</span></span> <span data-ttu-id="ff890-106">Isso ocorre porque o COM é um padrão binário e, como tal, é independente de linguagem.</span><span class="sxs-lookup"><span data-stu-id="ff890-106">This is because COM is a binary standard and, as such, is language-independent.</span></span>

<span data-ttu-id="ff890-107">Objetos COM são documentados na linguagem ou linguagens de programação mais relevantes.</span><span class="sxs-lookup"><span data-stu-id="ff890-107">COM objects are documented in the most relevant programming language or languages.</span></span> <span data-ttu-id="ff890-108">Por exemplo, os objetos criados para uso em páginas da Web normalmente são documentados no sistema de desenvolvimento Microsoft Visual Basic, enquanto os objetos no nível do sistema geralmente são documentados em C++.</span><span class="sxs-lookup"><span data-stu-id="ff890-108">For example, objects that are created for use in webpages are typically documented in the Microsoft Visual Basic development system, whereas system-level objects are typically documented in C++.</span></span> <span data-ttu-id="ff890-109">No entanto, como o COM é neutro à linguagem, você não está limitado a usar um objeto no mesmo idioma em que ele é escrito ou documentado.</span><span class="sxs-lookup"><span data-stu-id="ff890-109">However, because COM is language-neutral, you are not limited to using an object in the same language in which it is written or documented.</span></span> <span data-ttu-id="ff890-110">Por exemplo, você pode escrever um aplicativo em JScript que usa um controle criado em C++ e documentado em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ff890-110">For example, you can write an application in JScript that uses a control created in C++ and documented in Visual Basic.</span></span>

<span data-ttu-id="ff890-111">Os tópicos a seguir discutem as diferenças entre linguagens de programação e descrevem como converter a sintaxe de objeto COM de um idioma para outro.</span><span class="sxs-lookup"><span data-stu-id="ff890-111">The following topics discuss the differences between programming languages and describe how to translate COM object syntax from one language to another.</span></span> <span data-ttu-id="ff890-112">Tópicos adicionais descrevem como usar objetos COM em vários ambientes e linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="ff890-112">Additional topics describe how to use COM objects in various scripting languages and environments.</span></span>

-   [<span data-ttu-id="ff890-113">Diferenças de sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff890-113">Syntax Differences</span></span>](syntax-differences.md)
-   [<span data-ttu-id="ff890-114">Conversões de tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ff890-114">Data Type Conversions</span></span>](data-type-conversions.md)
-   [<span data-ttu-id="ff890-115">Arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="ff890-115">IDL Files</span></span>](idl-files.md)
-   [<span data-ttu-id="ff890-116">Convertendo sintaxe de objeto COM para linguagens de programação</span><span class="sxs-lookup"><span data-stu-id="ff890-116">Translating COM Object Syntax for Programming Languages</span></span>](translating-com-object-syntax-for-programming-languages.md)
-   [<span data-ttu-id="ff890-117">Criando scripts com objetos COM</span><span class="sxs-lookup"><span data-stu-id="ff890-117">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)

<span data-ttu-id="ff890-118">A intenção é abordar os problemas mais comuns de tradução de linguagem que surgem ao usar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="ff890-118">The intent is to address the most common language translation issues that arise when using COM objects.</span></span> <span data-ttu-id="ff890-119">As técnicas e os princípios descritos se aplicam a qualquer linguagem de programação ou script que ofereça suporte a COM.</span><span class="sxs-lookup"><span data-stu-id="ff890-119">The techniques and principles described apply to any programming or scripting language that supports COM.</span></span> <span data-ttu-id="ff890-120">Como linguagens de script e linguagens de programação representam paradigmas de programação diferentes, a conversão entre linguagens de script e linguagens de programação não é resolvida.</span><span class="sxs-lookup"><span data-stu-id="ff890-120">Because scripting languages and programming languages represent different programming paradigms, translation between scripting languages and programming languages is not addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff890-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff890-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff890-122">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="ff890-122">Component Object Model (COM)</span></span>](component-object-model--com--portal.md)
</dt> </dl>

 

 




