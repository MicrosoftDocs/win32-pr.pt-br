---
title: Instrução filestyle
description: Define os estilos de janela estendidos para uma caixa de diálogo. Em uma definição de recurso, a instrução filestyle é colocada com as instruções opcionais antes do início do corpo da definição de recurso.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Menus de instruções do filestyle e outros recursos
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454014"
---
# <a name="exstyle-statement"></a>Instrução filestyle

Define os estilos de janela estendidos para uma caixa de diálogo. Em uma definição de recurso, a instrução **filestyle** é colocada com as instruções opcionais antes do início do corpo da definição de recurso.

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo estendido*
</dt> <dd>

Estilo de janela estendida para a caixa de diálogo ou controle. Para obter uma lista de estilos de janela estendidos, consulte [**estilos de janela estendidos**](/windows/desktop/winmsg/extended-window-styles).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para controles, os estilos estendidos são especificados após a opção de *estilo* na instrução Control Resource-Definition. Para obter mais informações, consulte a instrução de definição de recurso para o controle individual.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CONTROLO**](control-control.md)
</dt> <dt>

[**'**](dialog-resource.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**POP-up**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[Recurso definido pelo usuário](user-defined-resource.md)
</dt> </dl>

 

 