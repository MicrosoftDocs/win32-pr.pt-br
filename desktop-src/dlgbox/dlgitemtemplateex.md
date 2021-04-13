---
title: Estrutura DLGITEMTEMPLATEEX
description: Um bloco de texto usado por um modelo de caixa de diálogo estendida para descrever a caixa de diálogo estendida. Para obter uma descrição do formato de um modelo de caixa de diálogo estendido, consulte DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Caixas de diálogo da estrutura DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369894"
---
# <a name="dlgitemtemplateex-structure"></a>Estrutura DLGITEMTEMPLATEEX

Um bloco de texto usado por um modelo de caixa de diálogo estendida para descrever a caixa de diálogo estendida. Para obter uma descrição do formato de um modelo de caixa de diálogo estendido, consulte [**DLGTEMPLATEEX**](dlgtemplateex.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a>Membros

<dl> <dt>

**HelpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O identificador de contexto da ajuda para o controle. Quando o sistema envia uma mensagem de [**\_ ajuda do WM**](../shell/wm-help.md) , ele passa o valor **HelpID** no membro **dwContextId** da estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .

</dd> <dt>

**comstyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Os estilos estendidos para uma janela. Esse membro não é usado para criar controles em caixas de diálogo, mas os aplicativos que usam modelos de caixa de diálogo podem usá-lo para criar outros tipos de janelas. Para obter uma lista de valores, consulte [**estilos de janela estendidos**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O estilo do controle. Esse membro pode ser uma combinação de [valores de estilo de janela](/windows/desktop/winmsg/window-styles) ( **como WS \_ Border**) e um ou mais dos [valores de estilo de controle](/windows/desktop/Controls/common-control-styles) (como a **BS \_** , e **es \_ à esquerda**).

</dd> <dt>

**x**
</dt> <dd>

Tipo: **curto**

</dd> <dd>

A coordenada x, nas unidades da caixa de diálogo, do canto superior esquerdo do controle. Essa coordenada é sempre relativa ao canto superior esquerdo da área do cliente da caixa de diálogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **curto**

</dd> <dd>

A coordenada y, nas unidades da caixa de diálogo, do canto superior esquerdo do controle. Essa coordenada é sempre relativa ao canto superior esquerdo da área do cliente da caixa de diálogo.

</dd> <dt>

**CX**
</dt> <dd>

Tipo: **curto**

</dd> <dd>

A largura, nas unidades da caixa de diálogo, do controle.

</dd> <dt>

**Cy**
</dt> <dd>

Tipo: **curto**

</dd> <dd>

A altura, nas unidades da caixa de diálogo, do controle.

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O identificador de controle.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **sz \_ ou \_ Ord**

</dd> <dd>

Uma matriz de comprimento variável de elementos de 16 bits que especifica a classe de janela do controle. Se o primeiro elemento dessa matriz for qualquer valor diferente de 0xFFFF, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de uma classe de janela registrada.

Se o primeiro elemento for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de uma classe de sistema predefinida. O ordinal pode ser um dos valores de Atom a seguir.



| Valor                                                                             | Significado               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>0x0080</dt> </dl> | Botão<br/>     |
| <dl> <dt>0x0081</dt> </dl> | Editar<br/>       |
| <dl> <dt>0x0082</dt> </dl> | Estático<br/>     |
| <dl> <dt>0x0083</dt> </dl> | Caixa de listagem<br/>   |
| <dl> <dt>0x0084</dt> </dl> | Barra de rolagem<br/> |
| <dl> <dt>0x0085</dt> </dl> | Caixa de combinação<br/>  |



 

</dd> <dt>

**title**
</dt> <dd>

Tipo: **sz \_ ou \_ Ord**

</dd> <dd>

Uma matriz de comprimento variável de elementos de 16 bits que contém o identificador de texto inicial ou de recurso do controle. Se o primeiro elemento dessa matriz for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de um recurso, como um ícone, em um arquivo executável. Você pode usar um identificador de recurso para controles, como controles de ícone estáticos, que carregam e exibem um ícone ou outro recurso em vez de texto. Se o primeiro elemento for qualquer valor diferente de 0xFFFF, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o texto inicial.

</dd> <dt>

**extraCount**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de bytes de dados de criação que seguem esse membro. Se esse valor for maior que zero, os dados de criação começarão no próximo limite de **palavra** . Esses dados de criação podem ser de qualquer tamanho e formato. O procedimento de janela do controle deve ser capaz de interpretar os dados. Quando o sistema cria o controle, ele passa um ponteiro para esses dados no parâmetro *lParam* da mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) que ele envia para o controle.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um modelo estendido para uma caixa de diálogo consiste em um cabeçalho [**DLGTEMPLATEEX**](dlgtemplateex.md) seguido por uma estrutura **DLGITEMTEMPLATEEX** para cada controle na caixa de diálogo.

Cada estrutura **DLGITEMTEMPLATEEX** deve estar alinhada em um limite **DWORD** . As matrizes **WindowClass** e **title** de comprimento variável devem ser alinhadas em limites de **palavras** . A matriz de dados de criação, se houver, deve estar alinhada em um limite de **palavra** .

Se você especificar cadeias de caracteres nas matrizes **WindowClass** e **title** , você deverá usar cadeias Unicode. Use a função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para gerar cadeias de caracteres Unicode de cadeias de caracteres ANSI.

Os membros **x**, **y**, **CX** e **CY** especificam valores nas unidades da caixa de diálogo. Você pode converter esses valores em unidades de tela (pixels) usando a função [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATEEX**](dlgtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**criação do WM \_**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**ajuda do WM \_**](../shell/wm-help.md)
</dt> </dl>

 

