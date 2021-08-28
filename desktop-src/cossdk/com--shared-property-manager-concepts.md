---
description: No COM+, o estado transitório compartilhado para objetos é gerenciado usando o SPM (gerenciador de propriedades compartilhadas). O SPM é um distribuidor de recursos que você pode usar para compartilhar o estado entre vários objetos dentro de um processo de servidor.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Conceitos de Gerenciador de Propriedades compartilhados COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9ce190cb4f4e65e6ab5208dd2adec08f807d4f6d29d4cf99a3e70a1c0a7004
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129008"
---
# <a name="com-shared-property-manager-concepts"></a>Conceitos de Gerenciador de Propriedades compartilhados COM+

No COM+, o estado transitório compartilhado para objetos é gerenciado usando o SPM (gerenciador de propriedades compartilhadas). O SPM é um distribuidor de recursos que você pode usar para compartilhar o estado entre vários objetos dentro de um processo de servidor.

Não é possível usar variáveis globais em um ambiente distribuído devido a problemas de colisão de nomes e de competência. O gerenciador de propriedades compartilhadas elimina colisões de nomes fornecendo grupos de propriedades compartilhadas, que estabelecem namespaces exclusivos para as propriedades compartilhadas que eles contêm. O SPM também implementa bloqueios e semáforos para ajudar a proteger propriedades compartilhadas contra acesso simultâneo, o que pode resultar em atualizações perdidas e deixar as propriedades em um estado imprevisível.

> [!Note]  
> Estado transitório compartilhado são informações de estado mantidas na memória que não sobrevivem a falhas do sistema. As informações são projetadas para serem compartilhadas por vários objetos entre os limites de transação (mas não entre o processo).

 

As propriedades compartilhadas armazenadas no SPM estão disponíveis somente para objetos em execução no mesmo processo. Isso significa que os objetos que usarão o SPM para armazenar valores e que precisarão ter acesso a esses valores devem ser instalados como parte do mesmo aplicativo COM+. É possível que os administradores do sistema movam classes COM+ de um pacote para outro após a implantação do aplicativo COM+. Se você depender de vários objetos que compartilham propriedades por meio do SPM, deverá documentar claramente que eles devem ser instalados no mesmo aplicativo COM+.

Também é importante que os componentes que compartilham propriedades tenham o mesmo atributo de ativação. Se dois componentes no mesmo pacote têm atributos de ativação diferentes, eles geralmente não poderão compartilhar propriedades. Por exemplo, se um componente estiver configurado para ser executado em um processo de cliente e o outro estiver configurado para ser executado em um processo de servidor, seus objetos geralmente serão executados em processos diferentes, mesmo que eles estão no mesmo pacote.

Você sempre deve insinuar os objetos [**SharedPropertyGroupManager,**](sharedpropertygroupmanager.md) [**SharedPropertyGroup**](sharedpropertygroup.md)e [**SharedProperty**](sharedproperty.md) de componentes COM+ em vez de de um cliente base. Se um cliente base criar propriedades e grupos de propriedades compartilhadas, as propriedades compartilhadas estão dentro do processo de cliente base, não em um processo de servidor. Isso significa que os objetos COM+ não podem compartilhar as propriedades, a menos que os objetos também sejam executados no processo do cliente (o que geralmente não é uma boa ideia).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Com+ Shared Gerenciador de Propriedades](com--shared-property-manager.md)
</dt> <dt>

[Grupos de propriedades compartilhadas](shared-property-groups.md)
</dt> </dl>

 

 



