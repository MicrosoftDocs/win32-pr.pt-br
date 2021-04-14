---
title: Configurando o serviço de nome
description: A partir do Windows 2000, quando você instala o SDK do Windows, o programa de instalação seleciona automaticamente o Microsoft Locator como o provedor de serviços de nome. Você pode alterar o nome provedor de serviços por meio do painel de controle.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453593"
---
# <a name="configuring-the-name-service"></a>Configurando o serviço de nome

A partir do Windows 2000, quando você instala o SDK do Windows, o programa de instalação seleciona automaticamente o Microsoft Locator como o provedor de serviços de nome. Você pode alterar o nome provedor de serviços por meio do painel de controle.

O computador host que executa o nsid atua como um gateway para o serviço de diretório de célula do DCE, passando chamadas de função de NSI entre computadores que executam sistemas operacionais da Microsoft e computadores DCE. Um endereço de rede pode ter até 80 caracteres — por exemplo, 11.1.9.169 é um endereço válido.

> [!Note]  
> Você deve ter o produto Digital Equipment Corporation DCE CDS para configurar os CDS do DCE como seu provedor de serviços de nome. Consulte a documentação fornecida pela Digital Equipment Corporation para obter informações sobre os CDS da DCE.

 

**Para reconfigurar o provedor de serviços de nome**

1.  No painel de controle, clique no ícone **conexões de rede** . A janela **conexões de rede** é exibida.
2.  Selecione a conexão de rede a ser configurada, clique com o botão direito do mouse e selecione **Propriedades** no menu de contexto. A caixa de diálogo **Propriedades da conexão** é exibida.
3.  Na caixa de diálogo **Propriedades da conexão** , selecione **cliente para redes Microsoft** e clique no botão **Propriedades** . A caixa de diálogo **cliente para propriedades de rede da Microsoft** é exibida.
4.  Na caixa **de diálogo cliente para propriedades de rede da Microsoft** , abra a lista suspensa **provedor de serviços de nome** e selecione um provedor de nomes na listagem.
    1.  Ao selecionar Microsoft Locator, clique em OK. O processo de configuração é concluído.
    2.  Ao selecionar o serviço de diretório de célula do DCE, na caixa **endereço de rede** , digite o nome do computador host que executa o daemon NSI (nsid) e clique em OK.

**Para reconfigurar o provedor de serviços de nome para o Windows 2000**

1.  No painel de controle, clique no ícone de **rede** .

    A caixa de diálogo **rede** é exibida.

2.  Na caixa de diálogo **rede** , clique em **Configurar**.
3.  Na lista **NetworkSoftware** , selecione **configuração de RPC**.

    A caixa de diálogo **configuração do provedor de serviço de nome RPC** é exibida.

4.  Na caixa de diálogo **configuração do provedor de serviço de nome de RPC** , selecione um provedor de serviços de nome na lista.
    1.  Ao selecionar Microsoft Locator, clique em OK. O processo de configuração é concluído.
    2.  Ao selecionar o serviço de diretório de célula do DCE, na caixa **endereço de rede** , digite o nome do computador host que executa o daemon NSI (nsid) e clique em OK.

 

 




