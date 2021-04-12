---
title: Canais virtuais Serviços de Área de Trabalho Remota
description: Os canais virtuais são extensões de software que podem ser usadas para adicionar aprimoramentos funcionais a um aplicativo Serviços de Área de Trabalho Remota.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292114"
---
# <a name="remote-desktop-services-virtual-channels"></a>Canais virtuais Serviços de Área de Trabalho Remota

Os *canais virtuais* são extensões de software que podem ser usadas para adicionar aprimoramentos funcionais a um aplicativo serviços de área de trabalho remota. Exemplos de aprimoramentos funcionais podem incluir: suporte para tipos especiais de hardware, áudio ou outras adições à funcionalidade básica fornecida pelo Serviços de Área de Trabalho Remota [protocolo RDP](remote-desktop-protocol.md) (RDP). O protocolo RDP fornece gerenciamento multiplexado de vários canais virtuais.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Usando Serviços de Área de Trabalho Remota canais virtuais](using-terminal-services-virtual-channels.md)
</dt> <dd>

Para implementar um canal virtual, você fornece os módulos de cliente e servidor do aplicativo de um canal virtual.

</dd> <dt>

[Referência de canais virtuais dinâmicos](dynamic-virtual-channels-reference.md)
</dt> <dd>

As interfaces de cliente do canal virtual dinâmico (DVC) têm suporte pelo Serviços de Área de Trabalho Remota.

</dd> <dt>

[Referência de canais virtuais de gráficos](graphics-virtual-channels-reference.md)
</dt> <dd>

A referência de canais virtuais de gráficos contém elementos de programação que permitem criar um canal virtual Graphics.

</dd> </dl>

Um aplicativo de canal virtual tem duas partes, um módulo de cliente e um módulo de servidor. O módulo de servidor é um programa executável em execução no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). O módulo do cliente é uma DLL que deve ser carregada na memória no computador cliente quando o programa cliente do Conexão de Área de Trabalho Remota (RDC) é executado.

Os canais virtuais podem adicionar aprimoramentos funcionais a um cliente Conexão de Área de Trabalho Remota (RDC), independentemente do protocolo RDP. Com o suporte ao canal virtual, novos recursos podem ser adicionados sem a necessidade de atualizar o software cliente ou servidor ou o protocolo RDP.

Quatro classes principais de usuários de canais virtuais foram identificadas:

-   Drivers gerais de modo kernel, como drivers de impressora ou serial.
-   Redirecionamento de sistema de arquivos (esse é apenas um caso especial de um driver de modo kernel geral).
-   Aplicativos de modo de usuário, por exemplo, recortar e colar remotamente.
-   Dispositivos de áudio.

Para obter mais informações, consulte [usando serviços de área de trabalho remota canais virtuais](using-terminal-services-virtual-channels.md).

Se você tiver habilitado um aplicativo de canais virtuais em sua implantação do Serviços de Área de Trabalho Remota, poderá disponibilizar o aplicativo para os computadores cliente que acessam o servidor Host da Sessão RD por meio do Área de Trabalho Remota controle ActiveX da Microsoft. Para obter mais informações, consulte [canais virtuais programáveis](scriptable-virtual-channels.md) e [usando o controle ActiveX área de trabalho remota com canais virtuais](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




