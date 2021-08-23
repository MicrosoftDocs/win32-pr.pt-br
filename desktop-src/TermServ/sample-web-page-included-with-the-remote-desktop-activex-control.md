---
title: Página da Web de exemplo incluída com o Área de Trabalho Remota ActiveX controle
description: Uma página da Web de exemplo (Default.htm) está no diretório em que Conexão Web de Área de Trabalho Remota está instalado.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c175bafe1ebde3367c20529a6d76d7933a42f343de56216649735c942105aa65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058534"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Página da Web de exemplo incluída com o Área de Trabalho Remota ActiveX controle

Quando você instala o Área de Trabalho Remota ActiveX de Conexão Web de Área de Trabalho Remota, uma página da Web de exemplo (Default.htm) é copiada para o diretório em que Conexão Web de Área de Trabalho Remota está instalado. Essa página pode ser executado no estado em que se está ou personalizado para se adequar às necessidades de um usuário ou de uma organização.

A página da Web de exemplo deve ser instalada em um servidor Web executando o Windows Server e o Servidor de Informações da Internet 4.0 ou posterior. Além disso, o navegador no computador cliente deve ser Internet Explorer versão 4.0 ou posterior. Para obter mais informações, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

Default.htm é uma página da Web de logon padrão que coleta informações de conexão do usuário. A página de logon contém um campo obrigatório no qual o usuário inseri o nome do servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) ou computador remoto ao qual se conectar. A página de logon também inclui campos opcionais para o tamanho da tela e informações de logon do usuário, incluindo nome de usuário e domínio.

Depois de coletar os dados do usuário, Default.htm os passa para o controle Área de Trabalho Remota ActiveX (Msrdp.ocx) para iniciar uma sessão de área de trabalho remota. As etapas envolvidas no início da sessão são as seguintes:

1.  Se necessário, Internet Explorer baixa o arquivo .cab e o instala no computador do usuário.
2.  O usuário insere o nome de domínio totalmente qualificado ou o endereço IP do computador remoto no campo apropriado.

    -   Opcionalmente, o usuário pode especificar um tamanho de tela para a conexão. Se o usuário não especificar um tamanho de tela, a sessão será aberta no modo de tela inteira se o usuário estiver em uma zona de segurança de URL confiável. Caso contrário, a sessão será aberta no modo de janela.
    -   Opcionalmente, o usuário pode fornecer informações de logon automático (nome de usuário, domínio) para a sessão remota.

3.  Quando o usuário clica no botão **Conexão,** Default.htm passa os dados fornecidos pelo usuário como parâmetros para o Área de Trabalho Remota ActiveX controle.
4.  A área de trabalho remota é aberta na janela do navegador ou no modo de tela inteira, conforme especificado pelo usuário.

Quando Default.htm abre pela primeira vez usando Internet Explorer, uma caixa de diálogo é exibida, dando ao usuário a opção de baixar o controle Área de Trabalho Remota ActiveX (Msrdp.ocx). A caixa de diálogo é exibida sob as seguintes condições:

-   O computador que acessou a página da Web não tem uma instalação completa do cliente Conexão Web de Área de Trabalho Remota (ou o Serviços de Área de Trabalho Remota Cliente Avançado) com suporte da Web.
-   A versão instalada do arquivo .cab no computador cliente é mais antiga do que a versão na Default.htm web.

O tamanho da sessão da área de trabalho remota que aparece na janela do navegador é o tamanho especificado na página Default.htm Web. Para alterar o tamanho da tela, o usuário deve se desconectar da sessão, retornar à página Default.htm web e editar as informações de conexão. Se nenhum tamanho de tela tiver sido especificado, a sessão será aberta na janela do navegador no modo de tela inteira padrão. Nessa resolução, a área de trabalho remota se expande para corresponder às dimensões completas da tela do usuário e as barras de ferramentas do navegador Internet Explorer e os quadros da janela não são exibidos. Assim como com o cliente de Conexão de Área de Trabalho Remota completo, o usuário pode alternar entre a [](terminal-services-shortcut-keys.md) tela inteira e o modo de janela pressionando a combinação de teclas de atalho do modo de tela inteira (CTRL+ALT+BREAK).

Por motivos de segurança, algumas opções disponíveis no Serviços de Área de Trabalho Remota Gerenciador de Conexões são restritas no controle Área de Trabalho Remota ActiveX para determinadas zonas de segurança Internet Explorer URL. Consulte [Fornecendo segurança de cliente RDP](providing-for-rdp-client-security.md) para obter mais informações sobre essas opções e sobre como especificar um programa a ser executado após a conexão.

 

 




