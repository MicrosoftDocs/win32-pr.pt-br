---
title: Estrutura MENUHEADER
description: Contém informações de versão para o recurso de menu. A definição de estrutura fornecida aqui é apenas para explicação; ele não está presente em nenhum arquivo de header padrão.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- MENUHEADER structure Menus and Other Resources
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e78b577d52f0e40737f90186903aff9bfe2470d7050eac1ee00bc79ca7f596f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972005"
---
# <a name="menuheader-structure"></a>Estrutura MENUHEADER

Contém informações de versão para o recurso de menu. A definição de estrutura fornecida aqui é apenas para explicação; ele não está presente em nenhum arquivo de header padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Wversion**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O número de versão do modelo de menu. Esse membro deve ser igual a zero para indicar que esse é um [**\_ MENU RT**](/windows/desktop/menurc/resource-types) criado com um modelo de menu padrão.

</dd> <dt>

**cbHeaderSize**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O tamanho do header do modelo de menu. Esse valor é zero para menus que você cria com um modelo de menu padrão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**HEADER \_ DO MODELO MENUEX \_**](menuex-template-header.md)
</dt> <dt>

[**ITEM DE MODELO \_ MENUEX \_**](menuex-template-item.md)
</dt> <dt>

[**Menuitemtemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

