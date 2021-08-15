---
title: Estrutura DLGTEMPLATEEX
description: Um modelo de caixa de diálogo estendido começa com um header DLGTEMPLATEEX que descreve a caixa de diálogo e especifica o número de controles na caixa de diálogo.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Caixas de diálogo da estrutura DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab23b93a72edb2da6784797dd47bdfb4a839e2e9ce662adfc6ffbe09e468ac17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503447"
---
# <a name="dlgtemplateex-structure"></a>Estrutura DLGTEMPLATEEX

Um modelo de caixa de diálogo estendido começa com um header **DLGTEMPLATEEX** que descreve a caixa de diálogo e especifica o número de controles na caixa de diálogo. Para cada controle em uma caixa de diálogo, um modelo de caixa de diálogo estendido tem um bloco de dados que usa o [**formato DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) para descrever o controle.

A **estrutura DLGTEMPLATEEX** não está definida em nenhum arquivo de header padrão. A definição de estrutura é fornecida aqui para explicar o formato de um modelo estendido para uma caixa de diálogo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a>Membros

<dl> <dt>

**dlgVer**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O número de versão do modelo de caixa de diálogo estendido. Esse membro deve ser definido como 1.

</dd> <dt>

**assinatura**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Indica se um modelo é um modelo de caixa de diálogo estendido. Se **a** assinatura for 0xFFFF, esse será um modelo de caixa de diálogo estendido. Nesse caso, o **membro dlgVer** especifica o número de versão do modelo. Se **a** assinatura for qualquer valor diferente 0xFFFF, esse será um modelo de caixa de diálogo padrão que usa as estruturas [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) e [**DLGITEMTEMPLATE.**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate)

</dd> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O identificador de contexto de ajuda para a janela da caixa de diálogo. Quando o sistema envia uma [**mensagem WM \_ HELP,**](../shell/wm-help.md) ele passa esse valor no **membro wContextId** da [**estrutura HELPINFO.**](/windows/win32/api/winuser/ns-winuser-helpinfo)

</dd> <dt>

**Exstyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Os estilos estendidos do Windows. Esse membro não é usado ao criar caixas de diálogo, mas os aplicativos que usam modelos de caixa de diálogo podem usá-lo para criar outros tipos de janelas. Para ver uma lista de valores, consulte [**Estilos de janela estendidos.**](/windows/desktop/winmsg/extended-window-styles)

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O estilo da caixa de diálogo. Esse membro pode ser uma combinação de valores de [estilo de janela](/windows/desktop/winmsg/window-styles) e valores de estilo de caixa de [diálogo](dialog-box-styles.md).

Se  style incluir o estilo da caixa de diálogo **DS \_ SETFONT** ou **DS \_ SHELLFONT,** o header **DLGTEMPLATEEX** do modelo de caixa de diálogo estendido conterá quatro membros adicionais ( **pointsize,** **weight,** **italic** e **typeface**) que descrevem a fonte a ser usada para o texto na área do cliente e controles da caixa de diálogo. Se possível, o sistema cria uma fonte de acordo com os valores especificados nesses membros. Em seguida, o sistema [**envia uma mensagem WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) para a caixa de diálogo e para cada controle para fornecer um alça para a fonte.

Para obter mais informações, consulte [Fontes da caixa de diálogo](about-dialog-boxes.md).

</dd> <dt>

**cDlgItems**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O número de controles na caixa de diálogo.

</dd> <dt>

**x**
</dt> <dd>

Tipo: **short**

</dd> <dd>

A coordenada X, em unidades da caixa de diálogo, do canto superior esquerdo da caixa de diálogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **short**

</dd> <dd>

A coordenada Y, em unidades da caixa de diálogo, do canto superior esquerdo da caixa de diálogo.

</dd> <dt>

**Cx**
</dt> <dd>

Tipo: **short**

</dd> <dd>

A largura, em unidades da caixa de diálogo, da caixa de diálogo.

</dd> <dt>

**Cy**
</dt> <dd>

Tipo: **short**

</dd> <dd>

A altura, em unidades da caixa de diálogo, da caixa de diálogo.

</dd> <dt>

**Menu**
</dt> <dd>

