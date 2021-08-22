---
description: Visão geral do uso da acessibilidade ativa para expor texto.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Usando Acessibilidade Ativa para expor texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 247d78149b82d15eb7c2dbd4ac2b2463d53c5d454dcb7877906197661de36ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334786"
---
# <a name="using-active-accessibility-to-expose-text"></a>Usando Acessibilidade Ativa para expor texto

Os aplicativos podem usar o Microsoft Acessibilidade Ativa para expor texto. No entanto, a interface [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) definida por versões anteriores do acessibilidade ativa não é otimizada para expor grandes quantidades de Rich Text. As versões posteriores definem as interfaces que são otimizadas para expor grandes quantidades de texto e atributos textuais.

Para expor texto de grandes quantidades, crie objetos COM (Component Object Model separados) que dão suporte a [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), ou elementos filho, para representar cada execução de texto. Uma execução é uma linha, ou parte de uma linha, que compartilha a mesma formatação.

Acessibilidade Ativa expõe apenas o texto e sua localização, mas não tem nenhum mecanismo para expor a formatação do texto. Apesar dessas limitações, alguns programas usam Acessibilidade Ativa para expor texto. por exemplo, o Microsoft Internet Explorer e o Microsoft Visual Studio usam Acessibilidade Ativa para expor grandes quantidades de texto.

Para obter mais informações sobre como expor texto usando Acessibilidade Ativa, consulte [acessibilidade](../accessibility/accessibility.md).

 

 
