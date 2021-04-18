---
description: A partir do Windows Server 2008, o provedor de recursos do servidor fornece informações sobre quais recursos de servidor estão instalados no servidor. Essa classe permite que os administradores inventariam e gerenciem suas funções e recursos de servidor.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Provedor de recursos do servidor
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807907"
---
# <a name="server-feature-provider"></a>Provedor de recursos do servidor

A partir do Windows Server 2008, o provedor de recursos do servidor fornece informações sobre quais recursos de servidor estão instalados no servidor. Essa classe permite que os administradores inventariam e gerenciem suas funções e recursos de servidor.

Uma função de servidor é definida como um grupo de componentes que fornecem funções para uma área específica de funcionalidade, como impressão, arquivos, controle de domínio e assim por diante. As funções de servidor típicas são servidor de arquivos, servidor de email, servidor DNS, controlador de domínio, servidor de aplicativos e assim por diante.

Se uma empresa não estiver executando um software de gerenciamento que relate funções de servidor, como o Microsoft Operations Manager com pacotes de gerenciamento instalados, você poderá obter essas informações consultando a classe [**Win32 \_ ServerFeature**](win32-serverfeature.md) . As informações de função e recurso de servidor de computadores remotos estão disponíveis por meio de conexões remotas WMI normais ou usando o Serviço Gerenciamento Remoto do Windows (WinRM). Para obter mais informações sobre conexões DCOM remotas do WMI, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md). Para obter mais informações sobre conexões usando o protocolo [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) , consulte [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal).

O provedor de recursos do servidor dá suporte às seguintes classes WMI:

-   [**\_ServerFeature Win32**](win32-serverfeature.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> </dl>

 

 
