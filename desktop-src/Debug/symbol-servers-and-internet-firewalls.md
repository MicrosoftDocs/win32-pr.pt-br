---
description: Alguns sistemas usam firewalls da Internet ou servidores proxy que exigem autenticação para todo o tráfego de Internet.
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: Servidores de símbolos e firewalls da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2a85a5d0ee2d41e6ffee40bbb275155bdf1e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500804"
---
# <a name="symbol-server-and-internet-firewalls"></a>Servidores de símbolos e firewalls da Internet

Alguns sistemas usam firewalls da Internet ou servidores proxy que exigem autenticação para todo o tráfego de Internet. As versões anteriores do servidor de símbolos não podiam acessar símbolos da Internet, a menos que o sistema tenha usado um cliente de firewall que tratou a autenticação de forma transparente.

A partir do dbghelp 6,1, o servidor de símbolos dá suporte a servidores proxy que exigem essa autenticação. O servidor de símbolos usa qualquer servidor que esteja configurado como o padrão nas configurações de LAN do computador. Para encontrar isso, abra o item **Opções da Internet** no painel de controle, clique na guia **conexões** e clique em configurações da **LAN**. Isso também pode ser feito no Internet Explorer, clicando em **Opções da Internet** no menu **ferramentas** . O servidor de símbolos foi testado em várias marcas de servidores proxy usando métodos básicos e de resposta a desafio de autenticação.

Para definir um servidor proxy específico para o servidor de símbolos a ser usado, defina a \_ variável de ambiente do proxy de \_ símbolo NT \_ como o nome (ou endereço IP) do servidor proxy, seguido pelo número da porta. Separe os dois valores com dois-pontos. Por exemplo:

**definir \_ \_Proxy de símbolo NT \_ =**_myproxyserver_*_: 80_*

Ao usar o depurador do WinDbg, configure o caminho do símbolo para apontar para o repositório de símbolos que você deseja usar. A única diferença é que o sistema exibirá uma caixa de diálogo na qual você precisa inserir sua ID de usuário e senha para passar para o servidor proxy. Se você inserir informações incorretas, a caixa de diálogo será exibida novamente. Se você clicar no botão **Cancelar** , a caixa de diálogo será descartada e o servidor de símbolos será desabilitado para uso pela Internet.

Ao usar as versões mais recentes do cdb.exe ou ntsd.exe, essa funcionalidade é desativada por padrão. No entanto, você pode habilitar ou desabilitar essa funcionalidade usando o comando de extensão de "Sym" da seguinte maneira:

-   Para ativar a solicitação de ID de usuário e senha: **! Sym prompts**.
-   Para desativar a solicitação de ID de usuário e senha: **! Sym prompts**.

Se você ativar a solicitação, será necessário recarregar os símbolos com o comando. recarregar.

A API DbgHelp foi expandida para dar suporte a essas alterações. A função [**SymbolServerSetOptions**](/previous-versions//ms680676(v=vs.85)) dá suporte à \_ opção de proxy SSRVOPT. Se o parâmetro de dados for **nulo**, o proxy padrão definido nas **Opções da Internet** será usado. Caso contrário, uma cadeia de caracteres terminada em zero será passada especificando o nome e o número da porta do servidor proxy. O nome e a porta são separados por dois-pontos, da seguinte maneira: *myproxyserver*: 80. A função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) dá suporte à \_ opção SYMOPT sem \_ prompts. Isso desativa todos os prompts de validação do servidor de símbolos.

 

 
