---
title: Usando capas com o controle do Windows Media Player
description: Usando capas com o controle do Windows Media Player
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, C++
- Modelo de objeto do Windows Media Player, C++
- modelo de objeto, C++
- Windows Media Player Mobile, C++
- Controle ActiveX do Windows Media Player, C++
- Controle ActiveX móvel do Windows Media Player, C++
- Controle ActiveX, C++
- Incorporação de programa C++
- incorporando, programas em C++
- Controle ActiveX do Windows Media Player, capas
- Controle ActiveX móvel do Windows Media Player, capas
- Controle ActiveX, capas
- capas, incorporando controle ActiveX
- Capas do Windows Media Player, incorporando controle ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159850"
---
# <a name="using-skins-with-the-windows-media-player-control"></a>Usando capas com o controle do Windows Media Player

Ao inserir o controle do Windows Media Player em um programa C++, você pode personalizar a interface do usuário do Player aplicando um arquivo de definição de capa a ele. Um arquivo de definição de capa é um documento baseado em XML que especifica o layout de componentes de interface do usuário padrão e personalizáveis e quaisquer elementos gráficos que o acompanham. Usando o Microsoft JScript, você pode especificar o comportamento desses componentes e manipular o controle do Windows Media Player sem a sobrecarga da sintaxe de C++ e COM.

As capas fornecem uma maneira fácil de manter o código de interface do usuário e o código do programa principal separados para que possam ser mantidos e desenvolvidos de forma independente. Você também pode reutilizar as capas originalmente projetadas para uso pelo Player autônomo no modo de capa. O código de capa que você cria especificamente para programas C++ pode interagir com seus programas por meio de um objeto programável que seu programa pode fornecer.

Para habilitar o modo de capa para o controle do Windows Media Player, o programa deve implementar a interface **IWMPRemoteMediaServices** . Embora você possa usar as capas com o controle e o controle remoto ao mesmo tempo, você pode usar essa interface para habilitar qualquer recurso sem habilitar o outro. Para desabilitar a comunicação remota, basta passar um valor de "local" como o parâmetro out do método **Getservicetype** e retornar um HRESULT de E \_ NOTIMPL do método **getApplicationName** .

Para alternar o controle do Windows Media Player para o modo de capa, chame o método **IWMPPlayer::p UT \_ UIMODE** , passando um valor de "Custom". Especifique o caminho e o nome de arquivo do arquivo de definição de capa a ser usado, retornando-o do método **IWMPRemoteMediaServices:: GetCustomUIMode** .

Se você quiser fornecer um objeto programável para comunicação entre sua capa e seu programa, passe um nome e um ponteiro para um ponteiro **IDispatch** como os dois parâmetros de saída do método **IWMPRemoteMediaServices:: GetScriptableObject** . Em seguida, sua capa pode fazer chamadas para o objeto programável usando o nome especificado como se fosse um atributo global semelhante ao atributo global do **Player** .

Uma capa aplicada a um controle remoto do Windows Media Player pode acessar o objeto **PlayerApplication** usando outro atributo global chamado **PlayerApplication**. Como a propriedade **Player. playerApplication** não pode ser acessada por capas, você deve usar esse atributo global quando desejar que o código de sua capa gerencie o encaixe e desencaixe.

## <a name="samples"></a>Exemplos

O pacote de instalação do SDK do Windows Media Player instala um exemplo que demonstra a aplicação de uma capa ao controle do Windows Media Player. Consulte o exemplo de RemoteSkin para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos**](samples.md)
</dt> <dt>

[**Usando o controle do Windows Media Player em um programa C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




