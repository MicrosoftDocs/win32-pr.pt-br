---
description: Os provedores, a menos que sejam dissociados provedores em execução em um aplicativo, sejam carregados em um processo de Wmiprvse.exe e não por meio de Svchost.exe com um processo de Winmgmt.exe. Para obter mais informações, consulte provedor de hospedagem e segurança.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Provedores de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921359"
---
# <a name="debugging-providers"></a>Provedores de depuração

Os provedores, a menos que sejam [*dissociados provedores*](gloss-d.md) em execução em um aplicativo, sejam carregados em um processo de Wmiprvse.exe e não por meio de Svchost.exe com um processo de Winmgmt.exe. Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).

Ao parar em um ponto de interrupção, o depurador do Visual Studio congela todo o processo de host do provedor, que geralmente é o host compartilhado Wmiprvse.exe. Isso impede a operação de quaisquer outros componentes hospedados nesse processo, incluindo a extensão de Gerenciador de Servidores WMI. Os aplicativos cliente que chamam o provedor também são bloqueados. Os problemas resultantes são piores no Windows 2000 e anteriores, pois o provedor é carregado no processo de serviço WMI (Winmgmt.exe).

Se você executar o WMI Gerenciador de Servidores em outra instância, o IDE do Visual Studio não congelará e você poderá liberar o ponto de interrupção. É recomendável que você execute seu provedor em um processo de hospedagem separado durante a fase de desenvolvimento, para que a interrupção em um ponto de interrupção apenas congele o processo que hospeda seu provedor. As outras funções no WMI continuam acessíveis para o WMI Gerenciador de Servidores e quaisquer outros aplicativos ou scripts baseados em WMI. Além disso, se o seu provedor falhar, ele não afetará a operação de outros provedores carregados no mesmo processo de host.

Para fazer com que seu provedor seja carregado em seu próprio processo de host, modifique o registro do provedor para definir a propriedade [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) para `NetworkServiceHost:[MyProvider]` onde MyProvider pode ser qualquer cadeia de caracteres que identifique exclusivamente seu provedor. Por exemplo, use o valor **\_ \_ Win32Provider. CLSID** . Quando seu provedor estiver pronto para ser entregue, retorne o **\_ \_ Win32Provider. HostingModel** para o valor pretendido, como **NetworkServiceHost**.

Se você não estiver depurando o carregamento do provedor, você pode chamar o [**método Load da \_ classe de provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) para forçar o carregamento do seu provedor e, em seguida, anexar ao processo de Wmiprvse.exe que tem a DLL carregada e depurar conforme necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classes de solução de problemas do WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
