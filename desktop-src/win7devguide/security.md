---
title: segurança (guia do desenvolvedor Windows 7)
description: o Windows 7 inclui recursos de segurança novos e aprimorados que facilitam para os desenvolvedores melhorarem, usarem e gerenciarem a segurança de seus aplicativos.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421256c23042ad1ea4bad57a616047e43276449bd93f771543d4eb41286c7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329736"
---
# <a name="security-windows-7-developer-guide"></a>segurança (guia do desenvolvedor Windows 7)

o Windows 7 inclui recursos de segurança novos e aprimorados que facilitam para os desenvolvedores melhorarem, usarem e gerenciarem a segurança de seus aplicativos. Ele vem com uma variedade de novos recursos de segurança que não só ajudam a proteger contra ameaças, mas também limitam o dano que os invasores podem fazer se acessarem um computador.

os aprimoramentos na plataforma de filtragem de Windows permitem que os desenvolvedores criem aplicativos que interagem com o processamento de pacotes na pilha de rede do sistema operacional. Os dados de rede podem ser filtrados e também modificados antes de atingirem seu destino.

além disso, devido a alterações no modelo de privilégio de Windows, a segurança do sistema é mais gerenciável pelos desenvolvedores e seus usuários finais. Novos aprimoramentos facilitam a identificação de prompts críticos para garantir que os usuários possam acessar os aplicativos e recursos de que precisam sem comprometer seus sistemas. (Consulte o [msdn Security Developer Center](https://msdn.microsoft.com/security/default.aspx).)

## <a name="windows-filtering-platform"></a>Plataforma de filtragem do Windows

no Windows 7, a plataforma de filtragem de Windows foi aprimorada para dar aos desenvolvedores mais controle sobre a funcionalidade de firewall. O nível de filtragem foi aumentado e os *ISVs* agora podem conectar a proteção e detecção personalizadas em níveis inferiores. além disso, os desenvolvedores de firewall podem ativar ou desativar seletivamente partes do firewall de Windows.

usando Windows plataforma de filtragem, os desenvolvedores podem criar firewalls, sistemas de detecção de intrusão, programas antivírus, ferramentas de monitoramento de rede e controles dos pais em seus aplicativos. Windows A filtragem de plataforma integra-se ao e oferece suporte a uma ampla variedade de recursos de firewall, incluindo comunicação autenticada e configuração dinâmica de firewall com base no uso dos aplicativos da API de soquetes (política baseada em aplicativo). Windows A filtragem de plataforma também fornece infraestrutura para gerenciamento de políticas, notificações de alteração, diagnóstico de rede e filtragem com monitoração de estado.

a arquitetura inicial da plataforma de filtragem de Windows no Windows Vista forneceu recursos para tráfego baseado em IP. Outros protocolos não IP, como, por exemplo, ARP (protocolo de resolução de endereço) e protocolos de camada de controle de acesso à mídia (*Mac*) para gerenciamento de rede e autenticação, também exigem filtragem, inspeção ou registro em log. no Windows 7, uma camada de inspeção *NDIS* que dá suporte a filtragem *MAC* e *ETHERNET* foi fornecida para atender a essa necessidade. (consulte [Windows plataforma de filtragem](../fwp/windows-filtering-platform-start-page.md).)

## <a name="user-account-control"></a>Controle de Conta de Usuário

o UAC (controle de conta de usuário) é um componente de segurança do Windows 7 que permite aos desenvolvedores criar aplicativos que permitem que os usuários executem tarefas comuns como não-administradores. Os desenvolvedores podem reduzir os riscos de segurança executando aplicativos sob um token de usuário padrão, reduzindo os riscos de erros ou ataques.

As contas de usuário que são membros do grupo *Administradores* local executarão a maioria dos aplicativos como um usuário padrão. Ao separar as funções de usuário e administrador, ao mesmo tempo em que permite a produtividade, o UAC oferece aos desenvolvedores maior controle sobre o nível de acesso que os usuários têm sobre áreas protegidas de um aplicativo. O UAC solicita credenciais em um modo de *área de trabalho seguro* , em que toda a tela é protegida para evitar falsificação da interface do usuário ou do mouse. (Consulte [atualizações da caixa de diálogo controle de conta de usuário](../win7appqual/user-interface---user-account-control-dialog-updates.md) e [controle de conta de usuário e WMI](../wmisdk/user-account-control-and-wmi.md).)

 

 
