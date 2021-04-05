---
description: Uma DLL (biblioteca de vínculo dinâmico) é um módulo que contém funções e dados que podem ser usados por outro módulo (aplicativo ou DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Bibliotecas de Dynamic-Link (bibliotecas de vínculo dinâmico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647720"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Bibliotecas de Dynamic-Link (bibliotecas de vínculo dinâmico)

Uma dll ( *biblioteca de vínculo dinâmico* ) é um módulo que contém funções e dados que podem ser usados por outro módulo (aplicativo ou dll).

Uma DLL pode definir dois tipos de funções: exportadas e internas. As funções exportadas são destinadas a serem chamadas por outros módulos, bem como de dentro da DLL em que são definidas. Normalmente, as funções internas devem ser chamadas somente de dentro da DLL em que são definidas. Embora uma DLL possa exportar dados, os dados geralmente são usados apenas por suas funções. No entanto, não há nada para impedir que outro módulo leia ou grave esse endereço.

As DLLs fornecem uma maneira de modularizar aplicativos para que sua funcionalidade possa ser atualizada e reutilizada com mais facilidade. As DLLs também ajudam a reduzir a sobrecarga de memória quando vários aplicativos usam a mesma funcionalidade ao mesmo tempo, porque, embora cada aplicativo receba sua própria cópia dos dados de DLL, os aplicativos compartilham o código de DLL.

A API (interface de programação de aplicativo) do Windows é implementada como um conjunto de DLLs, de modo que qualquer processo que usa a API do Windows usa vinculação dinâmica.

-   [Sobre bibliotecas de Dynamic-Link](about-dynamic-link-libraries.md)
-   [Usando bibliotecas de Dynamic-Link](using-dynamic-link-libraries.md)
-   [Referência da biblioteca de vínculo dinâmico](dynamic-link-library-reference.md)

> [!Note]  
> Se você for um usuário tendo dificuldades com uma DLL em seu computador, deverá entrar em contato com o atendimento ao cliente para o fornecedor de software que publica a DLL. Se você sentir que precisa de suporte para um produto da Microsoft (incluindo o Windows), acesse nosso site de suporte técnico em [support.Microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DLLs (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
