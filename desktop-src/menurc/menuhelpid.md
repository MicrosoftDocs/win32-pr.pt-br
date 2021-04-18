---
title: Estrutura MENUHELPID
description: Contém os dados finais gravados no \_ recurso de menu RT para um menu ou submenu se o membro resInfo da estrutura POPUPMENUITEM for definido como \_ Popup mfr.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menus de estrutura MENUHELPID e outros recursos
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750884"
---
# <a name="menuhelpid-structure"></a>Estrutura MENUHELPID

Contém os dados finais gravados no recurso de [**\_ menu RT**](/windows/desktop/menurc/resource-types) para um menu ou submenu se o membro **resInfo** da estrutura [**POPUPMENUITEM**](popupmenuitem.md) for definido como **\_ Popup mfr**. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a>Membros

<dl> <dt>

**HelpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O identificador usado para identificar o menu durante o processamento da [**\_ ajuda do WM**](/windows/desktop/shell/wm-help) .

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

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

