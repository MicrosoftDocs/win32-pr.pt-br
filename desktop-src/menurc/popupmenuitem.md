---
title: Estrutura POPUPMENUITEM
description: Contém informações sobre os itens de menu em um recurso de menu que abre um menu ou um submenu. A definição de estrutura fornecida aqui é apenas para explicação; ele não está presente em nenhum arquivo de header padrão.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menus de estrutura POPUPMENUITEM e outros recursos
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62d769e9756f0d15e7377a79f9aa94802a469746807e3a32b5ba329f76484b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011696"
---
# <a name="popupmenuitem-structure"></a>Estrutura POPUPMENUITEM

Contém informações sobre os itens de menu em um recurso de menu que abre um menu ou um submenu. A definição de estrutura fornecida aqui é apenas para explicação; ele não está presente em nenhum arquivo de header padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a>Membros

<dl> <dt>

**tipo**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Descreve o item de menu. Alguns dos valores que esse membro pode ter incluem aqueles mostrados na lista abaixo.

Além dos valores mostrados, esse membro também pode ser uma combinação dos valores de tipo listados com o **membro fType** da [**estrutura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) Os valores de tipo são aqueles que começam com \_ MFT. Para usar esses valores de tipo MFT \_ \* predefinidos, inclua a seguinte instrução no arquivo .rc:

`#include "winuser.h"`



| Valor                                                                                                                                                                                                    | Significado                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ END**</dt> <dt>0x80</dt> </dl>       | O item de menu é o último no menu; o sinalizador é usado internamente pelo sistema. <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ Pop-UP**</dt> <dt>0x01</dt> </dl> | O item de menu abre um menu ou um submenu; o sinalizador é usado internamente pelo sistema. <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Descreve o item de menu. Esse membro pode ser uma combinação dos valores de estado listados com **o membro dwState** da [**estrutura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) Os valores de estado são aqueles que começam com o \_ MFS. Para usar esses valores de estado \_ \* predefinidos do MFS, inclua a seguinte instrução no arquivo .rc:

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Uma expressão numérica que identifica o item de menu que é passado na mensagem [**WM \_ COMMAND.**](wm-command.md)

</dd> <dt>

**Resinfo**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Um conjunto de sinalizadores de bits que especificam o tipo de item de menu. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                       | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ END**</dt> <dt>0x80</dt> </dl>       | O item de menu é o último neste submenu ou recurso de menu; esse sinalizador é usado internamente pelo sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ Pop-up**</dt> <dt>0x01</dt> </dl> | O item de menu abre um menu ou um submenu; o sinalizador é usado internamente pelo sistema.<br/>                     |



 

</dd> <dt>

**Menutext**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que contém o texto deste item de menu. Não há nenhum limite fixo no tamanho dessa cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Há uma estrutura **POPUPMENUITEM para** cada item de menu que abre um menu ou um submenu. Identifique esse tipo de item  de menu definindo o membro de tipo como **\_ POPUP MF** e definindo o bit **\_ POPUP MFR** no membro **resInfo** como 0x0001. Nesse caso, os dados finais gravados no recurso [**\_ menu RT**](/windows/desktop/menurc/resource-types) para o menu ou submenu são a [**estrutura MENUHELPID.**](menuhelpid.md) **MENUHELPID** contém uma expressão numérica que identifica o menu durante o processamento [**\_ da AJUDA do WM.**](../shell/wm-help.md)

Além disso, cada estrutura **POPUPMENUITEM** que tem o bit **\_ POPUP MFR** definido no membro **resInfo** será seguida por uma estrutura [**MENUHELPID**](menuhelpid.md) mais um número adicional de estruturas **POPUPMENUITEM,** uma para cada item de menu nesse submenu. A última **estrutura POPUPMENUITEM** no submenu terá o bit **MFR \_ END** definido no **membro resInfo.** Para encontrar o final do recurso, procure um **MFR \_ END** correspondente para cada **\_ POPUP MFR** mais um **MFR \_ END** adicional que corresponde ao conjunto mais externo de itens de menu.

Indique o último item de menu definindo o **membro de tipo** como **MF \_ END.** Como você pode aninhar submenus, pode haver vários níveis de **MF \_ END.** Nessas instâncias, os itens de menu são sequenciais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**MENUHELPID**](menuhelpid.md)
</dt> <dt>

[**Menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

