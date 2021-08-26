---
title: Configurações. invokeURLs
description: A propriedade invokeURLs especifica ou recupera um valor que indica se os eventos de URL devem iniciar um navegador da Web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Configurações. invokeURLs Windows Media Player
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
ms.openlocfilehash: 75de25c5b4a18b6d53423657dc7180fe58cb095f3244800c2c42593d1d450e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002398"
---
# <a name="settingsinvokeurls"></a>Configurações. invokeURLs

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

Os arquivos de mídia podem conter URLs. quando uma URL é enviada ao controle de Windows Media Player, ela é passada primeiro para o manipulador de eventos **ScriptCommand** , independentemente do valor em **invokeURLs**. após o **ScriptCommand** sair, o Windows Media Player verifica **invokeURLs** para determinar se o navegador da Internet padrão deve ser iniciado com a URL. Você pode exibir URLs seletivamente, verificando-as em **ScriptCommand** e configurando **invokeURLs** conforme desejado.

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

[**Configurações Objeto**](settings-object.md)
</dt> </dl>

 

 





