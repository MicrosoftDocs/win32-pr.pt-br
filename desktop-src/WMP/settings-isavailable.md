---
title: Settings. IsAvailable
description: A propriedade IsAvailable indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada. | Settings. IsAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Settings. isdisponível Windows Media Player
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752590"
---
# <a name="settingsisavailable"></a>Settings. IsAvailable

A propriedade **IsAvailable** indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.

## <a name="syntax"></a>Syntax

Player. Settings. IsAvailable (nome)

## <a name="parameters"></a>Parâmetros

*name*

Cadeia de caracteres que contém um dos valores a seguir.



| String             | Descrição                                                    |
|--------------------|----------------------------------------------------------------|
| AutoStart          | Determina se a propriedade AutoStart pode ser definida.          |
| Saldo            | Determina se a propriedade de saldo pode ser definida.            |
| BaseURL            | Determina se a propriedade baseURL pode ser definida.            |
| DefaultFrame       | Determina se a propriedade DefaultFrame pode ser definida.       |
| EnableErrorDialogs | Determina se a propriedade enableErrorDialogs pode ser definida. |
| GetMode            | Determina se o método GetMode pode ser chamado.           |
| InvokeURLs         | Determina se a propriedade invokeURLs pode ser definida.         |
| Mute               | Determina se a propriedade de mudo pode ser definida.               |
| PlayCount          | Determina se a propriedade playCount pode ser definida.          |
| Tarifa               | Determina se a propriedade de taxa pode ser definida.               |
| Setmode            | Determina se o método setmode pode ser chamado.           |
| Volume             | Determina se a propriedade do volume pode ser definida.             |



 

## <a name="return-values"></a>Valores de retorno

Esse método retorna um valor **booliano** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> </dl>

 

 





