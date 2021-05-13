---
description: Contém informações que o Gerenciador de Arquivos usa para adicionar um menu personalizado fornecido por uma DLL de extensão do Gerenciador de Arquivos. A estrutura também fornece um valor delta que a DLL de extensão pode usar para manipular o menu personalizado depois que o Gerenciador de Arquivos carregar o menu.
title: FMS_LOAD estrutura (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842187"
---
# <a name="fms_load-structure"></a>Estrutura FMS \_ LOAD

Contém informações que o Gerenciador de Arquivos usa para adicionar um menu personalizado fornecido por uma DLL de extensão do Gerenciador de Arquivos. A estrutura também fornece um valor delta que a DLL de extensão pode usar para manipular o menu personalizado depois que o Gerenciador de Arquivos carregar o menu.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwsize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O comprimento, em bytes, da estrutura.

</dd> <dt>

**szMenuName**
</dt> <dd>

Tipo: **LEN DE TEXTO DO \[ MENU \_ \_ \] TCHAR**

</dd> <dd>

Um nome terminado em nulo para um item de menu que aparece na barra de menus no Gerenciador de Arquivos.

</dd> <dt>

**Hmenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

O identificador do menu pop-up adicionado à barra de menus no Gerenciador de Arquivos.

</dd> <dt>

**wMenuDelta**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

O valor delta do item de menu. Para evitar conflitos com seus próprios itens de menu, o Gerenciador de Arquivos renumera os identificadores de item de menu no menu pop-up identificado pelo membro **hMenu** adicionando esse valor delta a cada identificador. Uma DLL de extensão que deve modificar um item de menu deve identificar o item adicionando o valor delta ao identificador do item de menu. O valor desse membro pode variar de uma sessão para uma sessão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




