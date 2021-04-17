---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794549"
---
# <a name="a-volume-shadow-copy-service"></a>A (Serviço de Cópias de Sombra de Volume)

A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Anular evento**
</dt> <dd>

Um evento VSS emitido pelo Serviço de Cópias de Sombra de Volume indicando que uma operação de backup ou restauração em conformidade foi anulada. O manipulador de eventos é **CVssWriter:: OnAbort**.

</dd> <dt>

<span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**
</dt> <dd>

O serviço de Active Directory (ADSI) é um serviço baseado em COM que fornece um mecanismo para localizar, identificar e acessar os usuários e os recursos disponíveis em um sistema de ambiente de computação distribuído. Em particular, o serviço Active Directory é usado para gerenciar informações de diretório da empresa para distribuição por um servidor de domínio do Windows.

</dd> <dt>

<span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**mapeamento de local alternativo**
</dt> <dd>

Um caminho, diferente do caminho original de um arquivo, no qual o arquivo pode ser restaurado em determinadas condições. Normalmente, mapeamentos de local alternativos não são definidos para um único arquivo bem definido, mas para um par de especificação de caminho/arquivo e podem ser recursivos.

Um mapeamento de local alternativo é usado somente durante uma operação de restauração e não deve ser confundido com um caminho alternativo, que é usado somente durante uma operação de backup. Consulte também *caminho alternativo*.

</dd> <dt>

<span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**caminho alternativo**
</dt> <dd>

Durante as operações de backup, um par de especificação de caminho/arquivo (manipulado por uma instância da interface **IVssWMFiledesc** ) é considerado como um caminho alternativo se seu descritor de arquivo (como retornado por **IVssWMFiledesc:: GetAlternateLocation**) for não nulo. É desse caminho, em vez do caminho especificado padrão, que os arquivos devem ser copiados quando um volume é submetido a backup.

Um caminho alternativo é usado somente durante uma operação de backup e não deve ser confundido com um mapeamento de local alternativo. Um mapeamento de local alternativo é usado somente durante as operações de restauração. Consulte também *mapeamento de local alternativo*.

</dd> <dt>

<span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**nível do aplicativo**
</dt> <dd>

Usado pelo VSS para indicar o ponto no curso da criação de uma cópia de sombra que um gravador é notificado de um congelamento. Consulte também [*aplicativos de nível de back-end*](vssgloss-b.md), [*congelamento*](vssgloss-f.md), [*aplicativos de nível front-end*](vssgloss-f.md), [*cópia de sombra*](vssgloss-s.md), [*aplicativos de nível de sistema*](vssgloss-s.md), [*gravador*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**cópia de sombra recuperada automaticamente**
</dt> <dd>

Uma cópia de sombra que tinha processamento adicional por um gravador está em um estado completamente consistente para backup ou Data Mining ações (por exemplo, reverter todas as transações que ainda não foram concluídas no ponto em que a cópia de sombra foi criada.) Isso pode ser iniciado por um gravador, especificando um sinalizador apropriado da enumeração **de \_ \_ sinalizadores de componente do VSS** no membro **DwComponentFlags** da **estrutura \_ COMPONENTINFO do VSS** ou por um solicitante, adicionando o sinalizador de **\_ \_ \_ \_ recuperação de reversão do atributo VOLSNAP do VSS** para o contexto da cópia de sombra. A recuperação automática permite que os dados copiados de sombra sejam usados em um volume somente leitura, por Data Mining, restaurações parciais (por exemplo, itens selecionados em um banco de dados) ou outras finalidades.

Consulte também [*cópia de sombra transportável*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**cópia de sombra de lançamento automático**
</dt> <dd>

Uma cópia de sombra que será excluída após o encerramento de uma operação de backup. Programaticamente, isso significa que a cópia de sombra será excluída quando a interface **IVssBackupComponents** for liberada. Uma cópia de sombra de lançamento automático não pode ser persistente.

Por padrão, todas as cópias de sombra são lançadas automaticamente. Consulte também [*cópia de sombra persistente*](vssgloss-p.md), [*cópia de sombra transportável*](vssgloss-t.md).

</dd> </dl>

 

 



