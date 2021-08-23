---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3910a2fb09688e26b33b586f4558c05cb804688645486dfec751c9839fcff278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998026"
---
# <a name="d-volume-shadow-copy-service"></a>D (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L [M](vssgloss-l.md) [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**componente de banco de dados**
</dt> <dd>

Um grupo de arquivos usados por um banco de dados e definidos por um autor como que precisam ser tratados como uma unidade durante operações de backup e restauração. Consulte [*também*](vssgloss-c.md)componente , [*componente de grupo de arquivos*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**provedor padrão**
</dt> <dd>

Consulte [*provedor do sistema*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**cópia de sombra excluída**
</dt> <dd>

Cópias de sombra excluídas não são acessíveis e não devem ser acessadas a qualquer momento no futuro.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**Dependência**
</dt> <dd>

Consulte [*dependência de componente*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**objeto device**
</dt> <dd>

Uma cadeia de caracteres que indica a "raiz" de um volume copiado por sombra. Arquivos e diretórios em um volume copiado em sombra podem ser referenciados, prependendo da cadeia de caracteres de objeto do dispositivo para um caminho correspondente no volume original. Conforme obtido como o **membro m \_ pwszSnapshotDeviceObject** da estrutura [**VSS SNAPSHOT \_ \_ PROP,**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) o objeto do dispositivo não tem nenhuma barras invertida (" \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**área de comparação**
</dt> <dd>

O local no volume em que os *dados diferenciais* são armazenados. Isso também é conhecido como espaço de armazenamento de cópia de sombra.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**arquivos diferenciais**
</dt> <dd>

Arquivos envolvidos em uma operação de backup incremental ou diferencial implementada pela atualização de arquivos inteiros (em vez de modificar seções desses arquivos usando suporte parcial a arquivos). Por exemplo, se para implementar um backup diferencial, um arquivo inteiro (em vez de apenas a seção modificada) for copiado para uma mídia de backup, esse arquivo será um arquivo diferente. Consulte também operações [*de backup incremental,*](vssgloss-i.md) *operações de backup diferenciais,* [*suporte parcial a arquivos*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**operações de backup diferencial**
</dt> <dd>

Uma operação de backup ou restauração executada somente em arquivos criados ou alterados desde que o último backup completo foi salvo. Consulte também operações [*de backup incremental,*](vssgloss-i.md) [*suporte parcial a arquivos*](vssgloss-p.md), arquivos com *diferenças.*

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**dados diferenciais**
</dt> <dd>

Dados que podem ser aplicados a um volume original para gerar um volume de cópia de sombra. Isso também é conhecido como dados de cópia na gravação, mas essa documentação usa o termo dados diferenciais.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**direcionamento**
</dt> <dd>

Um modo de restauração pelo qual um autor indica que, quando um arquivo deve ser restaurado, ele (o arquivo de origem) deve ser remapped. O arquivo pode ser restaurado para um novo local de restauração e/ou intervalos de seus dados restaurados para um deslocamento diferente com o local de restauração.

</dd> </dl>

 

 



