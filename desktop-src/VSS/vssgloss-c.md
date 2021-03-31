---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647163"
---
# <a name="c-volume-shadow-copy-service"></a>C (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**autoridade de certificação**
</dt> <dd>

Uma entidade confiável para emitir certificados que declaram que o indivíduo, a máquina ou a organização do destinatário solicitando o certificado atende às condições de uma política estabelecida.

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**cópia de sombra acessível pelo cliente**
</dt> <dd>

Uma cópia de sombra criada pelo provedor do sistema para dar suporte a Cópias de Sombra para Pastas Compartilhadas e outros mecanismos de reversão, que permitem aos clientes ver versões antigas de arquivos e desfazer erros sem a necessidade de uma restauração completa. Uma cópia de sombra acessível pelo cliente é criada usando o valor **\_ acessível do \_ cliente \_ VSS CTX** da enumeração de [**\_ \_ \_ contexto de instantâneo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) . Além disso, o \_ \_ valor acessível do cliente de attr do VSS VOLSNAP \_ \_ da enumeração de [**\_ \_ atributos de \_ instantâneo \_ de volume do VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) é definido automaticamente para cópias de sombra acessíveis pelo cliente. Consulte também [*cópias de sombra para pastas compartilhadas*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**componente**
</dt> <dd>

Um grupo de arquivos, definido por um gravador, que deve ser tratado como uma unidade durante as operações de backup e restauração. Consulte também [*componente de banco de dados*](vssgloss-d.md), [*componente de grupo de arquivos*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dependência de componente**
</dt> <dd>

Uma situação na qual um componente (e o conjunto de componentes definido por ele) gerenciado por um gravador não pode ser submetido a backup ou restauração independentemente de componentes gerenciados por outros gravadores. Uma dependência não indica uma ordem de preferência entre o componente com as dependências documentadas e os componentes dos quais ela depende: uma dependência indica apenas que o componente e os componentes dos quais depende devem ser sempre submetidos a backup ou restaurados juntos.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modo de componente**
</dt> <dd>

Um modo no qual uma operação de backup ou restauração usa as informações de componente do gravador. Consulte também [*componente selecionável*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**conjunto de componentes**
</dt> <dd>

Um grupo de componentes com pelo menos um componente selecionável (para backup ou restauração) e vários componentes não selecionáveis organizados em uma hierarquia por seus caminhos lógicos. A participação implícita em uma operação de backup ou restauração depende da inclusão explícita do componente selecionável de nível superior. Somente as informações de componente desse componente selecionável estão incluídas no documento componentes de backup. Um conjunto de componentes pode incluir subcomponentes selecionáveis e não selecionáveis. Consulte também [*caminho lógico*](vssgloss-l.md), [*componente selecionável*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**cópia de sombra de cópia em gravação**
</dt> <dd>

Uma cópia de sombra criada salvando apenas as diferenças do volume original.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**estado consistente de falha**
</dt> <dd>

O estado dos discos é equivalente ao que seria encontrado após uma falha catastrófica que desliga abruptamente o sistema. Uma restauração desse conjunto de cópia de sombra seria equivalente a uma reinicialização após um desligamento abrupta. Esse é o estado padrão dos dados que foram copiados em sombra sem o suporte de gravadores.

</dd> </dl>

 

 



