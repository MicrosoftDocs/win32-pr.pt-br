---
description: Para criar um provedor de consumidor de eventos WMI, você deve registrar a \_ \_ instância Win32Provider que representa seu provedor usando uma instância de \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrando um provedor de consumidor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1922970838b99e2a4a371ed7b00ae0f506a0381f0018509bfd6874074e0dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992537"
---
# <a name="registering-an-event-consumer-provider"></a>Registrando um provedor de consumidor de eventos

Para criar um [*provedor de consumidor de eventos*](gloss-e.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md). Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).

O procedimento a seguir descreve como registrar um provedor de consumidor de eventos.

**Para registrar um provedor de consumidor de eventos**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.
2.  Crie uma instância da classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) que descreve o conjunto de recursos do provedor.

    As propriedades definidas por [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) incluem o caminho do objeto para o provedor e os nomes das classes de consumidor lógicas que o provedor de consumidor de eventos suporta.

    Certifique-se de marcar a classe com os qualificadores **dinâmicos** e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) . O qualificador **dinâmico** sinaliza que o WMI deve usar um provedor para recuperar as instâncias de classe. O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.

O exemplo de código a seguir mostra como registrar um provedor de consumidor de eventos.

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



