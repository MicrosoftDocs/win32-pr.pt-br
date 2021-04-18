---
description: Há muitas razões pelas quais um solicitante não deve ou não ser capaz de restaurar arquivos de mídia de backup para seu local original.
ms.assetid: 2a9cfd99-5a2c-4c0c-98ff-11c745298cda
title: Trabalhando com locais alternativos durante a restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1338d76f98153ccb388e86e738b408c03dd253b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105800201"
---
# <a name="working-with-alternate-locations-during-restore"></a>Trabalhando com locais alternativos durante a restauração

Há muitas razões pelas quais um solicitante não deve ou não ser capaz de restaurar arquivos de mídia de backup para seu local original. Por exemplo, um método ou destino de restauração pode exigir tal restauração ou o local de restauração atual pode ser ocupado e não gravável.

Para lidar com esses casos, um gravador pode ter definido um [*mapeamento de local alternativo*](vssgloss-a.md), um destino de restauração não padrão a ser usado para circunstâncias especiais.

O termo mapeamento de local alternativo, conforme usado com o VSS, não deve ser confundido com o termo [*caminho alternativo*](vssgloss-a.md). Mapeamentos de local alternativos são usados somente durante operações de restauração e se referem a um destino alternativo para operações de restauração. Os caminhos alternativos são usados somente durante as operações de backup e se referem a uma fonte alternativa da qual fazer backup.

Para usar mapeamentos de local alternativos durante a restauração, um solicitante faria o seguinte (normalmente seguindo a geração de um evento de [**Prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ):

1.  Usando uma instância da interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtida pela recuperação de um gravador armazenado, um solicitante usa o método [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) para obter mapeamentos de local alternativo do gravador como instâncias da interface [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) .

    > [!Note]  
    > O solicitante usa [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), não [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). O primeiro retorna os mapeamentos de local alternativos disponíveis para uso por um solicitante. O último é usado para indicar os mapeamentos de local alternativos realmente usados por um solicitante.

     

2.  A chamada para [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) retorna uma instância da interface [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) . Esta instância contém informações de conjunto de arquivos — um caminho especificado por [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), uma especificação de arquivo retornada por meio de [**IVssWMFiledesc:: filespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e um sinalizador de recursão obtido de [**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)– correspondendo a um dos conjuntos de arquivos adicionados (usando [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) a um dos componentes gerenciados pelo gravador

    O valor retornado por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) é o mapeamento de local alternativo para esse conjunto de arquivos.

3.  Mapeamentos de local alternativos não contêm informações de componente, portanto, será necessário comparar as informações de conjunto de arquivos (caminho, especificação de arquivo e sinalizador de recursão) obtidas chamando [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) para isso contido pelos componentes do gravador.

    Essas informações podem ser encontradas Iterando os componentes do gravador e chamando [**IVssExamineWriterMetadata:: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) para obter uma instância da interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) e usar [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) para obter uma instância [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) que contém as informações do conjunto de arquivos do componente.

    Quando as informações de conjunto de arquivos retornadas pela instância de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) obtidas de [**IVssExamineWriterMetadata:: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) e [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) corresponde à obtida da instância **IVssWMFiledesc** derivada de [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation), o componente que gerencia os arquivos com o mapeamento de local alternativo específico foi encontrado.

4.  Ao localizar o componente, o solicitante pode determinar as condições sob as quais um mapeamento de local alternativo deve ser usado fazendo o seguinte:

    -   Examinando o método Restore do componente, que é obtido chamando [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).
    -   Verificando se um destino de restauração substitui o método Restore, chamando [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget).

        Se o componente encontrado no documento de metadados do gravador tiver sido [*explicitamente incluído*](vssgloss-e.md) no backup, a instância da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corresponderá a esse componente. Se o componente tiver sido [*incluído implicitamente*](vssgloss-i.md) no backup, a instância de **IVssComponent** corresponderá ao componente que define o conjunto de componentes do qual o componente no documento de metadados do gravador é um subcomponente.

5.  Com essas informações, o solicitante pode determinar um componente por componente se precisar restaurar um determinado conjunto de arquivos de um determinado componente para um destino definido pelo mapeamento de local alternativo.

6.  Ao usar um mapeamento de local alternativo, o solicitante respeita o descritor de arquivo do conjunto de arquivos e o sinalizador recursivo e usa o caminho fornecido pelo mapeamento de local alternativo.

    O solicitante indica que ele usou um mapeamento de local alternativo durante uma operação de restauração chamando [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) com as informações de local padrão do conjunto de arquivos, o destino de restauração alternativo usado e um nome de componente.

    Se o conjunto de arquivos foi gerenciado por um componente que foi explicitamente incluído no backup, esse nome de componente será usado. Se o conjunto de arquivos foi gerenciado por um componente que foi incluído implicitamente no backup, o nome usado será aquele do componente que define o conjunto de componentes do qual o componente que gerencia o conjunto de arquivos é um subcomponente.

Os gravadores verificam se os conjuntos de arquivos de um de seus componentes foram restaurados para um mapeamento de local alternativo chamando [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).

 

 



