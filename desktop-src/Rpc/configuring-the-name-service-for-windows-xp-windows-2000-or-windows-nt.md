---
title: Configurando o serviço de nome
description: A partir do Windows 2000, quando você instala o SDK do Windows, o programa de instalação seleciona automaticamente o Microsoft Locator como o provedor de serviços de nome. Você pode alterar o provedor de serviços de nome por meio Painel de Controle.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84450f4408ac0e90be04cfff7d1cbc92890cde4434969431a986e9cda378ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022436"
---
# <a name="configuring-the-name-service"></a>Configurando o serviço de nome

A partir do Windows 2000, quando você instala o SDK do Windows, o programa de instalação seleciona automaticamente o Microsoft Locator como o provedor de serviços de nome. Você pode alterar o provedor de serviços de nome por meio Painel de Controle.

O computador host que executa o nsid atua como um gateway para o Serviço de Diretório de Célula do DCE, passando chamadas de função NSI entre computadores que executam sistemas operacionais da Microsoft e computadores DCE. Um endereço de rede pode ter até 80 caracteres, por exemplo, 11.1.9.169 é um endereço válido.

> [!Note]  
> Você deve ter o produto DCE CDS da Digital Equipment Corporation para configurar o CDS do DCE como seu provedor de serviços de nome. Consulte a documentação fornecida pela Digital Equipment Corporation para obter informações sobre o DCE CDS.

 

**Para reconfigurar o provedor de serviços de nome**

1.  No Painel de Controle, clique no ícone **Conexões de** Rede. A **janela Conexões** de Rede é exibida.
2.  Selecione a conexão de rede a ser configurada, clique com o botão direito do mouse e **selecione Propriedades** no menu de contexto. A **caixa de diálogo Propriedades** da Conexão é exibida.
3.  Na caixa **de diálogo Propriedades** da Conexão, selecione Cliente para Microsoft **Networks** e clique no **botão** Propriedades. A **caixa de diálogo Cliente para Propriedades de Rede da Microsoft** é exibida.
4.  Na caixa de diálogo Propriedades de  Rede do Cliente da **Microsoft,** abra a lista de opções Nome do provedor de serviços e selecione um provedor de nomes na lista.
    1.  Ao selecionar Microsoft Locator, clique em OK. O processo de configuração é concluído.
    2.  Quando você seleciona o Serviço de  Diretório de Célula do DCE, na caixa Endereço de Rede, digite o nome do computador host que executa o daemon NSI (nsid) e clique em OK.

**Para reconfigurar o provedor de serviços de nome Windows 2000**

1.  No Painel de Controle, clique no **ícone** Rede.

    A **caixa de** diálogo Rede é exibida.

2.  Na caixa **de diálogo** Rede, clique em **Configurar**.
3.  Na lista **NetworkSoftware,** selecione **Configuração de RPC.**

    A caixa **de diálogo Configuração do Provedor de Serviços** de Nome RPC é exibida.

4.  Na caixa de diálogo Configuração do Provedor de Serviços de Nome **RPC,** selecione um provedor de serviços de nome na lista.
    1.  Ao selecionar Microsoft Locator, clique em OK. O processo de configuração é concluído.
    2.  Quando você seleciona o Serviço de  Diretório de Célula do DCE, na caixa Endereço de Rede, digite o nome do computador host que executa o daemon NSI (nsid) e clique em OK.

 

 




