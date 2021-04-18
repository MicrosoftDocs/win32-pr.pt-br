---
title: Conexão Web de Área de Trabalho Remota
description: Conexão Web de Área de Trabalho Remota é um aplicativo Web que consiste em um controle ActiveX e uma página de conexão de exemplo.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Conexão Web de Área de Trabalho Remota Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota protocolo RDP (RDP), Conexão Web de Área de Trabalho Remota visão geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bb1e8f562e3e5c47c6050f550fe3c7090446be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759026"
---
# <a name="remote-desktop-web-connection"></a>Conexão Web de Área de Trabalho Remota

Conexão Web de Área de Trabalho Remota é um aplicativo Web que consiste em um controle ActiveX e uma página de conexão de exemplo. Ao implantar Conexão Web de Área de Trabalho Remota em um servidor Web, você pode fornecer conectividade de cliente a servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e a outros computadores usando o Internet Explorer e TCP/IP.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Requisitos para Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

Lista os requisitos para um Conexão Web de Área de Trabalho Remota.

</dd> <dt>

[Canais virtuais programáveis](scriptable-virtual-channels.md)
</dt> <dd>

Descreve as alterações no modelo de programação para implementar aplicativos de canal virtual que são fornecidos pelo Cliente Avançado de serviços de terminal (TSAC).

</dd> </dl>

O material de referência para Conexão Web de Área de Trabalho Remota está incluído na seção [referência de conexão Web de área de trabalho remota](remote-desktop-web-connection-reference.md) .

Para saber mais, consulte esses tópicos:

-   [Implementando canais virtuais programáveis usando o Conexão Web de Área de Trabalho Remota](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [Inserindo o controle ActiveX Área de Trabalho Remota em uma página da Web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   [Baixando e usando o controle ActiveX Área de Trabalho Remota](/previous-versions//aa380808(v=vs.85))
-   [Usando o controle ActiveX Área de Trabalho Remota com canais virtuais](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [Fornecendo para o RDP Client Security](providing-for-rdp-client-security.md)
-   [Desabilitando recursos de Serviços de Área de Trabalho Remota](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a>Instalando o Conexão Web de Área de Trabalho Remota

As etapas a seguir instalam o controle ActiveX Área de Trabalho Remota e a página da Web de exemplo no diretório do tsweb do site do% SystemRoot% \\ \\ . Eles compartilham a página da Web no diretório tsweb em seu servidor, por exemplo, em https://*meuservidor*/tsweb. O controle (Msrdp. ocx) e o código de Conexão Web de Área de Trabalho Remota estão localizados em Msrdp.cab.

**Para instalar o Conexão Web de Área de Trabalho Remota**

1.  No item Adicionar/remover programas no painel de controle, em Adicionar/remover componentes do Windows, instale o Microsoft Serviços de Informações da Internet (IIS).
2.  Instale o subcomponente de serviço World Wide Web do IIS.
3.  Instale o subcomponente Conexão Web de Área de Trabalho Remota do serviço World Wide Web.

Para obter uma descrição da página da Web incluída na instalação do Conexão Web de Área de Trabalho Remota, confira [a página da Web de exemplo incluída com o controle ActiveX área de trabalho remota](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 