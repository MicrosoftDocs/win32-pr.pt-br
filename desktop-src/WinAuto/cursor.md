---
title: Cursor (referência de elemento de interface do usuário MSAA)
description: Um cursor é uma pequena imagem cujo local na tela é controlado por um dispositivo apontador, como um mouse, uma caneta ou um trackball. Quando o usuário move o dispositivo apontador, o sistema operacional Windows move o cursor.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291902"
---
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve os cursores para fins de referência de elemento da interface do usuário do MSAA. Como usar cursores em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Um cursor é uma pequena imagem cujo local na tela é controlado por um dispositivo apontador, como um mouse, uma caneta ou um trackball. Quando o usuário move o dispositivo apontador, o sistema operacional Windows move o cursor.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um cursor dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um cursor dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**Get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— a propriedade **ChildCount** é zero.
-   [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– os desenvolvedores podem criar cursores personalizados ou usar os cursores predefinidos que são identificados por sua ID de cursor. A propriedade **Name** do cursor depende de sua forma e é uma das seguintes: 

    | Forma do cursor     | Nome              |
    |------------------|-------------------|
    | Cursor personalizado    | Conhecidos         |
    | seta da IDC \_       | "Normal"          |
    | \_IBEAM IDC       | Editar            |
    | espera da IDC \_        | Esperado            |
    | \_cruzada da IDC       | Gráfico         |
    | coseta do IDC \_     | Limpeza              |
    | \_SIZENWSE IDC    | "Tamanho do NWSE"       |
    | \_SIZENESW IDC    | "Tamanho do NESW"       |
    | \_SIZEWE IDC      | "Tamanho horizontal" |
    | \_SIZENS IDC      | "Tamanho vertical"   |
    | \_SIZEALL IDC     | Prosseguir            |
    | \_n º da IDC          | Proibido       |
    | \_APPSTARTING IDC | "Início do aplicativo"       |
    | ajuda da IDC \_        | Podem            |

    

     

-   [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— a propriedade **role** é [**\_ \_ cursor do sistema de função**](object-roles.md).
-   [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— a propriedade **State** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):

    [**Estado \_ sistema \_**](object-state-constants.md) de estado invisível do sistema \| [ **\_ \_ flutuante**](object-state-constants.md)

## <a name="notes"></a>Observações

-   Ao contrário de outros elementos da interface do usuário, o objeto de cursor não tem um identificador de janela associado. Para obter acesso ao objeto cursor, os clientes devem definir um [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e aguardar que o objeto de cursor gere eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




