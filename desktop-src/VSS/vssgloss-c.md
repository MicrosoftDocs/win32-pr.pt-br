---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e10734fa1676980473b53cb16f5cf1166d5b2ff2813f9bf59159c37116514c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751442"
---
# <a name="c-volume-shadow-copy-service"></a>C (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L [M](vssgloss-l.md) [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**autoridade de certificação**
</dt> <dd>

Uma entidade encarregada de emitir certificados declarando que o indivíduo, o computador ou a organização destinatário que solicita o certificado atende às condições de uma política estabelecida.

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**cópia de sombra acessível pelo cliente**
</dt> <dd>

Uma cópia de sombra criada pelo provedor do sistema para dar suporte a Cópias de Sombra para Pastas Compartilhadas e outros mecanismos de reversões, que permitem que os clientes vejam versões antigas de arquivos e desfaçam erros sem exigir uma restauração completa. Uma cópia de sombra acessível pelo cliente é criada usando o valor **VSS \_ CTX \_ CLIENT \_ ACCESSIBLE** da [**\_ enumeração \_ VSS SNAPSHOT \_ CONTEXT.**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) Além disso, o valor ACESSÍVEL DO CLIENTE \_ VSS VOLSNAP ATTR da enumeração ATRIBUTOS DE INSTANTÂNEO DE VOLUME DO \_ \_ \_ [**\_ VSS \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) é definido automaticamente para cópias de sombra acessíveis pelo cliente. Consulte também [*Cópias de Sombra para Pastas Compartilhadas*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**Componente**
</dt> <dd>

Um grupo de arquivos, definido por um autor, que deve ser tratado como uma unidade durante operações de backup e restauração. Consulte também componente [*de banco de dados*](vssgloss-d.md), componente de grupo de [*arquivos*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dependência de componente**
</dt> <dd>

Uma situação em que um componente (e o conjunto de componentes definido por ele) gerenciado por um autor não pode ser feito backup ou restauração independentemente dos componentes gerenciados por outros autores. Uma dependência não indica uma ordem de preferência entre o componente com as dependências documentadas e os componentes dos que ela depende: uma dependência simplesmente indica que o componente e os componentes dos que ele depende sempre devem ser backup ou restaurados juntos.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modo de componente**
</dt> <dd>

Um modo no qual uma operação de backup ou restauração usa as informações de componente de um autor. Consulte também [*componente selecionável*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**conjunto de componentes**
</dt> <dd>

Um grupo de componentes com pelo menos um componente selecionável (para backup ou restauração) e vários componentes não selecionáveis organizados em uma hierarquia por seus caminhos lógicos. A participação implícita em uma operação de backup ou restauração depende da inclusão explícita do componente selecionável de nível superior. Somente as informações de componente desse componente selecionável estão incluídas no Documento de Componentes de Backup. Um conjunto de componentes pode incluir subcomponentes selecionáveis e não selecionáveis. Consulte também [*o caminho lógico*](vssgloss-l.md), componente [*selecionável*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**cópia de sombra na gravação**
</dt> <dd>

Uma cópia de sombra criada salvando apenas as diferenças do volume original.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**estado consistente com falha**
</dt> <dd>

O estado dos discos equivalente ao que seria encontrado após uma falha catastrófica que desliga o sistema de forma repentina. Uma restauração desse conjunto de cópias de sombra seria equivalente a uma reinicialização após um desligamento repentino. Esse é o estado padrão dos dados que foram copiados em sombra sem o suporte de autores.

</dd> </dl>

 

 



