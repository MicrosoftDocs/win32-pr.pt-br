---
title: Protocolo RDP
description: o protocolo de Área de Trabalho Remota da Microsoft (RDP) fornece recursos de exibição e entrada remotos em conexões de rede para aplicativos baseados em Windows em execução em um servidor.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota protocolo RDP (RDP)
- RDP (consulte protocolo RDP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a322e90bd036533e357925607fac6a78c364eababad5f353b4d53dfa51df735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756167"
---
# <a name="remote-desktop-protocol"></a>Protocolo RDP

o protocolo de Área de Trabalho Remota da Microsoft (RDP) fornece recursos de exibição e entrada remotos em conexões de rede para aplicativos baseados em Windows em execução em um servidor. O RDP foi projetado para dar suporte a diferentes tipos de topologias de rede e vários protocolos de LAN.

> [!Note]  
> Este tópico destina-se a desenvolvedores de software. se você estiver procurando informações do usuário para Área de Trabalho Remota, consulte [suporte a Windows](https://windows.microsoft.com/windows/support#1TC=windows-8). Se você estiver procurando informações de profissionais de ti para Área de Trabalho Remota, consulte [serviços de área de trabalho remota no TechNet](/windows/deployment/deploy-whats-new).

 

## <a name="basic-architecture"></a>Arquitetura básica

O RDP se baseia em, e uma extensão da, a família de protocolos ITU T. 120. O RDP é um protocolo compatível com vários canais que permite canais virtuais separados para a realização de comunicação do dispositivo e dados de apresentação do servidor, bem como dados de teclado e mouse do cliente criptografados. O RDP fornece uma base extensível e dá suporte a até 64.000 canais separados para transmissão de dados e provisões para transmissão do MultiPoint.

No servidor, o RDP usa seu próprio driver de vídeo para renderizar a saída de exibição, construindo as informações de renderização em pacotes de rede usando o protocolo RDP e enviando-as pela rede para o cliente. no cliente, o RDP recebe dados de renderização e interpreta os pacotes em chamadas de API do Microsoft Windows graphics device interface (GDI). Para o caminho de entrada, os eventos de teclado e mouse do cliente são redirecionados do cliente para o servidor. No servidor, o RDP usa seu próprio teclado e driver de mouse para receber esses eventos de teclado e mouse.

Em uma sessão de Área de Trabalho Remota, todas as variáveis de ambiente — por exemplo, variáveis que determinam a profundidade de cor e a habilitação e a desabilitação de papel de parede — são determinadas pelas configurações de conexão de RCP-Tcp. Isso se aplica a todas as funções e métodos que definem variáveis de ambiente na [referência de conexão Web de área de trabalho remota](remote-desktop-web-connection-reference.md) e na interface de [provedor do serviços de área de trabalho remota WMI](terminal-services-wmi-provider-reference.md).

## <a name="features"></a>Recursos

O Microsoft RDP inclui os seguintes recursos e funcionalidades:

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encripta
</dt> <dd>

O RDP usa a codificação RC4 da segurança RSA, uma codificação de fluxo projetada para criptografar com eficiência pequenas quantidades de dados. O RC4 foi projetado para comunicações seguras em redes. Os administradores podem optar por criptografar dados usando uma chave de 56 ou 128 bits.

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Recursos de redução de largura de banda
</dt> <dd>

O RDP dá suporte a vários mecanismos para reduzir a quantidade de dados transmitidos em uma conexão de rede. Os mecanismos incluem compactação de dados, cache persistente de bitmaps e cache de glifos e fragmentos na RAM. O cache de bitmap persistente pode fornecer uma melhoria significativa no desempenho em relação a conexões de largura de banda baixa, especialmente ao executar aplicativos que fazem uso extensivo de bitmaps grandes.

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Desconexão de roaming
</dt> <dd>

Um usuário pode se desconectar manualmente de uma sessão de área de trabalho remota sem fazer logoff. O usuário é automaticamente reconectado à sessão desconectada quando ele faz logon no sistema, seja do mesmo dispositivo ou de um dispositivo diferente. Quando a sessão de um usuário é encerrada inesperadamente por uma falha de rede ou cliente, o usuário é desconectado, mas não é desconectado.

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Mapeamento da área de transferência
</dt> <dd>

Os usuários podem excluir, copiar e colar texto e gráficos entre aplicativos em execução no computador local e aqueles em execução em uma sessão de área de trabalho remota e entre sessões.

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Redirecionamento de impressão
</dt> <dd>

Os aplicativos executados em uma sessão de área de trabalho remota podem ser impressos em uma impressora anexada ao dispositivo cliente.

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canais virtuais
</dt> <dd>

Usando a arquitetura de canal virtual de RDP, os aplicativos existentes podem ser aumentados e novos aplicativos podem ser desenvolvidos para adicionar recursos que exigem comunicações entre o dispositivo cliente e um aplicativo em execução em uma sessão de área de trabalho remota.

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Controle remoto
</dt> <dd>

A equipe de suporte do computador pode exibir e controlar uma sessão de área de trabalho remota. O compartilhamento de entrada e exibição de gráficos entre duas sessões de área de trabalho remota oferece a uma pessoa de suporte a capacidade de diagnosticar e resolver problemas remotamente.

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Balanceamento de carga de rede
</dt> <dd>

O RDP aproveita o NLB (balanceamento de carga de rede), quando disponível.

</dd> </dl>

Além disso, o RDP contém os seguintes recursos:

-   Suporte para cor de 24 bits.
-   Desempenho aprimorado em conexões dial-up de baixa velocidade por meio de largura de banda reduzida.
-   Autenticação de cartão inteligente por meio de Serviços de Área de Trabalho Remota.
-   Gancho de teclado. a capacidade de direcionar combinações de chave de Windows especiais, no modo de tela inteira, para o computador local ou para um computador remoto.
-   Som, unidade, porta e redirecionamento de impressora de rede. Sons que ocorrem no computador remoto podem ser ouvidos no computador cliente que executa o cliente RDC, e as unidades de cliente locais ficarão visíveis para a sessão de área de trabalho remota.

 

 