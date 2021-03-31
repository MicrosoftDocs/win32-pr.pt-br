---
description: A desfragmentação é o processo de mover partes de arquivos em um disco para desfragmentar arquivos, ou seja, o processo de mover clusters de arquivos em um disco para torná-los contíguos.
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: Desfragmentando arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2d079f58ec98f320356a477531616788f84ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827772"
---
# <a name="defragmenting-files"></a>Desfragmentando arquivos

Quando um arquivo é gravado em um disco, às vezes o arquivo não pode ser gravado em clusters contíguos. Os clusters não contíguos reduzem o processo de leitura e gravação de um arquivo. Quanto mais detalhes em um disco os clusters não contíguos forem, pior será o problema, devido ao tempo necessário para mover o cabeçalho de leitura/gravação de uma unidade de disco rígido. Um arquivo com clusters não contíguos está *fragmentado*. Para otimizar arquivos para acesso rápido, um volume pode ser desfragmentado.

A *desfragmentação* é o processo de mover partes de arquivos em um disco para desfragmentar arquivos, ou seja, o processo de mover clusters de arquivos em um disco para torná-los contíguos. Para obter mais informações, consulte as seções a seguir:

-   [Desfragmentando um arquivo](#defragmenting-a-file)
-   [Minimizando interações entre a desfragmentação e as cópias de sombra](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [Arquivos, fluxos e tipos de fluxo com suporte para desfragmentação](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>Desfragmentando um arquivo

Em um sistema operacional simples de tarefa única, o software de desfragmentação é a única tarefa e não há nenhum outro processo para ler ou gravar no disco. No entanto, em um sistema operacional multitarefa, alguns processos podem ser lidos e gravados em uma unidade de disco rígido enquanto outro processo está Desfragmentando essa unidade de disco rígido. O truque é evitar gravações em um arquivo que está sendo desfragmentado sem interromper o processo de gravação por muito tempo. Resolver esse problema não é trivial, mas é possível.

Para permitir a desfragmentação sem a necessidade de conhecimento detalhado de uma estrutura de disco do sistema de arquivos, um conjunto de três códigos de controle é fornecido. Os códigos de controle fornecem a seguinte funcionalidade:

-   Habilitar aplicativos para localizar clusters vazios
-   Determinar o local do disco dos clusters de arquivos
-   Mover clusters em um disco

Os códigos de controle também tratam de forma transparente o problema de inibir e permitir que outros processos leiam e gravem em arquivos durante as movimentações.

Essas operações podem ser executadas sem inibir a execução de outros processos. No entanto, os outros processos têm tempos de resposta mais lentos enquanto uma unidade de disco está sendo desfragmentada.

**Para desfragmentar um arquivo**

1.  Use o código de controle [**fsctl \_ Get \_ volume \_ bitmap**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) para encontrar um local no volume que seja grande o suficiente para aceitar um arquivo inteiro.
    > [!Note]  
    > Se necessário, mova outros arquivos para tornar um local grande o suficiente. O ideal é que haja clusters não alocados suficientes após a primeira extensão do arquivo que você pode mover as extensões subsequentes para o espaço após a primeira extensão.

     

2.  Use o código de controle do [**fsctl \_ obter \_ \_ ponteiros de recuperação**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) para obter um mapa do layout atual do arquivo no disco.
3.  Percorra a estrutura do [**\_ \_ buffer dos ponteiros de recuperação**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer) retornados por [**fsctl \_ obter \_ \_ ponteiros de recuperação**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers).
4.  Use o código de controle de [**\_ \_ arquivo fsctl move**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) para mover cada cluster conforme você percorre a estrutura.
    > [!Note]  
    > Talvez seja necessário renovar o bitmap ou a estrutura de recuperação ou ambos em várias vezes enquanto outros processos gravam no disco.

     

Duas das operações que são usadas no processo de desfragmentação exigem um identificador para um volume. Somente os administradores podem obter um identificador para um volume, de modo que somente os administradores podem desfragmentar um volume. Um aplicativo deve verificar os direitos de um usuário que tenta executar o software de desfragmentação e não deve permitir que um usuário desfragmente um volume se o usuário não tiver os direitos apropriados.

Ao usar [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir um diretório durante a desfragmentação de um volume do sistema de arquivos FAT ou FAT32, especifique o valor de máscara de acesso de **\_ leitura genérico** . Não especifique o valor **máximo \_ permitido** de máscara de acesso. O acesso ao diretório será negado se isso for feito.

Não tente mover clusters alocados em um sistema de arquivos NTFS que ultrapassem o tamanho do arquivo arredondado do cluster, pois o resultado é um erro.

Os pontos de reanálise, os bitmaps e as listas de atributos nos volumes do sistema de arquivos NTFS podem ser desfragmentados, abertos para leitura e sincronização e nomeados usando a sintaxe *File*:*Name*:*Type* ; por exemplo, *dirname*: $i 30: $index \_ alocação, *MRP*:: $DATA, *MRP*:: $REPARSE \_ ponto e *MRP*:: $attribute \_ lista.

Ao desfragmentar volumes do sistema de arquivos NTFS, é permitido desfragmentar um cluster virtual além do tamanho de alocação de um arquivo.

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>Minimizando interações entre a desfragmentação e as cópias de sombra

Quando possível, mova dados em blocos alinhados em relação uns aos outros em incrementos de 16 quilobytes (KB). Isso reduz a sobrecarga de cópia em gravação quando as cópias de sombra são habilitadas, pois o espaço de cópia de sombra é aumentado e o desempenho é reduzido quando ocorrem as seguintes condições:

-   O tamanho do bloco da solicitação de movimentação é menor ou igual a 16 KB.
-   O Delta de movimentação não está em incrementos de 16 KB.

O Delta de movimentação é o número de bytes entre o início do bloco de origem e o início do bloco de destino. Em outras palavras, um bloco começando no deslocamento X (em disco) pode ser movido para um deslocamento inicial Y se o valor absoluto de X menos Y for um múltiplo par de 16 KB. Portanto, supondo que os clusters de 4 KB, uma mudança do cluster 3 para o cluster 27 será otimizada, mas uma mudança do cluster 18 para o cluster 24 não será. Observe que mod (3, 4) = 3 = Mod (27, 4). O Mod 4 é escolhido porque quatro clusters a 4 KB são equivalentes a 16 KB. Portanto, um volume formatado para um tamanho de cluster de 16 KB fará com que todos os arquivos de movimentação sejam otimizados.

Para obter mais informações sobre cópias de sombra, consulte [serviço de cópias de sombra de volume](/windows/desktop/VSS/about-the-volume-shadow-copy-service).

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>Arquivos, fluxos e tipos de fluxo com suporte para desfragmentação

Embora a maioria dos arquivos possa ser movida usando o código de controle de [**\_ \_ arquivo fsctl move**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) , nem todos podem ser movidos. Abaixo está a lista de arquivos, fluxos e tipos de fluxo (também chamados de códigos de tipo de atributo) com suporte do **\_ \_ arquivo de movimentação fsctl**. Outros arquivos, fluxos e tipos de fluxo não são suportados pelo **\_ \_ arquivo de movimentação fsctl**.

Tipos de fluxo com suporte para qualquer arquivo ou diretório.

-   :: $DATA
-   :: lista de $ATTRIBUTE \_
-   :: ponto de $REPARSE \_
-   :: $EA
-   :: $LOGGED \_ o \_ fluxo do utilitário

* * Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP: * *: $EA: \_ \_ não há suporte para o fluxo do utilitário de $logged antes do Windows 8 e do windows Server 2012

Tipos de fluxo com suporte para qualquer diretório.

-   :: $BITMAP
-   :: $INDEX \_ alocação

A seguir estão os tipos de arquivo do sistema, fluxo e fluxo com suporte do [**\_ \_ arquivo de movimentação fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) no formato "*filename*:*StreamName*: $*TypeName*".

-   $MFT:: $DATA
-   lista $MFT:: $ATTRIBUTE \_
-   $MFT:: $BITMAP
-   $AttrDef:: $DATA
-   Lista $AttrDef:: $ATTRIBUTE \_
-   $Secure: $SDS: $DATA
-   Lista $Secure:: $ATTRIBUTE \_
-   $Secure: $SDH: $INDEX \_ alocação
-   $Secure: $SDH: $BITMAP
-   $Secure: $SII: $INDEX \_ alocação
-   $Secure: $SII: $BITMAP
-   $UpCase:: $DATA
-   Lista $UpCase:: $ATTRIBUTE \_
-   $Extend: $I 30: $INDEX \_ alocação
-   Lista $Extend:: $ATTRIBUTE \_
-   $Extend: $I 30: $BITMAP
-   $Extend \\ $UsnJrnl: $J: $data
-   $Extend \\ $UsnJrnl:: $attribute \_ lista
-   $Extend \\ $UsnJrnl: $Max: $data
-   $Extend \\ $quota: $Q: alocação de $index \_
-   $Extend \\ $quota:: $attribute \_ lista
-   $Extend \\ $quota: $Q: $bitmap
-   $Extend \\ $quota: $O: alocação de $index \_
-   $Extend \\ $quota: $O: $bitmap
-   $Extend \\ $objID: $O: alocação de $index \_
-   $Extend \\ $objID:: $attribute \_ lista
-   $Extend \\ $objID: $O: $bitmap
-   $Extend \\ $Reparse: $R: alocação de $index \_
-   $Extend \\ $Reparse:: $attribute \_ lista
-   $Extend \\ $Reparse: $R: $bitmap
-   $Extend \\ $RmMetadata: $I 30: alocação de $index \_
-   $Extend \\ $RmMetadata: $I 30: $bitmap
-   $Extend \\ $RmMetadata:: $attribute \_ lista
-   $Extend \\ $RmMetadata \\ $Repair:: $data
-   $Extend \\ $RmMetadata \\ $Repair:: lista de $Attribute \_
-   $Extend \\ $RmMetadata \\ $Repair: $Config: $data
-   $Extend \\ $RmMetadata \\ $Txf: $I 30: $index \_ alocação
-   $Extend \\ $RmMetadata \\ $TxF:: lista de $Attribute \_
-   $Extend \\ $RmMetadata \\ $Txf: $I 30: $bitmap
-   $Extend \\ $RmMetadata \\ $Txf: $TxF \_ dados: $logged \_ o \_ fluxo do utilitário
-   $Extend \\ $RmMetadata \\ $TxfLog: $I 30: $index \_ alocação
-   $Extend \\ $RmMetadata \\ $TxfLog:: lista de $Attribute \_
-   $Extend \\ $RmMetadata \\ $TxfLog: $I 30: $bitmap
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops:: $data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $tops:: lista de $Attribute \_
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $tops: $T: $data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. blf:: $data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. blf:: lista de $Attribute \_

 

 
