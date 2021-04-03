---
title: Propriedades, métodos e eventos
description: Propriedades, métodos e eventos
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player, propriedades do modelo de objeto
- Windows Media Player, métodos para modelo de objeto
- Windows Media Player, eventos para modelo de objeto
- Modelo de objeto do Windows Media Player, propriedades
- Modelo de objeto do Windows Media Player, métodos
- Modelo de objeto do Windows Media Player, eventos
- modelo de objeto, propriedades
- modelo de objeto, métodos
- modelo de objeto, eventos
- Controle ActiveX do Windows Media Player, propriedades do modelo de objeto
- Controle ActiveX, propriedades do modelo de objeto
- Controle ActiveX móvel do Windows Media Player, propriedades do modelo de objeto
- Windows Media Player Mobile, propriedades para modelo de objeto
- Controle ActiveX do Windows Media Player, métodos para modelo de objeto
- Controle ActiveX, métodos para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, métodos para modelo de objeto
- Windows Media Player Mobile, métodos para modelo de objeto
- Controle ActiveX do Windows Media Player, eventos para modelo de objeto
- Controle ActiveX, eventos para o modelo de objeto
- Controle ActiveX móvel do Windows Media Player, eventos para modelo de objeto
- Windows Media Player Mobile, eventos para modelo de objeto
- Propriedades, modelo de objeto do Windows Media Player
- métodos, modelo de objeto do Windows Media Player
- eventos, modelo de objeto do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084087"
---
# <a name="properties-methods-and-events"></a>Propriedades, métodos e eventos

Cada objeto tem métodos e propriedades por meio dos quais você pode programar o controle do Windows Media Player. Um método é uma ação que o objeto pode tomar. Uma propriedade é um valor de dados que você pode ler ou alterar. Por exemplo, o método **Play** inicia o conteúdo que está sendo reproduzido e **a propriedade** ratename indica a taxa de quadros atual do conteúdo que está sendo reproduzido.

Além disso, o objeto **Player** gera eventos que oferecem a oportunidade de executar ações em momentos específicos. Você escreve o código em um manipulador de eventos que será executado quando o Windows Media Player gerar o evento correspondente. Por exemplo, você pode escrever código em um manipulador de eventos **PlayStateChange** que determina se a alteração no estado é que a mídia foi encerrada e, em caso afirmativo, exibe uma caixa de diálogo perguntando os usuários se eles desejam reproduzir a mídia novamente.

> [!Note]  
> Todos os métodos no modelo de objeto do Windows Media Player são assíncronos. Se você chamar dois métodos no mesmo procedimento, o segundo método não poderá confiar no primeiro método que concluiu sua ação.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




