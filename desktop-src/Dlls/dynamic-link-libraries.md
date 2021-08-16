---
description: Uma DLL (biblioteca de vínculo dinâmico) é um módulo que contém funções e dados que podem ser usados por outro módulo (aplicativo ou DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: bibliotecas Dynamic-Link (bibliotecas de vínculo dinâmico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369091464aad63ea78ea9f24a84fb4eb49eb810a1faff14571fc67e2e39bb0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815895"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>bibliotecas Dynamic-Link (bibliotecas de vínculo dinâmico)

Uma *DLL* (biblioteca de vínculo dinâmico) é um módulo que contém funções e dados que podem ser usados por outro módulo (aplicativo ou DLL).

Uma DLL pode definir dois tipos de funções: exportada e interna. As funções exportadas devem ser chamadas por outros módulos, bem como de dentro da DLL em que são definidas. As funções internas normalmente devem ser chamadas somente de dentro da DLL em que são definidas. Embora uma DLL possa exportar dados, seus dados geralmente são usados apenas por suas funções. No entanto, não há nada que impeça outro módulo de ler ou escrever esse endereço.

As DLLs fornecem uma maneira de modularizar aplicativos para que sua funcionalidade possa ser atualizada e reutilizado com mais facilidade. As DLLs também ajudam a reduzir a sobrecarga de memória quando vários aplicativos usam a mesma funcionalidade ao mesmo tempo, porque, embora cada aplicativo receba sua própria cópia dos dados da DLL, os aplicativos compartilham o código DLL.

O Windows api (interface de programação de aplicativo) do Windows é implementado como um conjunto de DLLs, portanto, qualquer processo que usa a API Windows usa vinculação dinâmica.

-   [Sobre Dynamic-Link bibliotecas](about-dynamic-link-libraries.md)
-   [Usando Dynamic-Link bibliotecas](using-dynamic-link-libraries.md)
-   [Referência da biblioteca de vínculo dinâmico](dynamic-link-library-reference.md)

> [!Note]  
> Se você for um usuário com dificuldades com uma DLL em seu computador, entre em contato com o suporte do cliente para o fornecedor de software que publica a DLL. Se você acha que precisa de suporte para um produto da Microsoft (incluindo Windows), acesse nosso site de suporte técnico em [support.microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DLLs (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
