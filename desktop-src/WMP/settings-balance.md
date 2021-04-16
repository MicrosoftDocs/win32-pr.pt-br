---
title: Configurações. saldo
description: A propriedade Balance especifica ou recupera o saldo estéreo atual.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Configurações. balancear o Windows Media Player
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
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747899"
---
# <a name="settingsbalance"></a>Configurações. saldo

A propriedade **Balance** especifica ou recupera o saldo estéreo atual.

## <a name="syntax"></a>Syntax

Player. Settings. Balance

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** de leitura/gravação (**longo**). Os valores variam de 100 a 100, com um valor padrão de zero.

## <a name="remarks"></a>Comentários

O valor zero indica que o áudio é reproduzido em um volume igual nos canais esquerdo e direito. Um valor de 100 indica que o áudio é reproduzido somente no canal à esquerda. Um valor de 100 indica que o áudio é reproduzido somente no canal correto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> </dl>

 

 





