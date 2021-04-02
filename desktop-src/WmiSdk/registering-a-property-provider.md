---
description: Para criar um provedor de propriedades WMI, você deve registrar a \_ \_ instância Win32Provider que representa seu provedor usando uma instância de \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrando um provedor de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165218"
---
# <a name="registering-a-property-provider"></a>Registrando um provedor de propriedades

Para criar um [*provedor de propriedades*](gloss-p.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md). Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).

O procedimento a seguir descreve como registrar um provedor de propriedades.

**Para registrar um provedor de propriedades**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor de propriedades.

    A classe [**\_ \_ Win32Provider**](--win32provider.md) aceita os valores padrão para outras propriedades, como o valor **verdadeiro** para a propriedade **pura** . Para obter mais informações, consulte [**\_ \_ Win32Provider**](--win32provider.md).

2.  Crie uma instância da classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) que descreve o conjunto de recursos do provedor.

    A classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , que fornece valores Boolianos que indicam suporte para recursos específicos e uma matriz de cadeias de caracteres para indicar suporte de consulta.

    Certifique-se de marcar a classe com os qualificadores [**dinâmicos**](dynamic-qualifier.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) . O qualificador **dinâmico** sinaliza que o WMI deve usar um provedor dinâmico para recuperar as instâncias de classe que contêm as propriedades com suporte. O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.

O WMI chama NewQuery em um provedor de eventos quando um consumidor cliente registra uma consulta de filtro de eventos que contém referências a eventos com suporte pelo provedor de eventos. Portanto, o provedor de eventos responsável por eventos de modificação de instância para a classe EmailClass pode ser configurado para gerar notificações somente para o remetente. Quando o provedor recebe uma consulta solicitando a notificação de alterações para a propriedade Subject, o provedor pode começar a gerar essas notificações. Nesse cenário, o WMI não é necessário para descartar as notificações que relatam apenas as alterações de destinatário.

O exemplo de código MOF a seguir descreve as instâncias que podem ser usadas para registrar um provedor de propriedades.

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

 

 

 



