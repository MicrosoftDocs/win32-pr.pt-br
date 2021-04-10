---
title: Página da Web de exemplo incluída com o controle ActiveX Área de Trabalho Remota
description: Uma página da Web de exemplo (Default.htm) está no diretório onde Conexão Web de Área de Trabalho Remota está instalado.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec07ee86dcb5d10dc289e8095c83771ebe9a8b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292290"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Página da Web de exemplo incluída com o controle ActiveX Área de Trabalho Remota

Quando você instala o controle ActiveX Área de Trabalho Remota do Conexão Web de Área de Trabalho Remota, uma página da Web de exemplo (Default.htm) é copiada para o diretório onde Conexão Web de Área de Trabalho Remota está instalado. Essa página pode ser executada no estado em que se encontra ou personalizada para atender às necessidades de um usuário ou de uma organização.

A página da Web de exemplo deve ser instalada em um servidor de rede que executa o Windows Server e o Internet Information Server 4,0 ou posterior. Além disso, o navegador no computador cliente deve ser o Internet Explorer versão 4,0 ou posterior. Para obter mais informações, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

Default.htm é uma página da Web de logon padrão que coleta informações de conexão do usuário. A página de logon contém um campo obrigatório no qual o usuário insere o nome do servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) ou o computador remoto ao qual se conectar. A página de logon também inclui campos opcionais para o tamanho da tela e informações de logon do usuário, incluindo o nome de usuário e o domínio.

Depois de coletar os dados do usuário, Default.htm os passa para o controle ActiveX Área de Trabalho Remota (Msrdp. ocx) para iniciar uma sessão de área de trabalho remota. As etapas envolvidas no início da sessão são as seguintes:

1.  Se necessário, o Internet Explorer baixa o arquivo. cab e o instala no computador do usuário.
2.  O usuário insere o nome de domínio totalmente qualificado ou o endereço IP do computador remoto no campo apropriado.

    -   Opcionalmente, o usuário pode especificar um tamanho de tela para a conexão. Se o usuário não especificar um tamanho de tela, a sessão será aberta no modo de tela inteira se o usuário estiver em uma zona de segurança de URL confiável. Caso contrário, a sessão será aberta no modo de janela.
    -   Opcionalmente, o usuário pode fornecer informações de logon automáticos (nome de usuário, domínio) para a sessão remota.

3.  Quando o usuário clica no botão **conectar** , Default.htm passa os dados fornecidos pelo usuário como parâmetros para o controle ActiveX área de trabalho remota.
4.  A área de trabalho remota é aberta na janela do navegador ou no modo de tela inteira, conforme especificado pelo usuário.

Quando Default.htm é aberto pela primeira vez usando o Internet Explorer, uma caixa de diálogo é exibida dando ao usuário a opção de baixar o controle ActiveX Área de Trabalho Remota (Msrdp. ocx). A caixa de diálogo aparece sob as seguintes condições:

-   O computador que acessou a página da Web não tem uma instalação completa do cliente do Conexão Web de Área de Trabalho Remota (ou do Serviços de Área de Trabalho Remota Cliente Avançado) com o suporte da Internet.
-   A versão instalada do arquivo. cab no computador cliente é mais antiga do que a versão na página da Web Default.htm.

O tamanho da sessão de área de trabalho remota que aparece na janela do navegador é o tamanho especificado na página da Web Default.htm. Para alterar o tamanho da tela, o usuário deve se desconectar da sessão, retornar para a página da Web Default.htm e editar as informações de conexão. Se nenhum tamanho de tela for especificado, a sessão será aberta na janela do navegador no modo de tela inteira padrão. Nessa resolução, a área de trabalho remota se expande para corresponder às dimensões completas da tela do usuário e as barras de ferramentas e quadros da janela do navegador Internet Explorer não são exibidos. Assim como com o cliente de Conexão de Área de Trabalho Remota completo, o usuário pode alternar entre o modo de tela inteira e de janela pressionando a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).

Por motivos de segurança, algumas opções que estão disponíveis no Gerenciador de conexões Serviços de Área de Trabalho Remota são restritas no controle ActiveX Área de Trabalho Remota a determinadas zonas de segurança de URL do Internet Explorer. Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações sobre essas opções e sobre como especificar um programa a ser executado na conexão.

 

 




