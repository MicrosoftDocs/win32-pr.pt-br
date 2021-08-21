---
description: Um conjunto de restauração é uma lista de todos os arquivos a serem restaurados e os locais para os quais eles serão restaurados.
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: Gerando um conjunto de restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85dd620869614420e5073f47ef4ac8732b1e2c0d0d218ea0e94ae690cb9f773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958446"
---
# <a name="generating-a-restore-set"></a>Gerando um conjunto de restauração

Um conjunto de restauração é uma lista de todos os arquivos a serem restaurados e os locais para os quais eles serão restaurados.

Como ao gerar a lista de arquivos de backup (consulte [gerando um conjunto de backup](generating-a-backup-set.md)), um algoritmo para determinar quais arquivos restaurar e onde restaurá-los deve continuar a [*instância do gravador*](vssgloss-w.md) por instância do gravador e em uma base componente por componente para cada instância do gravador.

É necessário associar cada arquivo na mídia de backup com o componente que o gerenciava. Também é necessário obter o [*método Restore*](vssgloss-r.md)do componente de gerenciamento e as informações de [*destino de restauração*](vssgloss-r.md) do arquivo e seus [*mapeamentos de local alternativos*](vssgloss-a.md) (se houver).

Alguns arquivos também podem exigir operações de [*arquivos parciais*](vssgloss-p.md) ou [*destinos direcionados*](vssgloss-d.md) para restauração.

Ao examinar a seleção dos componentes [*de backup*](vssgloss-s.md) e de [*caminhos lógicos*](vssgloss-l.md) (consulte [trabalhando com a seleção e os caminhos lógicos](working-with-selectability-and-logical-paths.md)), um solicitante é capaz de determinar a estrutura de componentes da operação de backup que ele vai restaurar.

Com a estrutura de componente do backup estabelecida, o solicitante pode obter informações de cada componente do [*conjunto de arquivos*](vssgloss-f.md) (especificação de arquivo, caminho e sinalizador de recursão). Um solicitante pode gerar um conjunto de restauração.

Arquivos que exigem [*arquivos parciais*](vssgloss-p.md)ou [*destinos direcionados*](vssgloss-d.md) fornecem suas próprias instruções de restauração detalhadas (consulte [locais de backup e restauração não padrão](non-default-backup-and-restore-locations.md)), que podem ser adicionados ao conjunto de restauração.

Um mecanismo típico para gerar um conjunto de restauração para arquivos não envolvidos em operações de arquivos parciais ou [*destinos direcionados*](vssgloss-d.md) pode continuar fazendo o seguinte:

1.  Obtenha uma lista de arquivos na mídia de backup, incluindo seus caminhos originais.

2.  Identifique a [*classe*](vssgloss-w.md) e o componente do gravador para cada arquivo na mídia de backup, fazendo o seguinte:

    -   Para cada gravador, obtenha informações de componente ([**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) chamando [**IVssExamineWriterMetadata:: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) em todos os seus componentes.
    -   Para cada componente, obtenha informações de descritor de arquivo ([**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) para cada conjunto de arquivos que o componente contém (dependendo dos tipos de dados que o componente contém chamando [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: getdatabasefile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)e [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).
    -   Compare as informações de nome e caminho do arquivo em relação às retornada pelas informações de caminho contidas no descritor de arquivo para cada conjunto de arquivos em um componente (retornado por [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc:: getspec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e [**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)) em relação a informações de caminho de arquivos armazenados para determinar se o arquivo faz parte do componente.
        > [!Note]  
        > Você deve ignorar todas as informações de local alternativo no descritor de arquivo recuperado de um componente encontrado em um documento de metadados do gravador armazenado (ou seja, [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) não retorna **NULL**). Esse local alternativo é o [*caminho alternativo*](vssgloss-a.md), que é usado somente durante o backup.

         

3.  Obtenha informações de mapeamento alternativo para cada arquivo na mídia de backup:

    -   Mapeamentos de arquivo alternativos são armazenados no gravador, não no nível de componente, e são obtidos do objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) retornado por [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).
    -   Você pode determinar se um arquivo específico tem um mapeamento de local alternativo verificando o caminho e o nome do arquivo em relação ao caminho e à especificação de arquivo contida no mapeamento de local alternativo retornado por [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), via [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc:: filespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e [**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive). (Se um caminho alternativo foi usado durante o backup, essas informações devem ser ignoradas durante essa verificação no processamento de uma restauração.)
    -   Se um arquivo e um mapeamento alternativo de descritores de arquivo corresponderem, você usará o método [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) do objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) retornado por [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) para localizar o local alternativo no qual você pode restaurar o arquivo.
    -   O mapeamento de local alternativo obtido dessa maneira não concordará necessariamente com o retornado do documento de componentes de backup de [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). O valor de [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) não estará em branco somente se o mapeamento de local alternativo for usado para um arquivo.

4.  Com essas informações de arquivo e componente, o documento de componentes de backup pode ser consultado para obter informações sobre destinos de restauração, opções e novos locais de restauração para cada arquivo. Essas informações podem ser combinadas com a lista de arquivos, componentes e locais alternativos.

5.  Os arquivos não protegidos por gravadores podem ser selecionados de maneira consistente com as operações de restauração tradicionais.

Neste ponto, um solicitante deve ter uma lista de todos os arquivos que precisa restaurar, juntamente com instruções sobre como restaurá-los e pode começar a restaurar arquivos com base em:

-   Se os mapeamentos de local alternativos ou o local do arquivo original serão usados como o destino para a restauração dependerão da presença ou da ausência de um arquivo nesse local de destino e nas configurações de componente do [**\_ \_ destino de restauração do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) e da [**\_ \_ enumeração do VSS RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) (consulte [locais de backup e restauração não padrão](non-default-backup-and-restore-locations.md)).
-   Se uma tentativa na restauração for realizada com sucesso dependerá de problemas como as permissões de acesso do destino, se os arquivos de destino estiverem bloqueados e outros problemas convencionais envolvidos na restauração de arquivos.
-   O êxito ou a falha da restauração de um determinado componente para uma determinada instância do gravador deve ser preservado no documento componentes de backup chamando [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). Isso tornará as informações acessíveis aos gravadores quando eles processarem o evento de restauração.
-   Se um arquivo for restaurado para um mapeamento de local alternativo, o solicitante deverá chamar [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping). Isso permitirá que os gravadores determinem se seus arquivos foram restaurados em locais alternativos por meio de [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Os solicitantes podem achar desejável restaurar arquivos para locais completamente novos. Isso é aceitável, mas o solicitante deve indicar isso ao gravador usando o método [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) .

 

 



