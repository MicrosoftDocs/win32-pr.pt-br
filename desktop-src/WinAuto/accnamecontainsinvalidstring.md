---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811399"
---
# <a name="accnamecontainsinvalidstring"></a><span data-ttu-id="6d095-103">AccNameContainsInvalidString</span><span class="sxs-lookup"><span data-stu-id="6d095-103">AccNameContainsInvalidString</span></span>

## <a name="text"></a><span data-ttu-id="6d095-104">Texto</span><span class="sxs-lookup"><span data-stu-id="6d095-104">Text</span></span>

<span data-ttu-id="6d095-105">accName não deve conter a cadeia de caracteres {0}</span><span class="sxs-lookup"><span data-stu-id="6d095-105">accName should not contain the string {0}</span></span>

## <a name="type"></a><span data-ttu-id="6d095-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d095-106">Type</span></span>

<span data-ttu-id="6d095-107">Erro</span><span class="sxs-lookup"><span data-stu-id="6d095-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="6d095-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d095-108">Description</span></span>

<span data-ttu-id="6d095-109">O nome de um elemento contém caracteres inválidos (esses caracteres são substituídos por AccChecker).</span><span class="sxs-lookup"><span data-stu-id="6d095-109">The name of an element contains invalid characters (these characters are replaced by AccChecker).</span></span> <span data-ttu-id="6d095-110">Por exemplo, o método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usado para recuperar o nome MSAA de um elemento retorna uma cadeia de caracteres que contém a tabulação, nova linha ou caractere de e comercial.</span><span class="sxs-lookup"><span data-stu-id="6d095-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string that contains tab, newline, or ampersand characters.</span></span>

<span data-ttu-id="6d095-111">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um elemento pode ter um nome não-pronunciado e não intuitivo.</span><span class="sxs-lookup"><span data-stu-id="6d095-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="6d095-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="6d095-112">Possible causes</span></span>

<span data-ttu-id="6d095-113">O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.</span><span class="sxs-lookup"><span data-stu-id="6d095-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d095-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d095-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d095-115">**IAccessible:: obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="6d095-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="6d095-116">Propriedade Name</span><span class="sxs-lookup"><span data-stu-id="6d095-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




