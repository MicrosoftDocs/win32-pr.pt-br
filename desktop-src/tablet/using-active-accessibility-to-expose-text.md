---
description: Visão geral do uso da acessibilidade ativa para expor texto.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Usando Acessibilidade Ativa para expor texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798422"
---
# <a name="using-active-accessibility-to-expose-text"></a><span data-ttu-id="62919-103">Usando Acessibilidade Ativa para expor texto</span><span class="sxs-lookup"><span data-stu-id="62919-103">Using Active Accessibility to Expose Text</span></span>

<span data-ttu-id="62919-104">Os aplicativos podem usar o Microsoft Acessibilidade Ativa para expor texto.</span><span class="sxs-lookup"><span data-stu-id="62919-104">Applications can use Microsoft Active Accessibility to expose text.</span></span> <span data-ttu-id="62919-105">No entanto, a interface [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) definida por versões anteriores do acessibilidade ativa não é otimizada para expor grandes quantidades de Rich Text.</span><span class="sxs-lookup"><span data-stu-id="62919-105">However, the [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) interface defined by earlier versions of Active Accessibility is not optimized for exposing large amounts of rich text.</span></span> <span data-ttu-id="62919-106">As versões posteriores definem as interfaces que são otimizadas para expor grandes quantidades de texto e atributos textuais.</span><span class="sxs-lookup"><span data-stu-id="62919-106">Later versions define interfaces that are optimized for exposing large amounts of text and textual attributes.</span></span>

<span data-ttu-id="62919-107">Para expor texto de grandes quantidades, crie objetos COM (Component Object Model separados) que dão suporte a [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), ou elementos filho, para representar cada execução de texto.</span><span class="sxs-lookup"><span data-stu-id="62919-107">To expose large amounts text, create separate Component Object Model (COM) objects that support [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), or child elements, to represent each run of text.</span></span> <span data-ttu-id="62919-108">Uma execução é uma linha, ou parte de uma linha, que compartilha a mesma formatação.</span><span class="sxs-lookup"><span data-stu-id="62919-108">A run is a line, or portion of a line, that shares the same formatting.</span></span>

<span data-ttu-id="62919-109">Acessibilidade Ativa expõe apenas o texto e sua localização, mas não tem nenhum mecanismo para expor a formatação do texto.</span><span class="sxs-lookup"><span data-stu-id="62919-109">Active Accessibility exposes only the text and its location, but has no mechanism for exposing the formatting of the text.</span></span> <span data-ttu-id="62919-110">Apesar dessas limitações, alguns programas usam Acessibilidade Ativa para expor texto.</span><span class="sxs-lookup"><span data-stu-id="62919-110">Despite these limitations, some programs use Active Accessibility to expose text.</span></span> <span data-ttu-id="62919-111">Por exemplo, o Microsoft Internet Explorer e o Microsoft Visual Studio usam Acessibilidade Ativa para expor grandes quantidades de texto.</span><span class="sxs-lookup"><span data-stu-id="62919-111">For example, Microsoft Internet Explorer and Microsoft Visual Studio both use Active Accessibility to expose large amounts of text.</span></span>

<span data-ttu-id="62919-112">Para obter mais informações sobre como expor texto usando Acessibilidade Ativa, consulte [acessibilidade](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="62919-112">For more information about exposing text by using Active Accessibility, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
