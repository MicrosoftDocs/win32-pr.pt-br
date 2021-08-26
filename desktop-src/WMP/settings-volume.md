---
title: Configurações.volume
description: A propriedade de volume especifica ou recupera o volume atual.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Configurações.volume Windows Media Player
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
ms.openlocfilehash: 1c02952426a78323421fd779b253136c1777d509141d51b590b9db40c4d077a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002206"
---
# <a name="settingsvolume"></a>Configurações.volume

A **propriedade de** volume especifica ou recupera o volume atual.

## <a name="syntax"></a>Syntax

player.settings.volume

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um  número de leitura/gravação (**longo**) que varia de 0 a 100.

## <a name="remarks"></a>Comentários

Zero não especifica nenhum volume e 100 especifica o volume completo. Se nenhum valor for especificado para essa propriedade, o padrão será a última configuração de volume estabelecida para o player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> </dl>

 

 





