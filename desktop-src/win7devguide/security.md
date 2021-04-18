---
title: Segurança (guia do desenvolvedor do Windows 7)
description: O Windows 7 inclui recursos de segurança novos e aprimorados que facilitam para os desenvolvedores a melhoria, o uso e o gerenciamento da segurança de seus aplicativos.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a3b317f2fe0c7d42559245108bae6a5dbf0e6f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105789519"
---
# <a name="security-windows-7-developer-guide"></a>Segurança (guia do desenvolvedor do Windows 7)

O Windows 7 inclui recursos de segurança novos e aprimorados que facilitam para os desenvolvedores a melhoria, o uso e o gerenciamento da segurança de seus aplicativos. Ele vem com uma variedade de novos recursos de segurança que não só ajudam a proteger contra ameaças, mas também limitam o dano que os invasores podem fazer se acessarem um computador.

Os aprimoramentos na plataforma de filtragem do Windows permitem que os desenvolvedores criem aplicativos que interagem com o processamento de pacotes na pilha de rede do sistema operacional. Os dados de rede podem ser filtrados e também modificados antes de atingirem seu destino.

Além disso, devido a alterações no modelo de privilégio do Windows, a segurança do sistema é mais gerenciável pelos desenvolvedores e seus usuários finais. Novos aprimoramentos facilitam a identificação de prompts críticos para garantir que os usuários possam acessar os aplicativos e recursos de que precisam sem comprometer seus sistemas. (Consulte o [msdn Security Developer Center](https://msdn.microsoft.com/security/default.aspx).)

## <a name="windows-filtering-platform"></a>Plataforma de filtragem do Windows

No Windows 7, a plataforma de filtragem do Windows foi aprimorada para fornecer aos desenvolvedores mais controle sobre a funcionalidade do firewall. O nível de filtragem foi aumentado e os *ISVs* agora podem conectar a proteção e detecção personalizadas em níveis inferiores. Além disso, os desenvolvedores de firewall podem ativar ou desativar seletivamente partes do firewall do Windows.

Usando a plataforma de filtragem do Windows, os desenvolvedores podem criar firewalls, sistemas de detecção de intrusão, programas antivírus, ferramentas de monitoramento de rede e controles dos pais em seus aplicativos. A plataforma de filtragem do Windows integra-se ao e oferece suporte a uma ampla variedade de recursos de firewall, incluindo a comunicação autenticada e a configuração dinâmica de firewall com base no uso dos aplicativos da API de soquetes (política baseada em aplicativo). A plataforma de filtragem do Windows também fornece infraestrutura para gerenciamento de políticas, notificações de alteração, diagnóstico de rede e filtragem com monitoração de estado.

A arquitetura inicial da plataforma de filtragem do Windows no Windows Vista forneceu recursos para tráfego baseado em IP. Outros protocolos não IP, como, por exemplo, ARP (protocolo de resolução de endereço) e protocolos de camada de controle de acesso à mídia (*Mac*) para gerenciamento de rede e autenticação, também exigem filtragem, inspeção ou registro em log. No Windows 7, uma camada de inspeção *NDIS* que dá suporte a filtragem *Mac* e *Ethernet* foi fornecida para atender a essa necessidade. (Consulte [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).)

## <a name="user-account-control"></a>Controle de Conta de Usuário

O UAC (controle de conta de usuário) é um componente de segurança do Windows 7 que permite aos desenvolvedores criar aplicativos que permitem que os usuários executem tarefas comuns como não-administradores. Os desenvolvedores podem reduzir os riscos de segurança executando aplicativos sob um token de usuário padrão, reduzindo os riscos de erros ou ataques.

As contas de usuário que são membros do grupo *Administradores* local executarão a maioria dos aplicativos como um usuário padrão. Ao separar as funções de usuário e administrador, ao mesmo tempo em que permite a produtividade, o UAC oferece aos desenvolvedores maior controle sobre o nível de acesso que os usuários têm sobre áreas protegidas de um aplicativo. O UAC solicita credenciais em um modo de *área de trabalho seguro* , em que toda a tela é protegida para evitar falsificação da interface do usuário ou do mouse. (Consulte [atualizações da caixa de diálogo controle de conta de usuário](../win7appqual/user-interface---user-account-control-dialog-updates.md) e [controle de conta de usuário e WMI](../wmisdk/user-account-control-and-wmi.md).)

 

 
