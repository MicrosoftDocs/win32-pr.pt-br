---
title: Estrutura de MENUEX_TEMPLATE_HEADER
description: Define o cabeçalho de um modelo de menu estendido. Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER de menus de estrutura e outros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105798539"
---
# <a name="menuex_template_header-structure"></a>Estrutura de cabeçalho do \_ modelo MENUEX \_

Define o cabeçalho de um modelo de menu estendido. Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**wVersion**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de versão do modelo. Esse membro deve ser 1 para modelos de menu estendidos.

</dd> <dt>

**wOffset**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O deslocamento para a primeira estrutura de [**\_ \_ item de modelo MENUEX**](menuex-template-item.md) , em relação ao final deste membro da estrutura. Se a primeira definição de item imediatamente seguir o membro **dwHelpId** , esse membro deverá ser 4.

</dd> <dt>

**dwHelpId**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O identificador da ajuda da barra de menus.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um modelo de menu estendido consiste em uma estrutura de **\_ \_ cabeçalho de modelo MENUEX** seguida por uma ou mais estruturas de [**\_ \_ item de modelo MENUEX**](menuex-template-item.md) contíguas. As estruturas de **\_ \_ item de modelo MENUEX** , que são variáveis de comprimento, são alinhadas nos limites **DWORD** . Para criar um menu a partir de um modelo de menu estendido na memória, use a função [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**\_item de modelo MENUEX \_**](menuex-template-item.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

 





