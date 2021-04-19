---
title: Estrutura MENUHEADER
description: Contém informações de versão para o recurso de menu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menus de estrutura MENUHEADER e outros recursos
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749346"
---
# <a name="menuheader-structure"></a>Estrutura MENUHEADER

Contém informações de versão para o recurso de menu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**wVersion**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de versão do modelo de menu. Esse membro deve ser igual a zero para indicar que este é um [**\_ menu de RT**](/windows/desktop/menurc/resource-types) criado com um modelo de menu padrão.

</dd> <dt>

**cbHeaderSize**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tamanho do cabeçalho do modelo de menu. Esse valor é zero para os menus que você criar com um modelo de menu padrão.

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

[**\_cabeçalho do modelo MENUEX \_**](menuex-template-header.md)
</dt> <dt>

[**\_item de modelo MENUEX \_**](menuex-template-item.md)
</dt> <dt>

[**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

