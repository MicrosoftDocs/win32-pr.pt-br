---
description: Um solicitante pode precisar restaurar arquivos para um local indicado por algo diferente do caminho padrão de um conjunto de arquivos ou seu mapeamento de local alternativo.
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: Trabalhando com novos destinos durante a restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f20a6e8c27c186648d0f662921160ab5c76988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783660"
---
# <a name="working-with-new-targets-during-restore"></a>Trabalhando com novos destinos durante a restauração

Um solicitante pode precisar restaurar arquivos para um local indicado por algo diferente do caminho padrão de um conjunto de arquivos ou seu [*mapeamento de local alternativo*](vssgloss-a.md). Há muitas razões pelas quais isso pode ocorrer — por exemplo, nenhum destino de restauração foi acessível ou um usuário solicitante solicita intencionalmente que os arquivos fossem restaurados para algum local desconhecido anteriormente. Nesse caso, o solicitante usa o novo mecanismo de destino para indicar aos gravadores que ele restaurou um arquivo em uma área diferente no disco.

Nem todos os gravadores dão suporte a um solicitante que altera o destino de restauração de um arquivo. Um solicitante precisa verificar o suporte do gravador verificando a máscara de esquema de backup do gravador (retornada por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)) e verificando se ele contém o gravador do VSS \_ BS que \_ \_ dá suporte ao \_ novo \_ sinalizador de destino.

O solicitante indica tal restauração por meio do método [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) . Além de especificar uma especificação de arquivo e um destino de restauração original e um novo, o solicitante especifica informações de componente — um caminho lógico e um nome de componente.

As informações do componente que são usadas dependem de se o componente que está gerenciando o arquivo que tem um novo destino adicionado foi [*explicitamente incluído*](vssgloss-e.md) ou [*incluído implicitamente*](vssgloss-i.md) no backup.

Se o componente de gerenciamento tiver sido explicitamente incluído, suas informações serão usadas. Se o componente de gerenciamento tiver sido incluído implicitamente, ele será um subcomponente em um conjunto de componentes. Nesse caso, as informações do componente de definição do conjunto de componentes são usadas.

Ao manipular o evento de [**pós-restauração**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , os gravadores devem verificar se algum de seus arquivos foram restaurados para um novo local. Isso pode ser feito usando os métodos [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) .

A instância da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que é usada depende de se o componente de gerenciamento do arquivo foi adicionado explicitamente ou implicitamente ao backup.

 

 



