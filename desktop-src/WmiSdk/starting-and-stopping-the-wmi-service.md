---
description: O WMI é executado como um serviço com o nome de exibição &\# 0034; Instrumentação de Gerenciamento do Windows&\# 0034; e o nome do serviço &\# 0034; winmgmt&\# 0034;.
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
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165202"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Iniciando e parando o serviço WMI

O WMI é executado como um serviço com o nome de exibição "Instrumentação de Gerenciamento do Windows" e o nome do serviço "winmgmt". O WMI é executado automaticamente na inicialização do sistema na conta LocalSystem. Se o WMI não estiver em execução, ele será iniciado automaticamente quando o primeiro aplicativo de gerenciamento ou script solicitar conexão a um namespace WMI.

Vários outros serviços dependem do serviço WMI, dependendo da versão do sistema operacional que o sistema está executando.

## <a name="starting-winmgmt-service"></a>Iniciando o serviço Winmgmt

O procedimento a seguir descreve como iniciar o serviço WMI.

**Para iniciar o serviço Winmgmt**

1.  Em um prompt de comando, digite **net** **Start** **winmgmt** \[ */<switch>* \] .

    Para obter mais informações sobre as opções disponíveis, consulte [winmgmt](winmgmt.md). Você usa a conta de administrador interna ou uma conta no grupo Administradores executando com direitos elevados para iniciar o serviço WMI. Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).

2.  Outros serviços que dependem do serviço WMI, como o host de agente do SMS ou o Firewall do Windows, não serão reiniciados automaticamente.

## <a name="stopping-winmgmt-service"></a>Parando o serviço Winmgmt

O procedimento a seguir descreve como interromper o serviço WMI.

**Para interromper o serviço Winmgmt**

1.  Em um prompt de comando, digite **net stop winmgmt**.

2.  Outros serviços que dependem do serviço WMI também são interrompidos, como o host de agente do SMS ou o Firewall do Windows.

## <a name="examples"></a>Exemplos

A galeria do TechNet contém o [script Watchdog do serviço WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), que descreve como desligar e reiniciar programaticamente o serviço Winmgmt com o PowerShell.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando as ferramentas de Command-Line do WMI](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



