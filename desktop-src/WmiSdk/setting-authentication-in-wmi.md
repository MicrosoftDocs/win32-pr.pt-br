---
description: Ao fazer chamadas fora do processo de chamada ou para um serviço WMI remoto, o WMI usa a versão distribuída do Component Object Model (DCOM).
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: Configurando a autenticação no WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0293d74c528e7c1c0e77a1ffb9f5f9ee7dfd5f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170378"
---
# <a name="setting-authentication-in-wmi"></a>Configurando a autenticação no WMI

Ao fazer chamadas fora do processo de chamada ou para um serviço WMI remoto, o WMI usa a versão distribuída do Component Object Model (DCOM). As chamadas remotas e fora do processo são feitas por meio de proxies, que exigem a autenticação das credenciais do processo de chamada.

Você define o nível de autenticação ao se conectar a um computador e a um namespace do WMI. Para se conectar ao WMI, chame [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) em C++. Em script ou Visual Basic, você se conecta ao WMI usando SWbemLocator. ConnectServer ou por meio da cadeia de caracteres do [moniker](constructing-a-moniker-string.md) . A segurança DCOM e o WMI exigem certos níveis de autenticação ao se conectar entre computadores. O nível necessário é diferente de acordo com o sistema operacional que você está conectando. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

O WMI normalmente é executado em um host de serviço compartilhado e compartilha a mesma autenticação que outros processos no host. Para executar o processo WMI com um nível diferente de autenticação, execute o WMI com o comando [**winmgmt**](winmgmt.md) com a opção **/standalonehost** e defina o nível de autenticação para WMI em geral. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

Para obter mais informações e exemplos de código de como definir a autenticação para conexões WMI, consulte [definindo o serviço de autenticação usando o VBScript](setting-the-authentication-service-using-vbscript.md) e [definindo a autenticação usando C++](setting-authentication-using-c-.md). Esses tópicos também contêm tabelas que listam as constantes de autenticação para C++ e scripts.

## <a name="using-proxies-in-wmi"></a>Usando proxies no WMI

Para definir a autenticação para um proxy, chame a função [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . Para obter mais informações e um exemplo de código, consulte [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

A seguinte [API com para objetos WMI](com-api-for-wmi.md) usa proxies diretamente em C++ ou C# para chamar fora do processo ou para um serviço WMI remoto:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Os objetos de script, como [**SWbemObject**](swbemobject.md), [**SWbemServices**](swbemservices.md)e [**SWbemRefresher**](swbemrefresher.md) não usam proxies diretamente. Em vez disso, os objetos de script representam um wrapper ou uma camada que chama a [API com para objetos WMI](com-api-for-wmi.md) listados acima. Para obter mais informações e um exemplo de código de configuração de autenticação em scripts, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
