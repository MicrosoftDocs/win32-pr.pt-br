---
title: Depurando código
description: Depurando código
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Capas do Windows Media Player, código de depuração
- capas, código de depuração
- código de depuração para capas
- Capas do Windows Media Player, registro em log
- capas, registro em log
- funcionalidade de registro em log em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292697"
---
# <a name="debugging-code"></a>Depurando código

Geralmente, você desejará ver o que está acontecendo na sua capa. Você pode fazer isso por meio de um controle de texto ou de um arquivo de log.

Você pode criar um elemento de **texto** e colocá-lo em uma parte da sua capa temporariamente. Por exemplo, você pode usar o seguinte código para criar seu elemento de **texto** :


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



Em seguida, por exemplo, se você quiser ver a posição atual do conteúdo de mídia digital no Windows Media Player, poderá usar um código semelhante ao seguinte para exibir a posição atual na caixa de texto.


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a>Para gravar informações de depuração em um arquivo de log

Para habilitar ou desabilitar a depuração, altere o valor da seguinte chave do registro:

**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**

Quando você define o valor como 1, o registro em log é habilitado. Quando você define o valor como 0 (o padrão), o registro em log é desabilitado.

Se o registro em log estiver habilitado, um arquivo será colocado no computador do usuário na mesma pasta que a capa. O arquivo será nomeado "*filename* \_ 0 \_log.txt", em que *filename* é o nome do arquivo de capa. O código em sua capa pode gravar texto nesse arquivo usando o *tema*. método **logString** . Isso pode ser útil se você quiser determinar o que está acontecendo dentro do seu código enquanto ele está em execução. Observe que o arquivo de texto é codificado com caracteres Unicode.

Quando o registro em log estiver habilitado e você tiver instalado um sistema de desenvolvimento que fornece recursos de depuração (como Microsoft Visual Studio), as exceções que não são tratadas pelo código de script farão com que uma caixa de diálogo de aviso do depurador seja aberta para cada exceção. Esse é um recurso útil para ajudá-lo a depurar seu código de script. Além disso, você pode anexar manualmente o processo do Windows Media Player ao seu depurador quando o log estiver habilitado.

Esse SDK inclui uma capa de exemplo, chamada "logging", que demonstra a funcionalidade de log em capas. Para saber mais sobre como usar os exemplos, consulte [exemplos](samples.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as capas**](about-skins.md)
</dt> </dl>

 

 




