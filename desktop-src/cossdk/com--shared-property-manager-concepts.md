---
description: No COM+, o estado transitório compartilhado para objetos é gerenciado usando o SPM (Shared Property Manager). O SPM é um dispensador de recursos que você pode usar para compartilhar o estado entre vários objetos dentro de um processo de servidor.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Conceitos de Gerenciador de Propriedades compartilhados do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771287"
---
# <a name="com-shared-property-manager-concepts"></a>Conceitos de Gerenciador de Propriedades compartilhados do COM+

No COM+, o estado transitório compartilhado para objetos é gerenciado usando o SPM (Shared Property Manager). O SPM é um dispensador de recursos que você pode usar para compartilhar o estado entre vários objetos dentro de um processo de servidor.

Você não pode usar variáveis globais em um ambiente distribuído devido a problemas de simultaneidade e de conflito de nome. O Gerenciador de propriedades compartilhado elimina colisões de nomes fornecendo grupos de propriedades compartilhadas, que estabelecem namespaces exclusivos para as propriedades compartilhadas que eles contêm. O SPM também implementa bloqueios e semáforos para ajudar a proteger propriedades compartilhadas de acesso simultâneo, o que pode resultar em atualizações perdidas e deixar Propriedades em um estado imprevisível.

> [!Note]  
> Estado transitório compartilhado são informações de estado mantidas na memória que não sobrevivem a falhas do sistema. As informações são projetadas para serem compartilhadas por vários objetos entre os limites de transação (mas não entre processos).

 

As propriedades compartilhadas armazenadas no SPM estão disponíveis somente para objetos em execução no mesmo processo. Isso significa que os objetos que usarão o SPM para armazenar valores e que deverão ter acesso a esses valores devem ser instalados como parte do mesmo aplicativo COM+. É possível que os administradores do sistema movam classes COM+ de um pacote para outro depois que seu aplicativo COM+ tiver sido implantado. Se você depender de vários objetos de compartilhamento de propriedades por meio do SPM, deverá documentar claramente que eles devem ser instalados no mesmo aplicativo COM+.

Também é importante que os componentes que compartilham propriedades tenham o mesmo atributo de ativação. Se dois componentes no mesmo pacote tiverem atributos de ativação diferentes, eles geralmente não poderão compartilhar Propriedades. Por exemplo, se um componente estiver configurado para ser executado em um processo de cliente e o outro estiver configurado para ser executado em um processo de servidor, seus objetos normalmente serão executados em processos diferentes, mesmo que estejam no mesmo pacote.

Você deve sempre instanciar os objetos [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)e [**SharedProperty**](sharedproperty.md) de componentes com+ em vez de um cliente base. Se um cliente base criar grupos de propriedades e propriedades compartilhadas, as propriedades compartilhadas estarão dentro do processo de cliente base, não em um processo de servidor. Isso significa que os objetos COM+ não podem compartilhar as propriedades, a menos que os objetos também estejam em execução no processo do cliente (o que geralmente não é uma boa ideia).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de Propriedades COM+ compartilhados](com--shared-property-manager.md)
</dt> <dt>

[Grupos de propriedades compartilhadas](shared-property-groups.md)
</dt> </dl>

 

 



