---
description: Às vezes, é útil fazer backup e restaurar apenas seções de arquivos. O VSS fornece mecanismos de arquivo parciais, que, se os solicitantes oferecerem suporte a ele, permite que os gravadores especifiquem backups e restaurações parciais de arquivos.
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: Trabalhando com arquivos parciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7194f01df11f6c0e368941e17ef6ab1620b17f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770542"
---
# <a name="working-with-partial-files"></a>Trabalhando com arquivos parciais

Às vezes, é útil fazer backup e restaurar apenas seções de arquivos. O VSS fornece mecanismos de [*arquivo parciais*](vssgloss-p.md) , que, se os solicitantes oferecerem suporte a ele, permite que os gravadores especifiquem backups e restaurações parciais de arquivos.

As operações de arquivo parcial são frequentemente de maior uso para gravadores que mantêm arquivos muito grandes, apenas uma pequena fração da alteração entre as operações de backup. Esse é o caso, geralmente é útil copiar apenas essa seção que foi alterada para mídia de backup. Por esse motivo, as operações de arquivo parcial são normalmente, mas não exclusivamente, usadas para dar suporte a operações incrementais de backup e restauração.

Se um gravador quiser implementar uma operação de arquivo parcial, ele usará [**CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) para determinar se o solicitante que está trabalhando oferece suporte à operação.

Se o solicitante oferecer suporte a operações de arquivo parciais e se ele adicionar o componente que gerencia o arquivo (ou o componente que define o conjunto de componentes que contém o arquivo) ao documento de componentes de backup, um gravador indicará quais seções do arquivo salvar (normalmente ao manipular um evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou [*pós-instantâneo*](vssgloss-p.md) ) chamando [**IVssComponent:: addparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

Além de um caminho e nome de arquivo, o gravador fornece o intervalo, informações de metadados opcionais para [**IVssComponent:: Addparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

As informações do intervalo são fornecidas como uma cadeia de caracteres que contém um dos seguintes:

-   Pares de deslocamentos no arquivo cujo backup será feito (em bytes) e o comprimento da seção de backup (em bytes), o deslocamento e o comprimento que estão sendo separados por dois-pontos e cada par separado por uma vírgula, por exemplo, *Offset1 ***:**_Length1_*_,_* * Offset2 ***:**_Length2_.

    Cada valor é um inteiro de 64 bits (em formato hexadecimal ou Decimal) que especifica um deslocamento de byte e um comprimento em bytes, respectivamente.

-   O caminho completo, incluindo o nome do arquivo, no sistema atual de um arquivo de intervalos binários que contém o seguinte:
    -   O número (expresso como um número inteiro de 64 bits) de intervalos de arquivos distintos contidos no arquivo
    -   Cada intervalo expresso como um par de inteiros de 64 bits: o primeiro membro do par que está sendo o deslocamento para o arquivo que está sendo submetido a backup (em bytes) e o segundo membro que tem o tamanho de dados a ser submetido a backup (em bytes)

Se um gravador usa um arquivo de intervalos para especificar uma operação de arquivo parcial, um solicitante deve garantir que o backup desse arquivo seja feito (mesmo que o arquivo não seja necessariamente parte do conjunto de backup padrão) ou que as informações de intervalos sejam preservadas na mídia de backup de alguma outra maneira. Se não for feito backup das informações do arquivo de intervalos, a restauração do arquivo de backup parcial será impossível.

O gravador também pode adicionar uma cadeia de caracteres que contém metadados. Esses metadados podem estar em um formato específico do gravador, pois ele destina-se a permitir que o gravador valide quaisquer restaurações futuras.

Com essas informações, um solicitante de suporte pode executar um backup de arquivo parcial.

Como exemplo, considere um arquivo grande cujo cabeçalho (bytes 64-512) contenha uma contagem de registros e outras informações atualizadas com frequência e cujos dados mais recentes sejam encontrados nos últimos 65536 bytes do arquivo — bytes 0x1239E8577A a 0x1239E7577A.

Um gravador poderia especificar uma lista de intervalos como a cadeia de caracteres "**64:448, 0x1239E8577A: 65536**."

Na restauração, e antes de realmente executar uma operação de restauração, um solicitante deve verificar se algum arquivo requer suporte parcial a arquivos.

Para fazer isso, o solicitante primeiro itera sobre os gravadores com componentes armazenados em seu documento de componentes de backup usando [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

A interface [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) é usada para retornar instâncias da interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) , que fornecem [**IVssWriterComponentsExt:: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount), que permitem que o solicitante obtenha as instâncias de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Isso permite que um solicitante obtenha informações sobre os arquivos com backup parcial para participar de uma restauração usando [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent:: getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) para a instância do [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente ao componente que gerencia o arquivo (ou o componente que define o conjunto de componentes que contém o arquivo).

Se a operação de arquivo parcial tiver sido controlada por um arquivo de intervalos, esse arquivo deverá ser restaurado antes de os dados copiados de volta para o disco. Pode acontecer que o solicitante precise copiar o arquivo de intervalos de volta para um novo local no disco. Nesse caso, indica que isso foi feito por meio do [**IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

Em seguida, o solicitante continua copiando dados para os locais apropriados no disco de restauração de destino já existente.

Um gravador (ao manipular um evento de [**pós-restauração**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) ), examinando [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) para os arquivos indicados por [**IVssComponent:: getpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile), determina se a operação de arquivo parcial foi bem-sucedida. O gravador sempre deve tentar verificar a exatidão dessa restauração usando as informações de deslocamento e todos os metadados incluídos no documento de componentes de backup.

Se o solicitante teve de restaurar o arquivo de intervalos para um novo local, o VSS atualizará essas informações para que o caminho retornado por [**IVssComponent:: Getpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) esteja correto.

 

 
