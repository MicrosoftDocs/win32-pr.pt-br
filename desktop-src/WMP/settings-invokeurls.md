---
title: Settings. invokeURLs
description: A propriedade invokeURLs especifica ou recupera um valor que indica se os eventos de URL devem iniciar um navegador da Web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Settings. invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747481"
---
# <a name="settingsinvokeurls"></a>Settings. invokeURLs

A propriedade **invokeURLs** especifica ou recupera um valor que indica se os eventos de URL devem iniciar um navegador da Web.

## <a name="syntax"></a>Syntax

Player. Settings. invokeURLs

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** de leitura/gravação.



| Valor | Descrição                                  |
|-------|----------------------------------------------|
| true  | Padrão. Os eventos de URL devem iniciar um navegador. |
| false | Os eventos de URL não devem iniciar um navegador.      |



 

## <a name="remarks"></a>Comentários

Os arquivos de mídia podem conter URLs. Quando uma URL é enviada ao controle do Windows Media Player, ela é passada primeiro para o manipulador de eventos **ScriptCommand** , independentemente do valor em **invokeURLs**. Após o **ScriptCommand** sair, o Windows Media Player verifica o **invokeURLs** para determinar se o navegador da Internet padrão deve ser iniciado com a URL. Você pode exibir URLs seletivamente, verificando-as em **ScriptCommand** e configurando **invokeURLs** conforme desejado.

**Windows Media Player 10 Mobile**: essa propriedade só aceita ou retorna false.

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

 

 





