---
title: Settings. DefaultFrame
description: A propriedade DefaultFrame especifica ou recupera o nome do quadro usado para exibir uma URL recebida em um evento ScriptCommand.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Settings. DefaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751778"
---
# <a name="settingsdefaultframe"></a>Settings. DefaultFrame

A propriedade **DefaultFrame** especifica ou recupera o nome do quadro usado para exibir uma URL recebida em um evento **ScriptCommand** .

## <a name="syntax"></a>Syntax

Player. Settings. DefaultFrame

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** de leitura/gravação correspondente ao valor do atributo **Name** do elemento de quadro de destino.

## <a name="remarks"></a>Comentários

Se um quadro de destino for especificado no próprio evento **ScriptCommand** , essa propriedade será ignorada.

Essa propriedade é ignorada ao usar o miniaplicativo Java do Netscape Navigator. No navegador, cada comando de script de URL recebido exibe a URL em uma nova janela do navegador, independentemente do valor das *configurações*. **DefaultFrame**.

**Windows Media Player 10 Mobile**: essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento Player. ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> <dt>

[**Uso do Windows Media Player com o Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





