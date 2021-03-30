---
title: Usando Serviços de Área de Trabalho Remota canais virtuais
description: Para implementar um canal virtual, você fornece os módulos de cliente e servidor do aplicativo de um canal virtual.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635319"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>Usando Serviços de Área de Trabalho Remota canais virtuais

Para implementar um canal virtual, você fornece os módulos de cliente e servidor do aplicativo de um canal virtual. O módulo de servidor pode ser um aplicativo de modo de usuário ou um driver de modo kernel. O módulo do cliente deve ser uma DLL.

Para obter descrições desses módulos, consulte os tópicos a seguir.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Aplicativo de servidor do virtual Channel](virtual-channel-server-application.md)
</dt> <dd>

O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Observe que você deve fornecer um método para iniciar o aplicativo de servidor.

</dd> <dt>

[DLL de cliente de canal virtual](virtual-channel-client-dll.md)
</dt> <dd>

O cliente de um aplicativo de canais virtuais é uma DLL que é carregada durante a inicialização do Serviços de Área de Trabalho Remota no computador cliente. A DLL deve ser registrada no computador cliente.

</dd> <dt>

[Registro de cliente de canal virtual](virtual-channel-client-registration.md)
</dt> <dd>

Você deve armazenar o nome da DLL do cliente no registro.

</dd> <dt>

[Canais virtuais persistentes de controle remoto](remote-control-persistent-virtual-channels.md)
</dt> <dd>

Um canal virtual persistente de controle remoto não é fechado quando um controle remoto se conecta ou se desconecta da sessão conectada ao cliente. Os dados continuarão a ser transmitidos e recebidos por meio desse canal.

</dd> <dt>

[Canais virtuais dinâmicos](dynamic-virtual-channels.md)
</dt> <dd>

As APIs de canal virtual dinâmico (DVC) estendem as APIs de canal virtual existentes para Serviços de Área de Trabalho Remota, conhecidas como APIs de SVC (canal virtual estático).

</dd> </dl>

Se você tiver habilitado um aplicativo de canal virtual em sua implantação de Serviços de Área de Trabalho Remota, também poderá disponibilizar o aplicativo para computadores cliente que acessam o servidor Host da Sessão RD por meio do controle ActiveX Área de Trabalho Remota. Para obter mais informações, consulte [usando o controle ActiveX área de trabalho remota com canais virtuais](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




