---
title: THEME. showErrorDialog
description: O método showErrorDialog exibe a caixa de diálogo de erro padrão.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- THEME. showErrorDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813022"
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

Se **Settings. enableErrorDialogs** for false, esse método poderá ser usado para exibir programaticamente a caixa de diálogo de erro. Se não houver erros na fila de erros, a caixa de diálogo de erro não será mostrada.

Para o Windows Media Player 9 Series ou posterior, esse método deve ser chamado a partir do manipulador de eventos de erro. O Windows Media Player 9 Series ou posterior limpa a fila de erros de capas depois que o evento de erro foi acionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**Settings. enableErrorDialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





