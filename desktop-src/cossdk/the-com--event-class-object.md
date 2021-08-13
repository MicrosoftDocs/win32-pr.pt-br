---
description: O serviço de eventos COM+ usa um objeto de classe de evento para gerenciar a conexão entre o Publicador e o Assinante.
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: O objeto de classe de evento COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5650969895cdfa63f07e6ba77e617a962335101d4f56aeb21a5b439b27daaf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546148"
---
# <a name="the-com-event-class-object"></a>O objeto de classe de evento COM+

O serviço de eventos COM+ usa um *objeto de classe de evento* para gerenciar a conexão entre o Publicador e o Assinante. O objeto de classe de evento é um componente COM+ que é gerenciado e armazenado pelo sistema de eventos COM+ e contém as interfaces e os métodos usados por um Publicador para acionar eventos. É um objeto persistente que indica os eventos que podem ocorrer e, opcionalmente, identifica o Publicador. Especifique as interfaces e os métodos que você deseja que uma classe de evento contenha, fornecendo uma biblioteca de tipos.

para acionar um evento, o publicador instancia o objeto da classe de evento chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou o método **CreateObject** do Microsoft Visual Basic e solicitando que a interface do evento seja retornada. O objeto de classe de evento instanciado contém a implementação do sistema de eventos da interface solicitada. Um assinante interessado também deve implementar a interface de classe de evento para receber eventos de um determinado Publicador. Quando o objeto da classe de evento é instanciado, o sistema de eventos o associa aos assinantes apropriados. A lista de assinantes é mantida durante o tempo de vida do objeto de classe de evento. Um evento pode ser entregue a vários assinantes em série ou em paralelo.

Ao implementar um objeto de classe de evento, você deve fornecer uma DLL de registro automático que exporta as funções [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) . A função **DllRegisterServer** registra uma classe com e a função **DllUnregisterServer** cancela o registro do componente. Os objetos da classe de evento são armazenados no catálogo COM+, seja usando a ferramenta de administração de serviços de componentes ou programaticamente usando os métodos das interfaces [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) ou [**ICOMAdminCatalog:: InstallMultipleEventClasses**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) . Para obter informações detalhadas sobre como registrar objetos de classe de evento, consulte [registrando uma classe de evento](registering-an-event-class.md).

Como os objetos de classe de evento são componentes configurados, outros atributos, como enfileiramento, transações, segurança e assim por diante, podem ser configurados para eles usando a ferramenta de administração de serviços de componentes ou as funções do SDK administrativo do COM+.

> [!Note]  
> O serviço de eventos COM+ usa o marshaling de biblioteca de tipos. Isso coloca algumas restrições em interfaces de classe de evento. Por exemplo, o empacotador de biblioteca de tipos não dá suporte ao [**tamanho \_**](/windows/desktop/Midl/size-is) de atributos MIDL e o [**comprimento \_ é**](/windows/desktop/Midl/length-is).

 

Um objeto de classe de evento possui atributos de publicação que determinam a maneira como os eventos são publicados, bem como as seguintes propriedades:

-   **EventCLSID**. Um identificador exclusivo que especifica o CLSID do componente.
-   **EventClassName**. Um identificador exclusivo que especifica o PROGID do componente.
-   **Biblioteca**. Fornece uma lista de interfaces oferecidas pelo objeto de classe de evento. Não é necessário implementar as interfaces de acionamento especificadas na biblioteca de tipos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações de segurança de eventos COM+](com--events-security-considerations.md)
</dt> <dt>

[Filtrando eventos no COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicando e fornecendo eventos no COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Assinaturas](subscriptions.md)
</dt> <dt>

[Usando eventos COM+ com componentes em fila COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
