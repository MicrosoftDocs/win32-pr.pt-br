---
title: Estrutura NORMALMENUITEM
description: Contém informações sobre cada item em um recurso de menu que não abre um menu ou um submenu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menus de estrutura NORMALMENUITEM e outros recursos
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294787"
---
# <a name="normalmenuitem-structure"></a>Estrutura NORMALMENUITEM

Contém informações sobre cada item em um recurso de menu que não abre um menu ou um submenu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a>Membros

<dl> <dt>

**resInfo**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tipo de item de menu. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                       | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**Mfr \_ ENCERRAR**</dt> <dt>0x80</dt> </dl>       | O item de menu é o último neste submenu ou recurso de menu; Esse sinalizador é usado internamente pelo sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**Mfr \_ POPUP**</dt> <dt>0x01</dt> </dl> | O item de menu abre um menu ou um submenu; o sinalizador é usado internamente pelo sistema. <br/>                    |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que contém o texto para este item de menu. Não há nenhum limite fixo para o tamanho dessa cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Há uma estrutura **NORMALMENUITEM** para cada item de menu que não abre um menu ou um submenu. Indique o último item de menu em um menu definindo o membro **resInfo** como **mfr \_ end**.

Um separador de menu é um tipo especial de item de menu que está inativo, mas aparece como uma barra de divisão entre dois itens de menu ativos. Indique um separador de menu deixando o membro **menuText** vazio.

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

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





