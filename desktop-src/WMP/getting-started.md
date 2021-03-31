---
title: Introdução com o SDK do Windows Media Player
description: Introdução com o SDK do Windows Media Player
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, plug-ins
- Windows Media Player Mobile, plug-ins de interface do usuário
- Plug-ins móveis do Windows Media Player
- plug-ins, interface do usuário
- plug-ins, Windows Media Player Mobile
- plug-ins de interface do usuário, Windows Media Player Mobile
- Plug-ins de interface do usuário, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644100"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a>Introdução com o SDK do Windows Media Player

Para criar seu plug-in, primeiro você precisa instalar o Microsoft eMbedded Visual C++ 4,0 e o Visual Studio 2003. Você também deve instalar o SDK do Pocket PC 2003 ou o SDK do Smartphone 2003, que são downloads separados. Para compilar e executar o projeto, um dispositivo Pocket PC ou smartphone que executa o sistema operacional Windows Mobile 2003 Second Edition deve ser sincronizado com o computador de desenvolvimento usando o Microsoft ActiveSync® 3.7.1 ou posterior.

Como os plug-ins da interface do usuário em dispositivos Windows Mobile usam o mesmo modelo de plug-in que as versões da área de trabalho, você pode usar o assistente de plug-in do Windows Media Player como um ponto de partida ao criar um plug-in de interface do usuário em segundo plano que funcionará com o Windows Media Player 10 Mobile.

Para criar o código de plug-in da interface do usuário, faça o seguinte:

1.  Abra o Visual Studio 2003 e inicie um novo projeto no Visual C++.
2.  Selecione **Assistente de plug-in do Windows Media Player** no painel **modelos** .
3.  Nomeie o projeto NetworkPlugin e clique em **OK**.
4.  Selecione **plug-in de interface do usuário** e clique em **Avançar**.
5.  Selecione **plano de fundo** e clique em **Avançar**.
6.  Clique em **Avançar** para concluir o assistente. Se você pretende monitorar eventos com seu plug-in, você deve verificar a **escuta de eventos** antes de concluir o assistente e deve ler a documentação da interface **IWMPEvents** para descobrir quais eventos têm suporte no Windows Media Player 10 Mobile.

Agora que você criou o código de plug-in da interface do usuário, precisará criar um projeto Windows CE DLL vazio no eMbedded Visual C++ 4,0. Em seguida, copie os arquivos de origem gerados pelo Assistente para esse novo projeto para que eles sejam compilados com o compilador ARM4.

Para criar um projeto vazio

1.  Inicie um novo projeto no Visual C++ inserido e, em seguida, selecione **stone Dynamic-Link biblioteca** no painel **projetos** .
2.  Nomeie seu projeto e clique em **OK**.
3.  Verifique se **um projeto Windows CE dll vazio** está selecionado e clique em **concluir**.
4.  Clique no item de menu **projeto** .
5.  Selecione **Adicionar ao projeto** e clique em **arquivos**.
6.  Selecione os arquivos C++ que você criou com o assistente de plug-in e clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um plug-in de interface do usuário para o Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[**Interface IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




