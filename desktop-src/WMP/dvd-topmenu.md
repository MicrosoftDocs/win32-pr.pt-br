---
title: Método DVD. topMenu
description: O método topMenu interrompe a reprodução do título e exibe o menu superior (ou raiz) do título atual.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- método topMenu Windows Media Player
- método topMenu Windows Media Player, classe de DVD
- Classe DVD Windows Media Player, método topMenu
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
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455367"
---
# <a name="dvdtopmenu-method"></a>Método DVD. topMenu

O método **topMenu** interrompe a reprodução do título e exibe o menu superior (ou raiz) do título atual.

## <a name="syntax"></a>Sintaxe


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada DVD é criado de maneira diferente. O DVD deve conter um menu para que esse método funcione. Alguns DVDs são criados para que os métodos **topMenu** e **titleMenu** Abram o mesmo menu. O método **topMenu** geralmente invoca o menu superior (ou raiz), mas ele pode invocar o menu de título, se não houver nenhum menu raiz disponível.

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

[**DVD. titleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





