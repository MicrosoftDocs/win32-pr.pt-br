---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783663"
---
# <a name="e-volume-shadow-copy-service"></a>E (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusão de componente explícita**
</dt> <dd>

Adicionar informações de um componente ao documento de componentes de backup de um solicitante quando ele participa de uma operação de backup ou restauração. Os solicitantes usam o [**componente IVssBackupComponents::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) Addpara incluir explicitamente um componente em uma operação de backup e [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) ou [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) para incluir explicitamente um componente em uma operação de restauração.

Se for feito backup ou restauração de qualquer componente de um gravador, todos os componentes não selecionáveis sem nenhum ancestral selecionável deverão ser incluídos explicitamente em uma operação de backup ou restauração.

Componentes selecionáveis sem ancestrais selecionáveis escolhidos por um solicitante para participação em um backup ou restauração devem ser incluídos explicitamente na operação.

Os componentes não selecionáveis com um ancestral selecionável nunca são incluídos explicitamente.

Os componentes selecionáveis com um ancestral selecionável podem ser incluídos explicitamente ou podem ser incluídos implicitamente se o ancestral for incluído explicitamente.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**cópia de sombra exposta**
</dt> <dd>

Uma cópia de sombra de volume que é montada em um sistema e está disponível para processos que não sejam aquele que o gerencia. Um volume de cópia de sombra montado sob uma letra da unidade ou um local do diretório é conhecido como "exposto localmente". Um volume de cópia de sombra acessível por meio de um compartilhamento (exceto para cópias de sombra acessíveis pelo cliente) é conhecido como "exposto remotamente". Todas as cópias de sombra expostas também são cópias de sombra em superfície. Consulte também [*cópia de sombra acessível ao cliente*](vssgloss-c.md), [*cópia de sombra*](vssgloss-s.md).

</dd> </dl>

 

 



