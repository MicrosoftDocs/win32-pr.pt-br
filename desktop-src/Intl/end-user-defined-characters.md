---
description: Os caracteres definidos pelo usuário final (EUDC) em conjuntos de caracteres de dois bytes (DBCS) e caracteres de área de uso particular (PUA) em Unicode são caracteres personalizados.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caracteres da área de uso privado e definido pelo usuário final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297277"
---
# <a name="end-user-defined-and-private-use-area-characters"></a><span data-ttu-id="24c15-103">Caracteres da área de uso privado e definido pelo usuário final</span><span class="sxs-lookup"><span data-stu-id="24c15-103">End-User-Defined and Private Use Area Characters</span></span>

<span data-ttu-id="24c15-104">Os caracteres definidos pelo usuário final (EUDC) em [conjuntos de caracteres de dois bytes](double-byte-character-sets.md) (DBCS) e caracteres de área de uso particular (pua) em [Unicode](unicode.md) são caracteres personalizados.</span><span class="sxs-lookup"><span data-stu-id="24c15-104">End-user-defined characters (EUDC) in [double-byte character sets](double-byte-character-sets.md) (DBCSs) and private use area (PUA) characters in [Unicode](unicode.md) are custom characters.</span></span> <span data-ttu-id="24c15-105">Eles podem ser definidos e implementados por um usuário final ou por outra parte, como um fabricante de equipamento, um grupo de usuários, um corpo governamental ou uma empresa de design de fontes.</span><span class="sxs-lookup"><span data-stu-id="24c15-105">They can be defined and implemented either by an end user or by another party, such as an equipment manufacturer, a user group, a government body, or a font design company.</span></span> <span data-ttu-id="24c15-106">Seu uso permite que os usuários formem nomes e outras palavras usando caracteres que não estão disponíveis em fontes de tela e de impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="24c15-106">Their use enables users to form names and other words using characters that are not available in standard screen and printer fonts.</span></span>

<span data-ttu-id="24c15-107">Os caracteres EUDC e PUA podem ser atribuídos de forma diferente, ou não atribuídos, em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="24c15-107">The EUDC and PUA characters can be assigned differently, or not assigned at all, on different computers.</span></span> <span data-ttu-id="24c15-108">Algumas páginas de código têm extensões que reutilizam o intervalo EUDC, e essas extensões podem entrar em conflito entre si.</span><span class="sxs-lookup"><span data-stu-id="24c15-108">Some code pages have extensions that reuse the EUDC range, and these extensions can conflict with each other.</span></span> <span data-ttu-id="24c15-109">Em outros casos, um fabricante pode fornecer um conjunto personalizado de caracteres em um desses intervalos.</span><span class="sxs-lookup"><span data-stu-id="24c15-109">In other cases, a manufacturer might provide a custom set of characters in one of these ranges.</span></span> <span data-ttu-id="24c15-110">Além disso, os grupos de usuários podem tentar fornecer caracteres adicionais no PUA.</span><span class="sxs-lookup"><span data-stu-id="24c15-110">Additionally, user groups can attempt to provide additional characters in the PUA.</span></span> <span data-ttu-id="24c15-111">Diferentes combinações desses casos podem causar conflitos.</span><span class="sxs-lookup"><span data-stu-id="24c15-111">Different combinations of these cases can cause conflict.</span></span> <span data-ttu-id="24c15-112">Ao criar aplicativos que dependem de caracteres EUDC ou PUA, você deve ter em mente as interpretações conflitantes de um ponto de código individual.</span><span class="sxs-lookup"><span data-stu-id="24c15-112">When creating applications that rely on EUDC or PUA characters, you should keep in mind the conflicting interpretations of an individual code point.</span></span>

<span data-ttu-id="24c15-113">Os tópicos a seguir discutem as fontes que dão suporte a EUDCs e acesso e gerenciamento para estes caracteres:</span><span class="sxs-lookup"><span data-stu-id="24c15-113">The following topics discuss the fonts that support EUDCs, and access and management for these characters:</span></span>

-   [<span data-ttu-id="24c15-114">Fontes e conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="24c15-114">Character Sets and Fonts</span></span>](character-sets-and-fonts.md)
-   [<span data-ttu-id="24c15-115">Entradas do registro EUDC</span><span class="sxs-lookup"><span data-stu-id="24c15-115">EUDC Registry Entries</span></span>](eudc-registry-entries.md)

## <a name="related-topics"></a><span data-ttu-id="24c15-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24c15-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24c15-117">Sobre Unicode e conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="24c15-117">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



