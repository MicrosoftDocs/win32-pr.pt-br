---
title: Configurações. volume
description: A propriedade volume especifica ou recupera o volume atual.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Configurações. volume Windows Media Player
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752614"
---
# <a name="settingsvolume"></a>Configurações. volume

A propriedade **volume** especifica ou recupera o volume atual.

## <a name="syntax"></a>Syntax

Player. Settings. volume

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **número** de leitura/gravação (**longo**) que varia de 0 a 100.

## <a name="remarks"></a>Comentários

Zero Especifica que nenhum volume e 100 especifica o volume completo. Se nenhum valor for especificado para essa propriedade, o padrão será a última configuração de volume estabelecida para o Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> </dl>

 

 





