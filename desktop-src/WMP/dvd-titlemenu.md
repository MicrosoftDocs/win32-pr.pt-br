---
title: Método DVD. titleMenu
description: O método titleMenu interrompe a reprodução do título e exibe o menu título.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- método titleMenu Windows Media Player
- método titleMenu Windows Media Player, classe de DVD
- Classe DVD Windows Media Player, método titleMenu
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
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295766"
---
# <a name="dvdtitlemenu-method"></a>Método DVD. titleMenu

O método **titleMenu** interrompe a reprodução do título e exibe o menu título.

## <a name="syntax"></a>Sintaxe


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada DVD é criado de maneira diferente. O DVD deve conter um menu para que esse método funcione. Alguns DVDs são criados para que os métodos **topMenu** e **titleMenu** Abram o mesmo menu. O método **titleMenu** geralmente invoca o menu de título, mas ele pode invocar o menu superior, se não houver nenhum menu de título disponível.

**Windows Media Player 10 Mobile:** Esse método sempre tem sucesso, mas não executa a operação pretendida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Versão<br/>                  | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> <dt>

[**DVD. topMenu**](dvd-topmenu.md)
</dt> </dl>

 

 





