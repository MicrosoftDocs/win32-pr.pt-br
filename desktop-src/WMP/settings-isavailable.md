---
title: Configurações. isavailable
description: A propriedade IsAvailable indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada. | Configurações. isavailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Configurações. isavailable Windows Media Player
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
ms.openlocfilehash: df10026007dd9e04fe88d634a3da566074b0d6a88420ef444d5f2bae39a793fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002396"
---
# <a name="settingsisavailable"></a>Configurações. isavailable

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

[**Configurações Objeto**](settings-object.md)
</dt> </dl>

 

 





