---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25af02bd43c5130fa7ce60ed08ec4ab822ff1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781077"
---
# <a name="d-volume-shadow-copy-service"></a>D (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**componente de banco de dados**
</dt> <dd>

Um grupo de arquivos usado por um banco de dados e definido por um gravador que precisa ser tratado como uma unidade durante as operações de backup e restauração. Consulte também [*componente*](vssgloss-c.md), [*componente de grupo de arquivos*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**provedor padrão**
</dt> <dd>

Consulte [*provedor do sistema*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**cópia de sombra excluída**
</dt> <dd>

Cópias de sombra excluídas não são acessíveis e não devem se tornar acessíveis a qualquer momento no futuro.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**Estados**
</dt> <dd>

Consulte [*dependência de componente*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**objeto de dispositivo**
</dt> <dd>

Uma cadeia de caracteres que indica a "raiz" de um volume copiado por sombra. Os arquivos e diretórios em um volume copiado de sombra podem ser referenciados por meio da prependência da cadeia de caracteres do objeto de dispositivo para um caminho correspondente no volume original. Conforme obtido como o membro do **m \_ pwszSnapshotDeviceObject** da estrutura de [**\_ \_ prop snapshot do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , o objeto do dispositivo não tem uma barra invertida (" \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**área de comparação**
</dt> <dd>

O local no volume em que os *dados diferenciais* são armazenados. Isso também é conhecido como espaço de armazenamento de cópia de sombra.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**arquivos diferenciados**
</dt> <dd>

Arquivos envolvidos em uma operação de backup incremental ou diferencial implementada pela atualização de arquivos inteiros (em oposição à modificação de seções desses arquivos usando o suporte a arquivos parciais). Por exemplo, se para implementar um backup diferencial, um arquivo inteiro (em vez de apenas a seção modificada) for copiado para uma mídia de backup, esse arquivo será um arquivo diferenciado. Consulte também [*operações de backup incremental*](vssgloss-i.md), *operações de backup diferenciais*, [*suporte a arquivos parciais*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**operações de backup diferencial**
</dt> <dd>

Uma operação de backup ou restauração executada somente em arquivos criados ou alterados desde que o último backup completo foi salvo. Consulte também [*operações de backup incremental*](vssgloss-i.md), [*suporte a arquivos parciais*](vssgloss-p.md), *arquivos diferenciados*.

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**dados diferenciais**
</dt> <dd>

Dados que podem ser aplicados a um volume original para gerar um volume de cópia de sombra. Isso também é conhecido como dados de copiar na gravação, mas esta documentação usa os dados diferenciais de termos.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**direcionamento direcionado**
</dt> <dd>

Um modo de restauração pelo qual um gravador indica que, quando um arquivo é restaurado, ele (o arquivo de origem) deve ser remapeado. O arquivo pode ser restaurado para um novo local de restauração e/ou intervalos de seus dados restaurados para um deslocamento diferente com o local de restauração.

</dd> </dl>

 

 



