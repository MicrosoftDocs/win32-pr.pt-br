---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647159"
---
# <a name="i-volume-shadow-copy-service"></a>I (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) i J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identificar evento**
</dt> <dd>

Um evento do VSS que indica que um gravador ou um solicitante precisa consultar o gravador atual. Ele é usado para construir as informações de metadados do gravador atual. Consulte também [*solicitante*](vssgloss-r.md), [*gravador*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusão de componente implícita**
</dt> <dd>

Não adicionar informações de um componente ao documento de componentes de backup de um solicitante quando ele participa de uma operação de backup ou restauração.

Os componentes não selecionáveis com um ancestral selecionável só serão incluídos implicitamente se seu ancestral estiver incluído.

Os componentes selecionáveis com um ancestral selecionável podem ser incluídos implicitamente, se o ancestral estiver incluído ou pode ser incluído explicitamente.

Os componentes não selecionáveis sem nenhum antepassado selecionável nunca são incluídos implicitamente em uma operação de backup ou restauração — todos esses componentes devem ser explicitamente adicionados ao documento de componentes de backup se qualquer um dos componentes do escritor participarem.

Componentes selecionáveis sem ancestrais selecionáveis escolhidos por um solicitante para participação em um backup ou restauração não podem ser incluídos implicitamente na operação, mas devem ser adicionados explicitamente ao documento de componentes de backup.

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**operações de backup incremental**
</dt> <dd>

Uma operação de backup ou restauração é executada somente em arquivos criados ou alterados desde que o último backup completo, incremental ou diferencial foi salvo. Consulte também [*operações de backup diferencial*](vssgloss-d.md).

</dd> </dl>

 

 



