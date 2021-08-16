---
title: Como usar a associação de fonte em controles de edição rich
description: O Microsoft Rich Edit 3.0 atribui um conjunto de caracteres a caracteres de texto sem-texto, dependendo do contexto.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3086f9f74469bc535700f28b6eeb45c204024beb34c21663139fd3d63746d4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829020"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Como usar a associação de fonte em controles de edição rich

O Microsoft Rich Edit 3.0 atribui um conjunto de caracteres a caracteres de texto sem-texto, dependendo do contexto. Alguns exemplos incluem:

-   Caracteres gregos são **atribuídos a GREEK \_ CHARSET.**
-   Os símbolos hangul são atribuídos **a HANGUL \_ CHARSET.**
-   Caracteres chineses são **atribuídos a SHIFTJIS \_ CHARSET** se caracteres kana são encontrados próximos ou **GB2312 \_ CHARSET** se nenhum kana for encontrado próximo.
-   Caracteres ANSI não neutros são **atribuídos a ANSI \_ CHARSET** em qualquer evento.

> [!Note]  
> O controle de edição rich usa Unicode internamente, portanto, esse uso de conjuntos de caracteres difere do original usado em especificações de fonte. Mas a [**estrutura CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) tem um local bem definido para o conjunto de caracteres.

 

Caracteres neutros, como espaços em branco e dígitos, são atribuídos a um conjunto de caracteres dependendo do contexto. Por exemplo, um espaço em branco entre caracteres do mesmo conjunto de caracteres obtém esse conjunto de caracteres. Neutros e dígitos usados para texto bidirecional são atribuídos conjuntos de caracteres de uma maneira baseada no algoritmo bidirecional Unicode.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="use-font-binding-in-a-rich-edit-control"></a>Usar associação de fonte em um controle de edição rich

Depois que os conjuntos de caracteres são atribuídos, o Rich Edit examina o texto em torno do ponto de inserção para frente e para trás para encontrar as fontes mais próximas que foram usadas para os conjuntos de caracteres. Se nenhuma fonte for encontrada para um conjunto de caracteres, o Rich Edit usará a fonte escolhida pelo cliente para esse conjunto de caracteres. Se o cliente não tiver especificado uma fonte para o conjunto de caracteres, o Rich Edit usará a fonte padrão para esse conjunto de caracteres. Se o cliente quiser alguma outra fonte, o cliente sempre poderá alterá-la, mas essa abordagem funcionará na maioria das vezes. As opções de fonte padrão atuais são baseadas na tabela a seguir. Observe que as fontes padrão são definidas por processo e há listas separadas para uso da interface do usuário e para uso não interface do usuário.



| Idioma                    | Nome da fonte da interface do usuário  | Tamanho da fonte da interface do usuário | nome da fonte não interface do usuário | tamanho da fonte que não é da interface do usuário |
|-----------------------------|---------------|--------------|------------------|------------------|
| Oeste, CE, ME, México | Tahoma        | 8            | Arial            | 10               |
| Japonês                    | MS UI Gothic  | 9            | MS P Gothic      | 10               |
| Coreano                      | Gulim         | 9            | Gulim            | 9                |
| Chinês simplificado          | Simsun        | 9            | SimSun           | 10               |
| Chinês tradicional         | Pmingliu      | 9            | Pmingliu         | 9                |
| Tailandês                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Símbolos                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tâmil                       | Latha         | 8            | Latha            | 10               |
| Grego, Grego          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Portanto, na tabela de associação de fonte padrão (as entradas têm um conjunto de caracteres, o nome da fonte e o tamanho), o Rich Edit permite que ANSI CHARSET corresponde a vários conjuntos de caracteres, enquanto o conjunto de caracteres apropriado corresponde a outras fontes em uma base \_ um-para-um. Mais precisamente, a edição rich usa a opção \_ ANSI CHARSET sempre que nenhuma outra alternativa é encontrada. Você poderá especificar uma granularidade mais fina do que esta; por exemplo, atribua um CHARSET ÁRABE específico para as executações em árabe, uma fonte grego específica para as executações do grego \_ e assim por diante. Essa granularidade mais fina também será usada se uma fonte com o carimbo de conjunto de caracteres desejado for encontrada em algum lugar no documento antes da área que está sendo vinculada à fonte.

Observe que o Rich Edit atualmente não trata um glifo ausente em uma fonte que declara dar suporte a um conjunto de caracteres, mas está incompleto. Em tempo de exibição em um script complexo, o Rich Edit acaba sabendo que esse glifo está ausente, mas não faz com que o armazenamento de backing use uma nova fonte. Normalmente, a vinculação de fonte subjacente do sistema operacional fará isso.

## <a name="remarks"></a>Comentários

**Rich Edit 4.1:** Para definir a fonte padrão para um script, chame [**EM \_ SETCHARFORMAT**](em-setcharformat.md) com [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a), especificando valores para os membros **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **lcid.** Além disso, para obter a fonte padrão de uma página de código específica, chame [**EM \_ GETCHARFORMAT**](em-getcharformat.md) com **CHARFORMAT2**, especificando valores para os **membros bCharSet** e **lcid.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição rich](using-rich-edit-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




