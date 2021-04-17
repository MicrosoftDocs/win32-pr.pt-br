---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501727"
---
# <a name="w-volume-shadow-copy-service"></a>W (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z

<dl> <dt>

<span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Proteção de arquivo do Windows**
</dt> <dd>

Um serviço do sistema que protege arquivos especiais do sistema operacional. Se um desses arquivos for excluído ou substituído, a proteção de arquivo do Windows substituirá o arquivo pelo original do cache.

</dd> <dt>

<span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**escritor**
</dt> <dd>

Um aplicativo que coordena suas operações de e/s com operações relacionadas à cópia de sombra e cópia de sombra do VSS (como backups e restaurações) para que os dados contidos no volume copiado de sombra estejam em um estado consistente.

Para dar suporte a essa coordenação, um gravador deve implementar uma instância de uma classe derivada da classe base abstrata **CVssWriter** para se comunicar com a infraestrutura do VSS. Consulte também [*cópia de sombra*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**classe de gravador**
</dt> <dd>

Um GUID (identificador global exclusivo) fornecido por um gravador durante a inicialização para indicar que ele pertence a um determinado tipo de gravadores. Por exemplo, várias implementações de um gravador podem compartilhar a mesma ID de classe do gravador.

Os gravadores da mesma classe podem ser diferenciados por suas instâncias do gravador. Cabe a um desenvolvedor de aplicativos especificar classes de gravador. Consulte também *instância do gravador*.

</dd> <dt>

<span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**instância do gravador**
</dt> <dd>

Um GUID (identificador global exclusivo) fornecido pelo VSS para cada processo do gravador em execução em um sistema. Um valor exclusivo para a instância do gravador é gerado cada vez que o gravador é iniciado.

</dd> <dt>

<span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Documento de metadados do gravador**
</dt> <dd>

Um documento XML criado por um gravador (usando a interface **IVssCreateWriterMetadata** ) que contém informações sobre o estado e os componentes do gravador. Um solicitante pode consultar documentos de metadados do gravador (usando a interface **IVssExamineWriterMetadata** ) ao executar uma operação de restauração ou backup.

Um documento de metadados do gravador contém a lista de todos os componentes de um gravador, qualquer um dos quais pode participar de um backup. Isso é diferente do documento de componentes de backup do solicitante, que contém apenas os componentes explicitamente incluídos para uma operação de backup ou restauração.

Depois de construído, o documento de metadados do gravador deve ser exibido como um objeto somente leitura. Ele pode ser salvo em disco. Consulte também [*documento de componentes de backup*](vssgloss-b.md), [*inclusão explícita de componentes*](vssgloss-e.md), inclusão de [*componentes implícitos*](vssgloss-i.md).

</dd> </dl>

 

 



