---
description: 'Para criar um aplicativo para WMI usando C++: você deve inicializar COM, acessar e definir protocolos WMI e executar uma limpeza manual.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Criando um aplicativo WMI usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc68bfb9b7c17967de3142c3e431b51fc340a32acfb94484030e8fe744bf067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612396"
---
# <a name="creating-a-wmi-application-using-c"></a>Criando um aplicativo WMI usando C++

Para criar um aplicativo para WMI usando C++: você deve inicializar COM, acessar e definir protocolos WMI e executar uma limpeza manual. No entanto, o C++ tem a vantagem de flexibilidade e potência. Portanto, embora você seja mais bem atendido usando o Visual Basic VBScript (Scripting Edition) ou o Windows PowerShell para processos simples, o C++ funciona melhor para aplicativos mais sofisticados e é necessário para escrever [provedores](providing-data-to-wmi.md).

O procedimento a seguir descreve como criar um aplicativo WMI.

**Para criar um aplicativo WMI**

1.  [Inicialize COM](initializing-com-for-a-wmi-application.md).

    Como o WMI é baseado na tecnologia COM, você deve executar chamadas para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para acessar o WMI.

2.  [Crie uma conexão com um namespace WMI](creating-a-connection-to-a-wmi-namespace.md).

    Por definição, o WMI é executado em um processo diferente do seu aplicativo. Portanto, você deve criar uma conexão entre seu aplicativo e o WMI.

3.  [De definir os níveis de segurança na conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).

    Para usar a conexão que você cria para o WMI, você deve definir os níveis de representação e autenticação para seu aplicativo.

4.  Implemente a finalidade do seu aplicativo.

    O WMI expõe uma variedade de interfaces COM usadas para acessar e manipular dados em toda a sua empresa. Para obter mais informações, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md), Recebendo um evento [WMI](receiving-a-wmi-event.md)e [API COM para WMI](com-api-for-wmi.md).

    É aí que a maior parte do aplicativo cliente WMI deve existir, como acessar objetos WMI ou manipular dados.

5.  [Limpe e desligue o aplicativo.](cleaning-up-and-shutting-down-a-wmi-application.md)

    Depois de concluir suas consultas no WMI, você deve destruir todos os ponteiros COM e desligar seu aplicativo corretamente.

Para obter mais informações e um exemplo de código sobre como criar um aplicativo WMI, consulte [Exemplo: criando um aplicativo WMI](example-creating-a-wmi-application.md).

 

 
