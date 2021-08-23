---
title: Configurações. defaultframe
description: A propriedade DefaultFrame especifica ou recupera o nome do quadro usado para exibir uma URL recebida em um evento ScriptCommand.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Configurações. defaultframe Windows Media Player
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
ms.openlocfilehash: 0240864cd19c1a4d84c30abfc6e6b8ecb08457d26c3c660d19fc18d228b19615
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571806"
---
# <a name="settingsdefaultframe"></a>Configurações. defaultframe

A propriedade **DefaultFrame** especifica ou recupera o nome do quadro usado para exibir uma URL recebida em um evento **ScriptCommand** .

## <a name="syntax"></a>Syntax

Player. Settings. DefaultFrame

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** de leitura/gravação correspondente ao valor do atributo **Name** do elemento de quadro de destino.

## <a name="remarks"></a>Comentários

Se um quadro de destino for especificado no próprio evento **ScriptCommand** , essa propriedade será ignorada.

Essa propriedade é ignorada ao usar o miniaplicativo Java do Netscape Navigator. no navegador, cada comando de script de url recebido exibe a URL em uma nova janela do navegador, independentemente do valor de *Configurações*. **DefaultFrame**.

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

[**Configurações Objeto**](settings-object.md)
</dt> <dt>

[**Uso do Windows Media Player com o Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





