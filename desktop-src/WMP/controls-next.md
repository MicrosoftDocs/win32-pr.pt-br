---
title: Método Controls. Next
description: O método Next define o item atual para o próximo item na lista de reprodução.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- Windows Media Player do próximo método
- método next Windows Media Player, classe Controls
- controla a classe Windows Media Player, o próximo método
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a40c063163b0dadaa3db2d0d6281ace64312f68ee999763e6b27d4bd98f84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997466"
---
# <a name="controlsnext-method"></a>Método Controls. Next

O método **Next** define o item atual para o próximo item na lista de reprodução.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.next()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a lista de reprodução estiver na última entrada quando o **próximo** for invocado, a primeira entrada da lista de reprodução se tornará a atual.

Para listas de reprodução do lado do servidor, esse método pula para o próximo item na lista de reprodução do lado do servidor, não a lista de reprodução do cliente.

Ao reproduzir um DVD, esse método pula para o próximo capítulo lógico na sequência de reprodução, que pode não ser o próximo capítulo da lista de reprodução. Ao reproduzir o DVD ainda, esse método pula para o próximo ainda.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que usa **Next** para mover para o próximo item na playlist atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controles. Previous**](controls-previous.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> </dl>

 

 





