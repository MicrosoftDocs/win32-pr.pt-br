---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305a02633e8ed2aca1e372f250d6d91a8560ef1cb7a9f565e64aea6924397ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905126"
---
# <a name="e-volume-shadow-copy-service"></a>E (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E F [](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L M](vssgloss-l.md) [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusão explícita de componente**
</dt> <dd>

A adição de informações de um componente ao documento Componentes de Backup de um solicitante quando ele participa de uma operação de backup ou restauração. Os solicitantes usam [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para incluir explicitamente um componente em uma operação de backup e [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) ou [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) para incluir explicitamente um componente em uma operação de restauração.

Se qualquer componente de um autor for feito backup ou restaurado, todos os componentes não selecionados sem nenhum ancestral selecionável deverão ser incluídos explicitamente em uma operação de backup ou restauração.

Componentes selecionáveis sem ancestrais selecionáveis escolhidos por um solicitante para participação em um backup ou restauração devem ser incluídos explicitamente na operação.

Componentes não selecionados com um ancestral selecionável nunca são incluídos explicitamente.

Componentes selecionáveis com um ancestral selecionável podem ser incluídos explicitamente ou podem ser incluídos implicitamente se o ancestral for incluído explicitamente.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**cópia de sombra exposta**
</dt> <dd>

Uma cópia de sombra de volume montada em um sistema e disponível para processos que não o gerenciam. Um volume de cópia de sombra montado em uma letra da unidade ou um local de diretório é conhecido como "exposto localmente". Um volume de cópia de sombra acessível por meio de um compartilhamento (exceto por cópias de sombra acessíveis pelo cliente) é conhecido como "exposto remotamente". Todas as cópias de sombra expostas também são cópias de sombra à tona. Consulte também cópia [*de sombra acessível pelo cliente,*](vssgloss-c.md) [*cópia de sombra.*](vssgloss-s.md)

</dd> </dl>

 

 



