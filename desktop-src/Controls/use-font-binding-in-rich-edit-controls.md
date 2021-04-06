---
title: Como usar a associação de fontes em controles de edição avançados
description: O Microsoft Rich Edit 3,0 atribui um conjunto de caracteres a caracteres de texto sem formatação, dependendo de seu contexto.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17c2f8e0e8c1b57611839a5bbf992f9af6bf65
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103823618"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Como usar a associação de fontes em controles de edição avançados

O Microsoft Rich Edit 3,0 atribui um conjunto de caracteres a caracteres de texto sem formatação, dependendo de seu contexto. Alguns exemplos incluem:

-   Caracteres gregos são atribuídos **a \_ charset grego**.
-   Os símbolos Hangul são atribuídos a **\_ charset Hangul**.
-   Caracteres chineses são atribuídos **SHIFTJIS \_ charset** se caracteres kana forem encontrados próximo ou **GB2312 \_ charset** se nenhum kana for encontrado próximo.
-   Caracteres ANSI não neutros são atribuídos **a \_ charset ANSI** em qualquer evento.

> [!Note]  
> O controle de edição rico usa Unicode internamente, portanto, esse uso de conjuntos de caracteres é diferente do original usado nas especificações de fonte. Mas a estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) tem um local bem definido para o conjunto de caracteres.

 

Caracteres neutros, como espaços em branco e dígitos, são atribuídos a um conjunto de caracteres, dependendo de seu contexto. Por exemplo, um espaço em branco cercado por caracteres do mesmo conjunto de caracteres obtém esse conjunto de caracteres. Os valores neutros e os dígitos usados para texto bidirecional são atribuídos a conjuntos de caracteres de uma maneira baseada no algoritmo bidirecional Unicode.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="use-font-binding-in-a-rich-edit-control"></a>Usar a associação de fontes em um controle de edição rico

Depois que os conjuntos de caracteres são atribuídos, a edição rica examina o texto ao redor do ponto de inserção para frente e para trás para localizar as fontes mais próximas que foram usadas para os conjuntos de caracteres. Se nenhuma fonte for encontrada para um conjunto de caracteres, a edição avançada usará a fonte escolhida pelo cliente para esse conjunto de caracteres. Se o cliente não tiver especificado uma fonte para o conjunto de caracteres, a edição avançada usará a fonte padrão para esse conjunto de caracteres. Se o cliente quiser alguma outra fonte, o cliente sempre poderá alterá-la, mas essa abordagem funcionará na maior parte do tempo. As opções de fonte padrão atuais são baseadas na tabela a seguir. Observe que as fontes padrão são definidas por processo e há listas separadas para uso da interface do usuário e para uso sem interface do usuário.



| Idioma                    | Nome da fonte da interface do usuário  | Tamanho da fonte da interface do usuário | nome da fonte sem interface do usuário | tamanho da fonte sem interface do usuário |
|-----------------------------|---------------|--------------|------------------|------------------|
| Ocidente, CE, ME, vietnamita | Tahoma        | 8            | Arial            | 10               |
| Japonês                    | MS UI Gothic  | 9            | MS P Gothic      | 10               |
| Coreano                      | Gulim         | 9            | Gulim            | 9                |
| Chinês simplificado          | SimSun        | 9            | SimSun           | 10               |
| Chinês tradicional         | PMingLiU      | 9            | PMingLiU         | 9                |
| Tailandês                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Símbolos                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tâmil                       | Latha         | 8            | Latha            | 10               |
| Georgiano, armênio          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Portanto, na tabela de associação de fonte padrão (as entradas têm um conjunto de caracteres, um nome de fonte e um tamanho), a edição avançada permite que \_ o conjunto de caracteres ANSI corresponda a vários conjuntos de caracteres, enquanto o grupo de caractere apropriado corresponde a outras fontes em uma base de um para um. Com mais precisão, a edição avançada usa a opção de conjunto de caracteres ANSI, \_ sempre que nenhuma outra alternativa é encontrada. Você poderá especificar uma granularidade mais fina do que esta; por exemplo, atribua um conjunto \_ de caracteres arábico específico para execuções em árabe, uma fonte grega específica para execuções em grego e assim por diante. Essa granularidade mais fina também será usada se uma fonte com o carimbo de conjunto de caracteres desejado for encontrada em algum lugar no documento antes da área que está sendo associada à fonte.

Observe que a edição avançada atualmente não lida com um glifo ausente em uma fonte que alega oferecer suporte a um conjunto de caracteres, mas está incompleta. No momento da exibição em um script complexo, a edição rica acaba sabendo que esse glifo está ausente, mas não faz com que o armazenamento de backup use uma nova fonte. Normalmente, a vinculação de fonte subjacente do sistema operacional fará isso.

## <a name="remarks"></a>Comentários

**Edição avançada 4,1:** Para definir a fonte padrão de um script, chame [**em \_ SETCHARFORMAT**](em-setcharformat.md) com [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a), especificando valores para os membros **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID** . Além disso, para obter a fonte padrão de uma página de código específica, chame em [**\_ GETCHARFORMAT**](em-getcharformat.md) com **CHARFORMAT2**, especificando valores para os membros **bCharSet** e **LCID** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




