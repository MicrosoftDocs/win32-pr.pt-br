---
title: Recurso de caixa de diálogo
description: Define uma caixa de diálogo. | Recurso de caixa de diálogo
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menus de recursos de caixa de diálogo e outros recursos
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760788"
---
# <a name="dialog-resource"></a>Recurso de caixa de diálogo

Define uma caixa de diálogo. A instrução define a posição e as dimensões da caixa de diálogo na tela, bem como o estilo da caixa de diálogo.

> [!Note]  
> A **caixa de diálogo** é uma ID de recurso obsoleta. Os novos aplicativos devem usar o [**DIALOGEX**](dialogex-resource.md).

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um valor inteiro de 16 bits sem sinal exclusivo que identifica a caixa de diálogo.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*
</dt> <dd>

Opções para a caixa de diálogo. Isso pode ser zero ou mais das instruções a seguir.



| Instrução                                                        | Descrição                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Legenda**](caption-statement.md) "*texto*"                    | Legenda da caixa de diálogo se ela tiver uma barra de título. Para obter mais informações, consulte [**legenda**](caption-statement.md).                                                                             |
| [**Características**](characteristics-statement.md) *DWORD*     | Valor **DWORD** definido pelo usuário para uso pelas ferramentas de recurso. Esse valor não é usado pelo sistema. Para obter mais informações, consulte [**características**](characteristics-statement.md).                |
| [](class-statement.md) *Classe* de classe                         | Um inteiro não assinado de 16 bits ou uma cadeia de caracteres entre aspas duplas ("), que identifica a classe da caixa de diálogo. Para obter mais informações, consulte [**classe**](class-statement.md).      |
| **Filestyle =** *estilos estendidos*                                   | Estilo de janela estendida da caixa de diálogo. Para obter mais informações, consulte [**comstyle**](exstyle-statement.md).                                                                                     |
|  *Pontos* de fonte, *face de tipos*                                 | Tamanho do ponto e tipo da fonte. Para obter mais informações, consulte [**fonte**](font-statement.md).                                                                                              |
| [](language-statement.md) *Idioma* do idioma, *subidioma* | Idioma da caixa de diálogo. Para obter mais informações, consulte [**Language**](language-statement.md).                                                                                                |
|  *Menuname* do menu                                              | Menu a ser usado. Esse valor é o nome do menu ou seu identificador de inteiro.                                                                                                        |
| [](style-statement.md) *Estilos* de estilo                        | Estilos da caixa de diálogo. Para obter mais informações, consulte [**estilo**](style-statement.md).                                                                                                        |
| [](version-statement.md) *DWORD* da versão                     | Valor **DWORD** definido pelo usuário. Essa instrução destina-se ao uso por ferramentas de recursos adicionais e não é usada pelo sistema. Para obter mais informações, consulte [**versão**](version-statement.md). |



 

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="remarks"></a>Comentários

A função [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retorna as unidades base da caixa de diálogo em pixels. O significado exato das coordenadas depende do estilo definido pela instrução de opção de [**estilo**](style-statement.md) . Para caixas de diálogo de estilo filho, as coordenadas são relativas à origem da janela pai, a menos que a caixa de diálogo tenha o estilo **DS \_ ABSALIGN**; nesse caso, as coordenadas são relativas à origem da tela de exibição.

Não use o estilo **\_ filho WS** com uma caixa de diálogo modal. A função [**caixa**](/windows/win32/api/winuser/nf-winuser-dialogboxa) sempre desabilita o pai/proprietário da caixa de diálogo recém-criada. Quando uma janela pai é desabilitada, suas janelas filhas são desabilitadas implicitamente. Como a janela pai da caixa de diálogo estilo filho está desabilitada, a caixa de diálogo estilo filho também é.

Se uma caixa de diálogo tiver o estilo **DS \_ ABSALIGN** , as coordenadas para seu canto superior esquerdo serão relativas à origem da tela em vez de ao canto superior esquerdo da janela pai. Normalmente, você usaria esse estilo quando quisesse que a caixa de diálogo fosse iniciada em uma parte específica da exibição, independentemente de onde a janela pai possa estar na tela.

A caixa de **diálogo** de nome também pode ser usada como o parâmetro Class-Name para a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela com atributos de caixas de diálogo.

## <a name="examples"></a>Exemplos

O seguinte demonstra o uso da instrução **Dialog** :

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando caixas de diálogo](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Caixa**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**IDIOMA**](language-statement.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versão**](version-statement.md)
</dt> </dl>

 

 
