---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92843e9277709a1138bc51b403089c932387e1b282e349c7907fc4cde88e9de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124476"
---
# <a name="s-volume-shadow-copy-service"></a>S (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-f.md) [](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L [M](vssgloss-l.md) [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selecionável para backup**
</dt> <dd>

Um componente será selecionável para backup se sua inclusão explícita em uma operação de backup for opcional. A selecionável para backup será habilitada se o valor do **membro bSelectable** da estrutura [**\_ COMPONENTINFO do VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) for **true.** Não há nenhum valor padrão para a seleção de um componente para backup; um autor sempre deve definir esse valor explicitamente.

Os autores também usam a seleção para restauração para organizar a participação de seus componentes em operações de restauração.

Consulte também *componente selecionável*, *selecionável para restauração,* [*inclusão explícita de componente*](vssgloss-e.md), inclusão implícita de [*componente*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selecionável para restauração**
</dt> <dd>

Um componente será selecionável para restauração se puder ser feito backup implicitamente como parte de um conjunto de componentes e, em seguida, restaurado individualmente sem o restante do conjunto de componentes. A selecionável para restauração será habilitada se o valor do **membro bSelectableForRestore** da estrutura [**\_ COMPONENTINFO do VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) for **true.** Por padrão, a selecionável de um componente para restauração é **falsa.** A selecionável para restauração tem significado apenas quando um componente não foi adicionado ao documento de backup.

Consulte também *componente selecionável,* *selecionável para backup,* [*inclusão explícita de componente,*](vssgloss-e.md) [*inclusão implícita de componente*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente selecionável**
</dt> <dd>

Um componente será selecionável se sua inclusão explícita em uma operação de backup ou restauração for opcional.

A selecionável para backup e selecionável para restauração é independente uma da outra– um componente pode ser selecionável para ambas as operações, para restauração e não para backup ou para backup e não para restauração.

Os autores também usam a seleção para organizar seus componentes em grupos:

-   Componentes não selecionados sem ancestrais selecionáveis em seus caminhos lógicos sempre deverão ser incluídos explicitamente se um autor deve ser feito backup ou restaurado.
-   Componentes não selecionáveis com ancestrais selecionáveis só serão incluídos em um backup ou restauração se pelo menos um ancestral selecionável for incluído.
-   Componentes selecionáveis sem ancestrais selecionáveis só podem ser incluídos em uma operação de backup ou restauração explicitamente.
-   Componentes selecionáveis com ancestrais selecionáveis podem ser incluídos explicitamente em uma operação de backup ou restauração ou podem ser incluídos implicitamente se um de seus ancestrais selecionáveis estiver incluído.

Consulte também [*componentes*](vssgloss-c.md), *selecionável para backup,* *selecionável para* restauração, inclusão explícita [*de componente*](vssgloss-e.md), inclusão implícita [*de componente*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**cópia de sombra**
</dt> <dd>

Uma réplica point-in-time somente leitura do conteúdo de um volume original. Cada cópia de sombra é chaveada por um GUID persistente. Também chamado de cópia de sombra de volume. Consulte também conjunto *de cópias de sombra.*

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Cópias de Sombra para Pastas Compartilhadas**
</dt> <dd>

Um recurso de Windows que cria cópias de backup online leves de volumes usando VSS. Os clientes podem acessar esses backups por meio do shell Windows para ver versões antigas de arquivos e desfazer erros sem exigir uma restauração completa. Consulte também cópia [*de sombra acessível pelo cliente.*](vssgloss-c.md)

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**conjunto de cópias de sombra**
</dt> <dd>

Uma coleção de cópias de sombra de volume criadas ao mesmo tempo e identificadas por um valor de ID do conjunto de cópias de sombra comum (um GUID persistente). Esse é o mecanismo usado para permitir que uma operação de cópia de sombra seja gerenciada entre volumes. Confira também cópia *de sombra.*

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**provedor de software**
</dt> <dd>

Um provedor que intercepta solicitações de E/S no nível de software entre o sistema de arquivos e o gerenciador de volumes. Consulte também provedor [*de hardware*](vssgloss-h.md), [*provedor*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**Subcomponente**
</dt> <dd>

Qualquer componente que tenha um caminho lógico que contenha um componente pai selecionável (para backup ou restauração). Os subcomponentes devem ter um caminho lógico do formato {nome \_ do componente} \\ {nome do subcomponente}. \_ Se o ancestral selecionável de um subcomponente (para backup ou restauração) estiver explicitamente incluído em um backup ou restauração, o subcomponente será incluído implicitamente na operação. Os subcomponentes incluídos implicitamente não têm seus dados incluídos no Documento de Componentes de Backup, independentemente de eles ser selecionáveis (para restauração ou backup) ou não. Consulte também [*componente*](vssgloss-c.md), [*caminho lógico*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**cópia de sombra em superfície**
</dt> <dd>

Um volume de sombra copiado visível para o namespace do Mount Manager de um sistema, o que significa que **FindFirstVolume** e **FindNextVolume** podem encontrá-lo e que as notificações de chegada e partida do volume são geradas. Todas as cópias de sombra expostas também são cópias de sombra à tona. No entanto, uma cópia de sombra à superfície não precisa ser exposta. Se uma cópia de sombra for transportável, ela não poderá ser a tona. Consulte também [*cópia de sombra exposta,*](vssgloss-e.md) [*cópia de sombra transportável.*](vssgloss-t.md)

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Proteção de Arquivos do Sistema**
</dt> <dd>

Consulte [*Windows Proteção de Arquivos.*](vssgloss-w.md)

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**aplicativos no nível do sistema**
</dt> <dd>

Indica o ponto no qual o VSS notifica um autor de um congelamento. Os autores inicializados como aplicativos no nível do sistema são notificados depois que os autores são inicializados como aplicativos de nível de front-end ou como aplicativos de nível de back-end. Consulte também [*nível de aplicativo*](vssgloss-a.md), [*aplicativos de nível de back-end*](vssgloss-b.md), [*aplicativos de nível de front-end*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**provedor do sistema**
</dt> <dd>

O provedor pré-instalado padrão fornecido como parte do Windows.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Pasta de Volume do Sistema**
</dt> <dd>

Um diretório compartilhado que armazena as cópias compartilhadas dos arquivos públicos de um domínio, ou seja, os arquivos replicados entre todos os controladores de domínio no domínio.

</dd> </dl>

 

 



