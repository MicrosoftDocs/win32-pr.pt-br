---
description: A segurança é verificada apenas nos limites do aplicativo.
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: Limites de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcfca8868677ba14c8544657aa77acf04262805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765775"
---
# <a name="security-boundaries"></a>Limites de segurança

A segurança é verificada apenas nos limites do aplicativo. Ou seja, para dois componentes no mesmo aplicativo, quando um componente chama o outro, nenhuma verificação de segurança será feita. No entanto, se dois aplicativos compartilharem o mesmo processo e um componente em um chamar um componente no outro, uma verificação de segurança será feita porque um limite de aplicativo é ultrapassado. Da mesma forma, se dois aplicativos residirem em processos de servidor diferentes e um componente no primeiro aplicativo chamar um componente no segundo aplicativo, uma verificação de segurança será feita.

Portanto, se você tiver dois componentes e quiser que as verificações de segurança sejam feitas quando um chamar o outro, você precisará colocar os componentes em aplicativos COM+ separados.

Como os aplicativos de biblioteca COM+ são hospedados por outros processos, há um limite de segurança entre o aplicativo de biblioteca e o processo de hospedagem. Além disso, o aplicativo de biblioteca não controla a segurança em nível de processo, o que afeta como você precisa configurar a segurança para ele. Para obter mais informações, consulte [segurança do aplicativo de biblioteca](library-application-security.md).

Determinar se uma verificação de segurança deve ser executada em uma chamada em um componente é baseada na propriedade de segurança no contexto de objeto criado quando o componente configurado é instanciado. Para obter mais informações, consulte [propriedade de contexto de segurança](security-context-property.md).

## <a name="component-level-access-checks"></a>Component-Level verificações de acesso

Para um aplicativo de servidor do COM+, você tem a opção de impor verificações de acesso no nível do componente ou no nível do processo.

Ao selecionar a verificação de acesso no nível do componente, você habilita as atribuições de função refinadas. Você pode atribuir funções a componentes, interfaces e métodos e obter uma política de autorização articulada. Essa será a configuração padrão para aplicativos que usam a segurança baseada em função.

Para aplicativos de biblioteca COM+, você deve selecionar segurança em nível de componente se quiser usar funções. Os aplicativos de biblioteca não podem usar a segurança em nível de processo.

Você deve selecionar a verificação de acesso no nível de componente se estiver usando a segurança programática baseada em função. As informações de contexto de chamada de segurança estão disponíveis somente quando a segurança em nível de componente está habilitada. Para obter mais informações, consulte [informações de contexto de chamada de segurança](security-call-context-information.md).

Além disso, quando você seleciona a verificação de acesso no nível do componente, a propriedade de segurança será incluída no contexto do objeto. Isso significa que a configuração de segurança pode desempenhar uma função em como o objeto é ativado. Para obter mais informações, consulte [propriedade de contexto de segurança](security-context-property.md).

## <a name="process-level-access-checks"></a>Process-Level verificações de acesso

As verificações de nível de processo aplicam-se somente ao limite do aplicativo. Ou seja, as funções que você definiu para todo o aplicativo COM+ determinarão quem recebe acesso a qualquer recurso dentro do aplicativo. Nenhuma atribuição de função refinada se aplica. Essencialmente, as funções são usadas para criar um descritor de segurança no qual qualquer chamada para os componentes do aplicativo é validada. Nesse caso, você não desejaria construir uma política de autorização detalhada com várias funções. O aplicativo usará um único descritor de segurança.

Para aplicativos de biblioteca COM+, você não selecionará verificações de acesso no nível de processo. O aplicativo de biblioteca será executado hospedado no processo do cliente e, portanto, não controlará a segurança em nível de processo. Para obter mais informações, consulte [segurança do aplicativo de biblioteca](library-application-security.md).

Com as verificações de acesso em nível de processo habilitadas, as informações de contexto de chamada de segurança não estão disponíveis. Isso significa que você não pode fazer a segurança programática ao usar apenas a segurança em nível de processo. Para obter mais informações, consulte [informações de contexto de chamada de segurança](security-call-context-information.md).

Além disso, a propriedade de segurança não será incluída no contexto do objeto. Isso significa que, ao usar apenas verificações de acesso em nível de processo, a configuração de segurança nunca desempenhará uma função na forma como o objeto é ativado. Para obter mais informações, consulte [propriedade de contexto de segurança](security-context-property.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando funções com eficiência](designing-roles-effectively.md)
</dt> <dt>

[Informações de contexto de chamada de segurança](security-call-context-information.md)
</dt> <dt>

[Propriedade de contexto de segurança](security-context-property.md)
</dt> <dt>

[Usando funções para autorização de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



