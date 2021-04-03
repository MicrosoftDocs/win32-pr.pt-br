---
description: Descreve dois tipos de armazenamento em disco e discute os estilos de partição.
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: Discos básicos e dinâmicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3b52767983c7707f619b83c93e987b51879fdd
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "103930224"
---
# <a name="basic-and-dynamic-disks"></a>Discos básicos e dinâmicos

Antes de particionar uma unidade ou obter informações sobre o layout de partição de uma unidade, você deve primeiro compreender os recursos e as limitações dos tipos de armazenamento de disco básico e dinâmico.

Para os fins deste tópico, o termo *volume* é usado para se referir ao conceito de uma partição de disco formatada com um sistema de arquivos válido, mais COMUMENTE o NTFS, que é usado pelo sistema operacional Windows para armazenar arquivos. Um volume tem um nome de caminho Win32, pode ser enumerado pelas funções [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) e [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) , e geralmente tem uma letra de unidade atribuída a ela, como C:. Para obter mais informações sobre volumes e sistemas de arquivos, consulte [sistemas de arquivos](file-systems.md).

Neste tópico:

-   [Discos básicos](#basic-disks)
-   [Discos dinâmicos](#dynamic-disks)
-   [Estilos de partição](#partition-styles)
    -   [MBR (Registro Mestre de Inicialização)](#master-boot-record)
    -   [Tabela de partição GUID](#guid-partition-table)
-   [Detectando o tipo de disco](#detecting-the-type-of-disk)
-   [Tópicos relacionados](#related-topics)

Há dois tipos de discos ao se referir a tipos de armazenamento neste contexto: *discos básicos* e *discos dinâmicos*. Observe que os tipos de armazenamento discutidos aqui não são os mesmos que discos físicos ou estilos de partição, que estão relacionados, mas conceitos separados. Por exemplo, fazer referência a um disco básico não implica em um estilo de partição específico – o estilo de partição usado para o disco em discussão também precisa ser especificado. Para obter uma descrição simplificada de como um tipo de armazenamento de disco básico se relaciona a um disco rígido físico, consulte [partições e dispositivos de disco](disk-devices-and-partitions.md).

## <a name="basic-disks"></a>Discos básicos

Os *discos básicos* são os tipos de armazenamento mais frequentemente usados com o Windows. O termo *disco básico* refere-se a um disco que contém partições, como partições primárias e unidades lógicas, e elas, por sua vez, geralmente são formatadas com um sistema de arquivos para se tornar um volume para armazenamento de arquivos. Os discos básicos fornecem uma solução de armazenamento simples que pode acomodar uma matriz útil de cenários de requisitos de armazenamento em constante mudança. Os discos básicos também dão suporte a discos clusterizados, discos IEEE (Institute of Electrical and Electronics Engineers) 1394 e unidades removíveis USB (Universal Serial Bus). Para compatibilidade com versões anteriores, os discos básicos geralmente usam o mesmo estilo de partição MBR (registro mestre de inicialização) que os discos usados pelo sistema operacional Microsoft MS-DOS e todas as versões do Windows, mas também podem oferecer suporte a partições GPT (tabela de partição **GUID** ) em sistemas que dão suporte a ela. Para obter mais informações sobre estilos de partição MBR e GPT, consulte a seção [estilos de partição](#partition-styles) .

É possível adicionar mais espaço às partições primárias e lógicas existentes estendendo-as para um espaço não alocado adjacente e contíguo no mesmo disco. Para estender um volume básico, ele deve ser formatado com o sistema de arquivos NTFS. É possível estender uma unidade lógica no espaço livre contíguo na partição estendida que contém essa unidade. Se você estender uma unidade lógica além do espaço livre disponível na partição estendida, esta aumenta para conter a unidade lógica, contanto que a partição estendida seja seguida por espaço não alocado contíguo. Para obter mais informações, consulte [como funcionam os discos básicos e os volumes](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)).

As operações a seguir podem ser executadas somente em discos básicos:

-   Crie e exclua partições primárias e estendidas.
-   Crie e exclua unidades lógicas em uma partição estendida.
-   Formate uma partição e marque-a como ativa.

## <a name="dynamic-disks"></a>Discos Dinâmicos

> [!NOTE]
> Para todos os usos, exceto volumes de inicialização espelho (usando um volume espelhado para hospedar o sistema operacional), discos dinâmicos são preteridos. Para dados que exigem resiliência contra falha de unidade, use espaços de armazenamento, uma solução de virtualização de armazenamento resiliente. Para obter mais informações, consulte [visão geral de espaços de armazenamento](/windows-server/storage/storage-spaces/overview).

Os *discos dinâmicos* fornecem recursos que os discos básicos não têm, como a capacidade de criar volumes que abrangem vários discos (volumes estendidos e distribuídos) e a capacidade de criar volumes tolerantes a falhas (volumes espelhados e RAID-5). Assim como os discos básicos, os discos dinâmicos podem usar os estilos de partição MBR ou GPT em sistemas que dão suporte a ambos. Todos os volumes em discos dinâmicos são conhecidos como volumes dinâmicos. Os discos dinâmicos oferecem maior flexibilidade para gerenciamento de volume porque usam um banco de dados para rastrear informações sobre volumes dinâmicos no disco e sobre outros discos dinâmicos no computador. Como cada disco dinâmico em um computador armazena uma réplica do banco de dados de disco dinâmico, por exemplo, um banco de dados de disco dinâmico corrompido pode reparar um disco dinâmico usando o banco de dados em outro disco dinâmico. O local do banco de dados é determinado pelo estilo de partição do disco. Em partições MBR, o banco de dados está contido nos últimos 1 megabyte (MB) do disco. Em partições GPT, o banco de dados está contido em uma partição reservada de 1 MB (oculto).

Discos dinâmicos são uma forma separada de gerenciamento de volume que permite que volumes tenham extensões não contíguas em um ou mais discos físicos. Discos dinâmicos e volumes dependem do LDM (Gerenciador de discos lógicos) e do VDS (serviço de disco virtual) e de seus recursos associados. Esses recursos permitem que você execute tarefas como converter discos básicos em discos dinâmicos e criar volumes tolerantes a falhas. Para incentivar o uso de discos dinâmicos, o suporte ao volume de várias partições foi removido dos discos básicos e agora tem suporte exclusivo em discos dinâmicos.

As operações a seguir podem ser executadas somente em discos dinâmicos:

-   Crie e exclua volumes simples, estendidos, distribuídos, espelhados e RAID-5.
-   Estenda um volume simples ou estendido.
-   Remova um espelho de um volume espelhado ou divida o volume espelhado em dois volumes.
-   Reparar volumes espelhados ou RAID-5.
-   Reativar um disco ausente ou offline.

Outra diferença entre discos básicos e dinâmicos é que os volumes de disco dinâmicos podem ser compostos de um conjunto de extensões não contíguas em um ou vários discos físicos. Por outro lado, um volume em um disco básico consiste em um conjunto de extensões contíguas em um único disco. Devido ao local e tamanho do espaço em disco necessário para o banco de dados LDM, o Windows não pode converter um disco básico em um disco dinâmico, a menos que haja pelo menos 1 MB de espaço não utilizado no disco.

Independentemente de os discos dinâmicos em um sistema usarem o estilo de partição MBR ou GPT, você pode criar até 2.000 volumes dinâmicos em um sistema, embora o número recomendado de volumes dinâmicos seja 32 ou menos. Para obter detalhes e outras considerações sobre como usar discos dinâmicos e volumes, consulte [discos dinâmicos e volumes](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10)).

Para obter mais recursos e cenários de uso para discos dinâmicos, consulte [o que são discos e volumes dinâmicos?](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10)).

As operações comuns a discos básicos e dinâmicos são as seguintes:

-   Dão suporte a estilos de partição MBR e GPT.
-   Verifique as propriedades do disco, como capacidade, espaço livre disponível e status atual.
-   Exiba as propriedades da partição, como deslocamento, comprimento, tipo e se a partição pode ser usada como o volume do sistema na inicialização.
-   Exiba as propriedades do volume, como tamanho, atribuição de letra da unidade, rótulo, tipo, nome do caminho Win32, tipo de partição e sistema de arquivos.
-   Estabeleça atribuições de letra de unidade para volumes de disco ou partições e para dispositivos de CD-ROM.
-   Converta um disco básico em um disco dinâmico ou em um disco dinâmico em um disco básico.

A menos que especificado de outra forma, o Windows inicialmente particiona uma unidade como um disco básico por padrão. Você deve converter explicitamente um disco básico em um disco dinâmico. No entanto, há considerações de espaço em disco que devem ser contadas antes de você tentar fazer isso. Para obter mais informações, consulte [como converter em discos básicos e dinâmicos no Windows XP Professional](https://support.microsoft.com/kb/309044).

## <a name="partition-styles"></a>Estilos de partição

Os *estilos de partição*, às vezes chamados de esquemas de *partição*, são um termo que se refere à estrutura subjacente específica do layout do disco e como o particionamento é realmente organizado, quais são os recursos e também quais são as limitações. Para inicializar o Windows, as implementações do BIOS em computadores baseados em x86 e x64 exigem um disco básico que deve conter pelo menos uma partição MBR (registro mestre de inicialização) marcada como ativa, em que informações sobre o sistema operacional Windows (mas não necessariamente a instalação completa do sistema operacional) e onde as informações sobre as partições no disco são armazenadas. Essas informações são colocadas em locais separados, e esses dois locais podem estar localizados em partições separadas ou em uma única partição. Todos os outros armazenamentos de disco físico podem ser configurados como várias combinações dos dois estilos de partição disponíveis, descritos nas seções a seguir. Para obter mais informações sobre outros tipos de sistema, consulte o tópico do TechNet sobre [estilos de partição](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10)).

Os discos dinâmicos seguem cenários de uso um pouco diferentes, conforme descrito anteriormente, e a maneira como eles utilizam os dois estilos de partição é afetada por esse uso. Como discos dinâmicos geralmente não são usados para conter volumes de inicialização do sistema, essa discussão é simplificada para excluir cenários de caso especial. Para obter informações mais detalhadas sobre layouts de bloco de dados de partição e cenários de uso de disco básico ou dinâmico relacionados a estilos de partição, consulte [como funcionam os discos e volumes básicos](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) e [como funcionam os discos e volumes dinâmicos](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10)).

### <a name="master-boot-record"></a>MBR (Registro Mestre de Inicialização)

Todos os computadores baseados em x86 e x64 que executam o Windows podem usar o estilo de partição conhecido como MBR ( *registro mestre de inicialização* ). O estilo de partição MBR contém uma tabela de partição que descreve onde as partições estão localizadas no disco. Como o MBR é o único estilo de partição disponível em computadores baseados em x86 antes do Windows Server 2003 com Service Pack 1 (SP1), você não precisa escolher esse estilo. Ele é usado automaticamente.

Você pode criar até quatro partições em um disco básico usando o esquema de partição MBR: quatro partições primárias ou três principais e uma estendida. A partição estendida pode conter uma ou mais unidades lógicas. A figura a seguir ilustra um exemplo de layout de três partições primárias e uma partição estendida em um disco básico usando MBR. A partição estendida contém quatro unidades lógicas estendidas dentro dela. A partição estendida pode ou não estar localizada no final do disco, mas é sempre um único espaço contíguo para as unidades lógicas 1 a n.

![três partições primárias e uma partição estendida em um disco básico usando MBR](images/basic-mbr.png)

Cada partição, seja ela primária ou estendida, pode ser formatada para ser um volume do Windows, com uma correlação um-para-um de volume para partição. Em outras palavras, uma única partição não pode conter mais de um único volume. Neste exemplo, haveria um total de sete volumes disponíveis para o Windows para armazenamento de arquivos. Uma partição não formatada não está disponível para armazenamento de arquivos no Windows.

O layout MBR do disco dinâmico é muito semelhante ao layout MBR do disco básico, exceto que apenas uma partição primária é permitida (conhecida como a partição LDM), nenhum particionamento estendido é permitido e há uma partição oculta no final do disco para o banco de dados LDM. Para obter mais informações sobre o LDM, consulte a seção [discos dinâmicos](#basic-and-dynamic-disks) .

### <a name="guid-partition-table"></a>Tabela de partição GUID

Os sistemas que executam o Windows Server 2003 com SP1 e posterior podem usar um estilo de partição conhecido como GPT (**GUID**) (tabela de partição de identificador global exclusivo), além do estilo de partição MBR. Um disco básico usando o estilo de partição GPT pode ter até 128 partições primárias, enquanto discos dinâmicos terão uma única partição LDM como com o particionamento MBR. Como os discos básicos que usam o particionamento GPT não limitam você a quatro partições, você não precisa criar partições estendidas ou unidades lógicas.

O estilo de partição GPT também tem as seguintes propriedades:

-   Permite partições com mais de 2 terabytes.
-   Confiabilidade adicionada de replicação e proteção de verificação de redundância cíclica (CRC) da tabela de partição.
-   Suporte para tipos de partição adicionais **GUID** s definidos por OEMs (fabricantes de equipamento original), ISVs (fornecedores independentes de software) e outros sistemas operacionais.

O layout de particionamento GPT para um disco básico é ilustrado na figura a seguir.

![layout de GPT](images/basic-gpt.png)

A área de MBR de proteção existe em um layout de partição GPT para compatibilidade com versões anteriores com utilitários de gerenciamento de disco que operam em MBR. O cabeçalho GPT define o intervalo de endereços de blocos lógicos que são utilizáveis por entradas de partição. O cabeçalho GPT também define seu local no disco, seu **GUID** e uma soma de verificação de CRC32 (seleção de redundância cíclica) de 32 bits que é usada para verificar a integridade do cabeçalho GPT. Cada entrada de partição **GUID** começa com um GUID de tipo de partição. O **GUID** do tipo de partição de 16 bytes, que é semelhante a uma ID do sistema na tabela de partições de um disco MBR, identifica o tipo de dados que a partição contém e identifica como a partição é usada, por exemplo, se for um disco básico ou um disco dinâmico. Observe que cada entrada de partição **GUID** tem uma cópia de backup.

Layouts de partição **GPT** de disco dinâmico são semelhantes a este exemplo de disco básico, mas como mencionado anteriormente têm apenas uma entrada de partição LDM em vez de 1-n partições primárias, como permitido em discos básicos. Também há uma partição de banco de dados LDM oculta com uma entrada de partição **GUID** correspondente. Para obter mais informações sobre o LDM, consulte a seção [discos dinâmicos](#basic-and-dynamic-disks) .

## <a name="detecting-the-type-of-disk"></a>Detectando o tipo de disco

Não há nenhuma função específica para detectar programaticamente o tipo de disco em que um arquivo ou diretório específico está localizado. Há um método indireto.

* Passe o caminho do arquivo ou diretório para [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) para obter o ponto de montagem.
* Passe o ponto de montagem para [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) para obter o nome do volume.
* Remova a barra invertida à direita do nome do volume.
* Passe o nome do volume sem a barra invertida à direita para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir o volume.
* Use [**o \_ volume de IOCTL \_ obter \_ \_ \_ extensões de disco de volume**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) com o identificador de volume para obter os números de disco.
* Use os números de disco para construir os caminhos de disco, como " \\ \\ ? \\ PhysicalDrive *X*".
* Passe cada caminho de disco para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir o disco.
* Use [**o \_ disco do IOCTL \_ obter layout da \_ unidade \_ \_ ex**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) para obter a lista de partições.
* Verifique o **PartitionType** para cada entrada na lista de partições.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de volume](about-volume-management.md)
</dt> <dt>

[Referência técnica de volumes e discos básicos](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Referência técnica de volumes e discos dinâmicos](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Armazenamento básico versus armazenamento dinâmico no Windows XP]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
