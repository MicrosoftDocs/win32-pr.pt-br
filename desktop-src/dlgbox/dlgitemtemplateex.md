---
title: Estrutura DLGITEMTEMPLATEEX
description: Um bloco de texto usado por um modelo de caixa de diálogo estendido para descrever a caixa de diálogo estendida. Para ver uma descrição do formato de um modelo de caixa de diálogo estendido, consulte DLGTEMPLATEEX.
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
ms.openlocfilehash: ad2bf1795f5059ec1fdda00ddb6a93cfe396dae5b4119d392eff42382fa978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785862"
---
# <a name="dlgitemtemplateex-structure"></a>Estrutura DLGITEMTEMPLATEEX

Um bloco de texto usado por um modelo de caixa de diálogo estendido para descrever a caixa de diálogo estendida. Para ver uma descrição do formato de um modelo de caixa de diálogo estendido, consulte [**DLGTEMPLATEEX**](dlgtemplateex.md).

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

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O identificador de contexto de ajuda para o controle. Quando o sistema envia uma [**mensagem DE \_ AJUDA**](../shell/wm-help.md) do WM, ele passa o **valor helpID** no **membro dwContextId** da [**estrutura HELPINFO.**](/windows/win32/api/winuser/ns-winuser-helpinfo)

</dd> <dt>

**Exstyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Os estilos estendidos para uma janela. Esse membro não é usado para criar controles em caixas de diálogo, mas aplicativos que usam modelos de caixa de diálogo podem usá-lo para criar outros tipos de janelas. Para ver uma lista de valores, consulte [**Estilos de janela estendidos.**](/windows/desktop/winmsg/extended-window-styles)

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O estilo do controle. Esse membro pode ser uma combinação de valores de estilo de janela [(como](/windows/desktop/winmsg/window-styles) **WS \_ BORDER**) e um ou mais dos valores de estilo [de](/windows/desktop/Controls/common-control-styles) controle (como **BS \_ PUSHBUTTON** **e ES \_ LEFT**).

</dd> <dt>

**x**
</dt> <dd>

Tipo: **short**

</dd> <dd>

A coordenada X, em unidades da caixa de diálogo, do canto superior esquerdo do controle. Essa coordenada é sempre relativa ao canto superior esquerdo da área de cliente da caixa de diálogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **short**

</dd> <dd>

A coordenada y, em unidades da caixa de diálogo, do canto superior esquerdo do controle. Essa coordenada é sempre relativa ao canto superior esquerdo da área de cliente da caixa de diálogo.

</dd> <dt>

**Cx**
</dt> <dd>

Tipo: **short**

</dd> <dd>

A largura, em unidades da caixa de diálogo, do controle .

</dd> <dt>

**Cy**
</dt> <dd>

Tipo: **short**

</dd> <dd>

A altura, em unidades da caixa de diálogo, do controle.

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O identificador de controle.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **sz \_ Or \_ Ord**

</dd> <dd>

Uma matriz de comprimento variável de elementos de 16 bits que especifica a classe de janela do controle . Se o primeiro elemento dessa matriz for qualquer valor diferente de 0xFFFF, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de uma classe de janela registrada.

Se o primeiro elemento for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de uma classe de sistema predefinida. O ordinal pode ser um dos valores atom a seguir.



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

Tipo: **sz \_ Or \_ Ord**

</dd> <dd>

Uma matriz de comprimento variável de elementos de 16 bits que contém o texto inicial ou o identificador de recurso do controle. Se o primeiro elemento dessa matriz for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de um recurso, como um ícone, em um arquivo executável. Você pode usar um identificador de recurso para controles, como controles de ícone estáticos, que carregam e exibem um ícone ou outro recurso em vez de texto. Se o primeiro elemento for qualquer valor diferente de 0xFFFF, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o texto inicial.

</dd> <dt>

**extraCount**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O número de bytes de dados de criação que seguem este membro. Se esse valor for maior que zero, os dados de criação começarão no próximo **limite word.** Esses dados de criação podem ser de qualquer tamanho e formato. O procedimento de janela do controle deve ser capaz de interpretar os dados. Quando o sistema cria o controle , ele passa um ponteiro para esses dados no parâmetro *lParam* da mensagem [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) que ele envia para o controle.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um modelo estendido para uma caixa de diálogo consiste em um header [**DLGTEMPLATEEX**](dlgtemplateex.md) seguido por uma **estrutura DLGITEMTEMPLATEEX** para cada controle na caixa de diálogo.

Cada **estrutura DLGITEMTEMPLATEEX** deve ser alinhada em um **limite DWORD.** As matrizes **windowClass e** **title** de comprimento variável devem ser alinhadas nos limites **do WORD.** A matriz de dados de criação, se alguma, deve ser alinhada em um **limite word.**

Se você especificar cadeias de caracteres nas **matrizes windowClass** e **title,** deverá usar cadeias de caracteres Unicode. Use a [**função MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para gerar cadeias de caracteres Unicode de cadeias de caracteres ANSI.

Os **membros x**, **y**, **cx** e **cy** especificam valores em unidades de caixa de diálogo. Você pode converter esses valores em unidades de tela (pixels) usando a [**função MapDialogRect.**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Createdialogindirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**Createdialogindirectparam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**Createwindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**Dialogboxindirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**Dialogboxindirectparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATEEX**](dlgtemplateex.md)
</dt> <dt>

[**Mapdialogrect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**ajuda do WM \_**](../shell/wm-help.md)
</dt> </dl>

 

