---
title: Propriedades, métodos e eventos
description: Propriedades, métodos e eventos
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player, propriedades do modelo de objeto
- Windows Media Player, métodos para o modelo de objeto
- Windows Media Player, eventos para o modelo de objeto
- modelo de objeto Windows Media Player, propriedades
- modelo de objeto Windows Media Player, métodos
- modelo de objeto Windows Media Player, eventos
- modelo de objeto, propriedades
- modelo de objeto, métodos
- modelo de objeto, eventos
- Windows Media Player ActiveX controle, propriedades do modelo de objeto
- controle de ActiveX, propriedades do modelo de objeto
- Windows Media Player controle de ActiveX móvel, propriedades do modelo de objeto
- Windows Media Player Móvel, propriedades do modelo de objeto
- Windows Media Player ActiveX controle, métodos para o modelo de objeto
- controle de ActiveX, métodos para o modelo de objeto
- Windows Media Player controle de ActiveX móvel, métodos para modelo de objeto
- Windows Media Player Móvel, métodos para modelo de objeto
- Windows Media Player controle de ActiveX, eventos para o modelo de objeto
- ActiveX controle, eventos para o modelo de objeto
- Windows Media Player controle de ActiveX móvel, eventos para o modelo de objeto
- Windows Media Player Dispositivos móveis, eventos para o modelo de objeto
- propriedades, modelo de objeto Windows Media Player
- métodos, Windows Media Player modelo de objeto
- eventos, Windows Media Player modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcc07977bc7ddcd2dd162600d4fa3d2822a3f52f38983ea8427f89d9403ecf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571080"
---
# <a name="properties-methods-and-events"></a>Propriedades, métodos e eventos

cada objeto tem métodos e propriedades por meio dos quais você pode programar o controle de Windows Media Player. Um método é uma ação que o objeto pode tomar. Uma propriedade é um valor de dados que você pode ler ou alterar. Por exemplo, o método **Play** inicia o conteúdo que está sendo reproduzido e **a propriedade** ratename indica a taxa de quadros atual do conteúdo que está sendo reproduzido.

Além disso, o objeto **Player** gera eventos que oferecem a oportunidade de executar ações em momentos específicos. você escreve o código em um manipulador de eventos que será executado quando Windows Media Player gerar o evento correspondente. Por exemplo, você pode escrever código em um manipulador de eventos **PlayStateChange** que determina se a alteração no estado é que a mídia foi encerrada e, em caso afirmativo, exibe uma caixa de diálogo perguntando os usuários se eles desejam reproduzir a mídia novamente.

> [!Note]  
> todos os métodos no modelo de objeto Windows Media Player são assíncronos. Se você chamar dois métodos no mesmo procedimento, o segundo método não poderá confiar no primeiro método que concluiu sua ação.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




