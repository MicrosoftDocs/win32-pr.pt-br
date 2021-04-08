---
description: Ao usar o serviço de eventos COM+, há etapas que você pode seguir para garantir que quaisquer informações confidenciais contidas em um evento não sejam comprometidas.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Considerações de segurança de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920610"
---
# <a name="com-events-security-considerations"></a>Considerações de segurança de eventos COM+

Ao usar o serviço de eventos COM+, há etapas que você pode seguir para garantir que quaisquer informações confidenciais contidas em um evento não sejam comprometidas.

Os editores de eventos devem ter em mente que qualquer parte que possa gravar em seu catálogo COM+ pode assinar seus eventos. Portanto, se as informações contidas em um objeto de classe de evento forem confidenciais, você deverá usar a ferramenta de administração de serviços de componentes para verificar se as comunicações com assinantes são criptografadas para o aplicativo que contém os componentes da classe de evento. (Na guia **segurança** da folha de propriedades do aplicativo com+, selecione **privacidade do pacote** como o **nível de autenticação para as configurações de chamadas** .) Além disso, você deve usar [filtros de eventos](filtering-events-in-com-.md) para ajudar a garantir que os eventos sejam entregues somente aos assinantes apropriados.

Os assinantes de eventos devem ter em mente que uma parte mal-intencionada com acesso à sua rede e o conhecimento de seu objeto de classe de evento poderia criar eventos falsos. Portanto, você deve usar a [segurança baseada em função](role-based-security-administration.md) para ajudar a garantir que os chamadores dos métodos do seu objeto de classe de evento tenham as credenciais apropriadas para executar as ações descritas pela sua implementação.

Para ajudar a proteger Publicadores e assinantes, use o serviço de eventos COM+ em uma rede privada de hosts confiáveis que é isolada da Internet por um firewall.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança do COM+](com--security.md)
</dt> <dt>

[Filtrando eventos no COM+](filtering-events-in-com-.md)
</dt> <dt>

[O objeto de classe de evento COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



