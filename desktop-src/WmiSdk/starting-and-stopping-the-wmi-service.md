---
description: O WMI é executado como um serviço com o nome de exibição &\# 0034;Windows Management Instrumentation&0034; e o nome do serviço \# &\# 0034;winmgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Iniciando e parando o serviço WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b22524d356bad5f23f4ca1cc8a3e7c68e69fd83f0dc38e64eba70bc1812436f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315004"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Iniciando e parando o serviço WMI

O WMI é executado como um serviço com o nome de exibição "Windows Instrumentação de Gerenciamento" e o nome do serviço "winmgmt". O WMI é executado automaticamente na inicialização do sistema na conta LocalSystem. Se o WMI não estiver em execução, ele será iniciado automaticamente quando o primeiro aplicativo de gerenciamento ou script solicitar conexão com um namespace WMI.

Vários outros serviços dependem do serviço WMI, dependendo da versão do sistema operacional que o sistema está executando.

## <a name="starting-winmgmt-service"></a>Iniciando o serviço Winmgmt

O procedimento a seguir descreve como iniciar o serviço WMI.

**Para iniciar o Serviço Winmgmt**

1.  Em um prompt de comando, insira **net** **start** **winmgmt** \[ */<switch>* \] .

    Para obter mais informações sobre as opções disponíveis, consulte [winmgmt](winmgmt.md). Você usa a conta de Administrador ou uma conta no grupo Administradores em execução com direitos elevados para iniciar o serviço WMI. Para obter mais informações, consulte [Controle de conta de usuário e WMI](user-account-control-and-wmi.md).

2.  Outros serviços que dependem do serviço WMI, como o Host do Agente de SMS ou Windows Firewall, não serão reiniciados automaticamente.

## <a name="stopping-winmgmt-service"></a>Interrompendo o serviço Winmgmt

O procedimento a seguir descreve como interromper o serviço WMI.

**Para interromper o serviço Winmgmt**

1.  Em um prompt de comando, insira **net stop winmgmt**.

2.  Outros serviços que dependem do serviço WMI também são interrompidos, como o Host do Agente de SMS ou Windows Firewall.

## <a name="examples"></a>Exemplos

A Galeria do TechNet contém o script watchdog do serviço [WMI,](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282)que descreve como desligar e reiniciar programaticamente o serviço winmgmt com o PowerShell.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando as ferramentas de Command-Line WMI](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



