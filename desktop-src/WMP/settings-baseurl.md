---
title: Configurações.baseURL
description: A propriedade baseURL especifica ou recupera a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos em itens de mídia.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Configurações.baseURL Windows Media Player
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
ms.openlocfilehash: 69e06275a3028df6b90d25665e11aab3c2a0961dfa6c525cde0636434f06986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995376"
---
# <a name="settingsbaseurl"></a>Configurações.baseURL

A **propriedade baseURL** especifica ou recupera a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos em itens de mídia.

## <a name="syntax"></a>Syntax

player.settings.baseURL

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Essa propriedade especifica a URL HTTP base que é passada como o parâmetro de comando pelo **evento ScriptCommand.** A URL base é concatenada com a URL relativa da seguinte forma:

1.  Uma barra (/) à frente à frente é adicionada ao valor da **propriedade baseURL.**
2.  Um ponto à frente, barra inotrógrada ou barra (., e /) são \\ excluídos da URL relativa.
3.  A URL relativa é adicionada ao final da URL base.
4.  Todas as barras na URL totalmente qualificada resultante são apontadas na mesma direção (convertidas em barras para frente ou para trás) com base na direção do primeiro caractere de barramento encontrado na nova URL.

**Observação**

O controle de player não dá suporte ao uso de dois pontos (..) na URL relativa para indicar o pai do local atual.

**Windows Media Player 10 Mobile:** essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento Player.ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> </dl>

 

 





