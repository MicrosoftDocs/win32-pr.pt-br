---
description: Para criar um provedor de propriedades WMI, você deve registrar a instância win32Provider que representa seu provedor usando uma instância \_ \_ de \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrando um provedor de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbbec33f81fdfa9c1d32b20f2f5cff44566c417b1311c3429bbfaa400b68625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554204"
---
# <a name="registering-a-property-provider"></a>Registrando um provedor de propriedades

Para criar um provedor [*de*](gloss-p.md) propriedades WMI, você deve registrar a instância [**\_ \_ win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md). Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressu que você já implementou o processo de registro, conforme descrito [em Registrando um provedor.](registering-a-provider.md)

O procedimento a seguir descreve como registrar um provedor de propriedades.

**Para registrar um provedor de propriedades**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor de propriedade.

    A [**\_ \_ classe Win32Provider**](--win32provider.md) aceita os valores padrão para outras propriedades, como o **valor TRUE** para a **propriedade** Pure. Para obter mais informações, [**\_ \_ consulte Win32Provider**](--win32provider.md).

2.  Crie uma instância da [**\_ \_ classe PropertyProviderRegistration**](--propertyproviderregistration.md) que descreve o conjunto de recursos do provedor.

    A classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration,**](--objectproviderregistration.md) que fornece valores boolianas que indicam suporte para recursos específicos e uma matriz de cadeias de caracteres para indicar o suporte à consulta.

    Certifique-se de marcar a classe com os qualificadores [**Dinâmico**](dynamic-qualifier.md) [**e**](/windows/desktop/api/Provider/nl-provider-provider) Provedor. O **qualificador** dinâmico sinaliza que o WMI deve usar um provedor dinâmico para recuperar as instâncias de classe que contêm as propriedades com suporte. O **qualificador** provedor especifica o nome do provedor que o WMI deve usar.

O WMI chama NewQuery em um provedor de eventos quando um consumidor cliente registra uma consulta de filtro de evento que contém referências a eventos com suporte desse provedor de eventos. Portanto, o provedor de eventos responsável por eventos de modificação de instância para a classe EmailClass pode ser definido para gerar notificações somente para o remetente. Quando o provedor recebe uma consulta solicitando notificação de alterações na propriedade de assunto, o provedor pode começar a gerar essas notificações. Nesse cenário, o WMI não é necessário para descartar as notificações que o destinatário do relatório só altera.

O exemplo de código MOF a seguir descreve instâncias que podem ser usadas para registrar um provedor de propriedades.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> Somente os administradores podem registrar ou excluir um provedor de propriedades criando uma instância de [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).

 

 

 



