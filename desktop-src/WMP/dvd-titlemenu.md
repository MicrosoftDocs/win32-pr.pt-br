---
title: Método DVD.titleMenu
description: O método titleMenu interrompe a reprodução de título e exibe o menu de título.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- Método titleMenu Windows Media Player
- Método titleMenu Windows Media Player , classe DVD
- Classe dvd Windows Media Player , método titleMenu
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1954ea52d5a67dc502278c7f1e821a06c4e2b849dc4040e690275b6d1b0ef0bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996876"
---
# <a name="dvdtitlemenu-method"></a>Método DVD.titleMenu

O **método titleMenu** interrompe a reprodução de título e exibe o menu de título.

## <a name="syntax"></a>Sintaxe


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada DVD é gravado de forma diferente. O DVD deve conter um menu para que esse método funcione. Alguns DVDs são autores para que os **métodos topMenu** e **titleMenu** abram o mesmo menu. O **método titleMenu** geralmente invoca o menu de título, mas pode invocar o menu superior em vez disso, se não houver nenhum menu de título disponível.

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

[**DVD.topMenu**](dvd-topmenu.md)
</dt> </dl>

 

 





