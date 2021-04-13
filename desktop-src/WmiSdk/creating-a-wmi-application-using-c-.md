---
description: 'Para criar um aplicativo para WMI usando C++: você deve inicializar COM, acessar e definir protocolos WMI e executar uma limpeza manual.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Criando um aplicativo WMI usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297330"
---
# <a name="creating-a-wmi-application-using-c"></a>Criando um aplicativo WMI usando C++

Para criar um aplicativo para WMI usando C++: você deve inicializar COM, acessar e definir protocolos WMI e executar uma limpeza manual. No entanto, o C++ tem a vantagem de flexibilidade e potência. Portanto, embora você esteja mais bem atendido no uso do Visual Basic Scripting Edition (VBScript) ou do Windows PowerShell para processos simples, o C++ funciona melhor para aplicativos mais sofisticados e é necessário para escrever [provedores](providing-data-to-wmi.md).

O procedimento a seguir descreve como criar um aplicativo WMI.

**Para criar um aplicativo WMI**

1.  [Inicializar com](initializing-com-for-a-wmi-application.md).

    Como o WMI é baseado em tecnologia COM, você deve executar chamadas para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para acessar o WMI.

2.  [Crie uma conexão com um namespace WMI](creating-a-connection-to-a-wmi-namespace.md).

    Por definição, o WMI é executado em um processo diferente do seu aplicativo. Portanto, você deve criar uma conexão entre seu aplicativo e o WMI.

3.  [Defina os níveis de segurança na conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).

    Para usar a conexão que você cria para o WMI, você deve definir os níveis de representação e de autenticação para seu aplicativo.

4.  Implemente a finalidade do seu aplicativo.

    O WMI expõe uma variedade de interfaces COM usadas para acessar e manipular dados em toda a sua empresa. Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [recebendo um evento WMI](receiving-a-wmi-event.md)e a [API com para WMI](com-api-for-wmi.md).

    É aí que deve existir a maior parte do seu aplicativo cliente WMI, como acessar objetos WMI ou manipular dados.

5.  [Limpe e desative seu aplicativo](cleaning-up-and-shutting-down-a-wmi-application.md).

    Depois de concluir suas consultas para o WMI, você deve destruir todos os ponteiros COM e desligar o aplicativo corretamente.

Para obter mais informações e um exemplo de código sobre como criar um aplicativo WMI, consulte [exemplo: Criando um aplicativo WMI](example-creating-a-wmi-application.md).

 

 
