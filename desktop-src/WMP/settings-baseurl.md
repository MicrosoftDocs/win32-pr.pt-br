---
title: Settings. baseURL
description: A propriedade baseURL especifica ou recupera a URL base usada para a resolução de caminho relativa com comandos de script de URL inseridos em itens de mídia.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Settings. baseURL Windows Media Player
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748708"
---
# <a name="settingsbaseurl"></a>Settings. baseURL

A propriedade **baseURL** especifica ou recupera a URL base usada para a resolução de caminho relativa com comandos de script de URL inseridos em itens de mídia.

## <a name="syntax"></a>Syntax

Player. Settings. baseURL

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Essa propriedade especifica a URL HTTP base que é passada como o parâmetro de comando pelo evento **ScriptCommand** . A URL base é concatenada com a URL relativa da seguinte maneira:

1.  Uma barra (/) à direita é adicionada ao valor da propriedade **baseURL** .
2.  Um período à esquerda, uma barra invertida ou uma barra (., \\ e/) são excluídos da URL relativa.
3.  A URL relativa é adicionada ao final da URL base.
4.  Todas as barras na URL totalmente qualificada resultante são apontadas na mesma direção (convertida para barras para frente ou para trás) com base na direção do caractere de primeira barra encontrado na nova URL.

**Observação**

O controle de jogador não dá suporte ao uso de dois pontos (..) na URL relativa para indicar o pai do local atual.

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
</dt> </dl>

 

 





