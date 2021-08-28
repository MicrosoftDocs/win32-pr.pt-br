---
title: Método DVD.topMenu
description: O método topMenu interrompe a reprodução de título e exibe o menu superior (ou raiz) do título atual.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- Método topMenu Windows Media Player
- método topMenu Windows Media Player classe , DVD
- Classe dvd Windows Media Player , método topMenu
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6042547d26d40c620da503836de1ec15991280b17dd066cf81d32c617e85064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651156"
---
# <a name="dvdtopmenu-method"></a>Método DVD.topMenu

O **método topMenu** interrompe a reprodução de título e exibe o menu superior (ou raiz) do título atual.

## <a name="syntax"></a>Sintaxe


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada DVD é gravado de forma diferente. O DVD deve conter um menu para que esse método funcione. Alguns DVDs são autores para que os **métodos topMenu** e **titleMenu** abram o mesmo menu. O **método topMenu** geralmente invoca o menu superior (ou raiz), mas pode invocar o menu de título em vez disso, se não houver nenhum menu raiz disponível.

**Windows Media Player 10 Mobile:** Esse método sempre é bem-sucedido, mas não executa a operação pretendido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Versão<br/>                  | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DVD**](dvd-object.md)
</dt> <dt>

[**DVD.titleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





