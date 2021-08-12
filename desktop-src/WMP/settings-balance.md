---
title: Configurações.balance
description: A propriedade balance especifica ou recupera o saldo estéreo atual.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Configurações.balance Windows Media Player
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e569c40214655fc643762da8580bd8d6a16e098b99c649bb27e1a1485d498931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569571"
---
# <a name="settingsbalance"></a>Configurações.balance

A **propriedade** balance especifica ou recupera o saldo estéreo atual.

## <a name="syntax"></a>Sintaxe

player.settings.balance

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um número de **leitura/gravação** (**longo).** Os valores variam de 100 a 100, com um valor padrão de zero.

## <a name="remarks"></a>Comentários

O valor zero indica que o áudio é reproduzindo em volume igual nos canais esquerdo e direito. Um valor de 100 indica que o áudio é reproduzindo somente no canal esquerdo. Um valor de 100 indica que o áudio é reproduzindo somente no canal direito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> </dl>

 

 





