---
title: THEME. showErrorDialog
description: O método showErrorDialog exibe a caixa de diálogo de erro padrão.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- Windows Media Player THEME. showErrorDialog
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf5affd0989f0bebf57c821b32679fcbd03b03093e9e6d66f176bb66bdbd57d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932501"
---
# <a name="themeshowerrordialog"></a>THEME. showErrorDialog

O método **showErrorDialog** exibe a caixa de diálogo de erro padrão.

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

se **Configurações. enableErrorDialogs** for false, esse método poderá ser usado para exibir programaticamente a caixa de diálogo de erro. Se não houver erros na fila de erros, a caixa de diálogo de erro não será mostrada.

para o Windows Media Player 9 Series ou posterior, esse método deve ser chamado a partir do manipulador de eventos de erro. Windows Media Player 9 Series ou posterior limpa a fila de erros para capas depois que o evento de erro foi acionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**Configurações. enableErrorDialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





