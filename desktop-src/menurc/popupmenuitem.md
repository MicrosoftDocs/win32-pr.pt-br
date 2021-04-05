---
title: Estrutura POPUPMENUITEM
description: Contém informações sobre os itens de menu em um recurso de menu que abre um menu ou um submenu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
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
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918123"
---
# <a name="popupmenuitem-structure"></a>Estrutura POPUPMENUITEM

Contém informações sobre os itens de menu em um recurso de menu que abre um menu ou um submenu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

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

Descreve o item de menu. Alguns dos valores que esse membro pode ter incluem os mostrados na lista abaixo.

Além dos valores mostrados, esse membro também pode ser uma combinação dos valores de tipo listados com o membro **ftype** da estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Os valores de tipo são aqueles que começam com MFT \_ . Para usar esses valores de tipo de MFT predefinidos \_ \* , inclua a seguinte instrução no arquivo. rc:

`#include "winuser.h"`



| Valor                                                                                                                                                                                                    | Significado                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ ENCERRAR**</dt> <dt>0x80</dt> </dl>       | O item de menu é o último no menu; o sinalizador é usado internamente pelo sistema. <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x01</dt> </dl> | O item de menu abre um menu ou um submenu; o sinalizador é usado internamente pelo sistema. <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Descreve o item de menu. Esse membro pode ser uma combinação dos valores de estado listados com o membro **dwState** da estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Os valores de estado são aqueles que começam com MFS \_ . Para usar esses valores de estado de MFS predefinidos \_ \* , inclua a seguinte instrução no arquivo. rc:

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Uma expressão numérica que identifica o item de menu que é passado na mensagem de [**\_ comando do WM**](wm-command.md) .

</dd> <dt>

**resInfo**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Um conjunto de sinalizadores de bits que especificam o tipo de item de menu. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                       | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**Mfr \_ ENCERRAR**</dt> <dt>0x80</dt> </dl>       | O item de menu é o último neste submenu ou recurso de menu; Esse sinalizador é usado internamente pelo sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**Mfr \_ POPUP**</dt> <dt>0x01</dt> </dl> | O item de menu abre um menu ou um submenu; o sinalizador é usado internamente pelo sistema.<br/>                     |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que contém o texto para este item de menu. Não há nenhum limite fixo para o tamanho dessa cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Há uma estrutura **POPUPMENUITEM** para cada item de menu que abre um menu ou um submenu. Identifique esse tipo de item de menu definindo o membro de **tipo** como **\_ Popup MF** e definindo o bit de **\_ Popup mfr** no membro **resInfo** como 0x0001. Nesse caso, os dados finais gravados no recurso [**de \_ menu RT**](/windows/desktop/menurc/resource-types) para o menu ou submenu é a estrutura [**MENUHELPID**](menuhelpid.md) . **MENUHELPID** contém uma expressão numérica que identifica o menu durante o processamento da [**\_ ajuda do WM**](../shell/wm-help.md) .

Além disso, toda estrutura **POPUPMENUITEM** que tem o bit de **\_ Popup mfr** definido no membro **ResInfo** será seguida por uma estrutura [**MENUHELPID**](menuhelpid.md) mais um número adicional de estruturas **POPUPMENUITEM** , uma para cada item de menu nesse submenu. A última estrutura **POPUPMENUITEM** no submenu terá o bit de **\_ término mfr** definido no membro **resInfo** . Para localizar o fim do recurso, procure uma **\_ extremidade mfr** correspondente para cada **\_ pop-up mfr** , além de **uma \_ extremidade** adicional de Mfr que corresponda ao conjunto mais externo de itens de menu.

Indique o último item de menu definindo o membro de **tipo** para o **\_ fim de MF**. Como você pode aninhar submenus, pode haver vários níveis de **\_ fim de MF**. Nesses casos, os itens de menu são sequenciais.

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

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