Tipo: **sz \_ Or \_ Ord**

</dd> <dd>

Uma matriz de comprimento variável de elementos de 16 bits que identifica um recurso de menu para a caixa de diálogo. Se o primeiro elemento dessa matriz for 0x0000, a caixa de diálogo não terá nenhum menu e a matriz não terá nenhum outro elemento. Se o primeiro elemento for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de um recurso de menu em um arquivo executável. Se o primeiro elemento tiver qualquer outro valor, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de um recurso de menu em um arquivo executável.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **sz \_ Or \_ Ord**

</dd> <dd>

Uma matriz de comprimento variável de elementos de 16 bits que identifica a classe de janela da caixa de diálogo. Se o primeiro elemento da matriz for 0x0000, o sistema usará a classe de caixa de diálogo predefinida para a caixa de diálogo e a matriz não terá nenhum outro elemento. Se o primeiro elemento for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de uma classe de janela do sistema predefinida. Se o primeiro elemento tiver qualquer outro valor, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de uma classe de janela registrada.

</dd> <dt>

**title**
</dt> <dd>

Tipo: **WCHAR \[ titleLen \]**

</dd> <dd>

O título da caixa de diálogo. Se o primeiro elemento dessa matriz for 0x0000, a caixa de diálogo não terá nenhum título e a matriz não terá nenhum outro elemento.

</dd> <dt>

**Pointsize**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O tamanho do ponto da fonte a ser usada para o texto na caixa de diálogo e seus controles.

Esse membro estará presente somente se o membro **de estilo** especificar **DS \_ SETFONT** ou **DS \_ SHELLFONT**.

</dd> <dt>

**weight**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O peso da fonte. Observe que, embora esse possa ser qualquer um dos valores listados para o membro **lfWeight** da estrutura [**LOGFONT,**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qualquer valor usado será alterado automaticamente para **FW \_ NORMAL.**

Esse membro estará presente somente se o membro **de estilo** especificar **DS \_ SETFONT** ou **DS \_ SHELLFONT**.

</dd> <dt>

**italic**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Indica se a fonte é itálico. Se esse valor for **TRUE,** a fonte será itálico.

Esse membro estará presente somente se o membro **de estilo** especificar **DS \_ SETFONT** ou **DS \_ SHELLFONT**.

</dd> <dt>

**Charset**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

O conjunto de caracteres a ser usado. Para obter mais informações, consulte **o membro lfcharset** de [**LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

Esse membro estará presente somente se o membro **de estilo** especificar **DS \_ SETFONT** ou **DS \_ SHELLFONT**.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **WCHAR \[ stringLen \]**

</dd> <dd>

O nome da face de tipo da fonte.

Esse membro estará presente somente se o membro **de estilo** especificar **DS \_ SETFONT** ou **DS \_ SHELLFONT**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar um modelo de caixa de diálogo estendido em vez de um modelo de caixa de diálogo padrão nas funções [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)e [**DialogBoxIndirect.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)

Após o **header DLGTEMPLATEEX em um** modelo de caixa de diálogo estendido, há uma ou mais estruturas [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) que descrevem os controles da caixa de diálogo. O **membro cDlgItems** da estrutura **DLGITEMTEMPLATEEX** especifica o número de estruturas **DLGITEMTEMPLATEEX** que seguem no modelo.

Cada [**estrutura DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) no modelo deve ser alinhada em um **limite DWORD.** Se  o membro de estilo especificar o estilo **DS \_ SETFONT** ou **DS \_ SHELLFONT,** a primeira **estrutura DLGITEMTEMPLATEEX** começará no primeiro limite **DWORD** após a cadeia de caracteres **typeface.** Se esses estilos não são especificados, a primeira estrutura começa no primeiro limite **DWORD** após a cadeia **de caracteres de** título.

As **matrizes de menu**, **windowClass**, **title** e **typeface** devem ser alinhadas nos limites **do WORD.**

Se você especificar cadeias de caracteres no **menu**, **windowClass**, **título** e **matrizes de face** de tipo, deverá usar cadeias de caracteres Unicode. Use a função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para gerar essas cadeias de caracteres Unicode a partir de cadeias de caracteres ANSI.

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

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

