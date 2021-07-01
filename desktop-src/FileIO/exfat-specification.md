---
description: Especificação do sistema de arquivos exFat.
title: Especificação do sistema de arquivos exFAT
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 94b5bcdc69201573bc92290c148a7d3ce8304868
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119011"
---
# <a name="exfat-file-system-specification"></a>Especificação do sistema de arquivos exFAT

## <a name="1-introduction"></a>1 Introdução

O sistema de arquivos exFAT é o sucesso do FAT32 na família FAT de sistemas de arquivos. Essa especificação descreve o sistema de arquivos exFAT e fornece todas as informações necessárias para implementar o sistema de arquivos exFAT.

### <a name="11-design-goals"></a>1.1 Metas de design

O sistema de arquivos exFAT tem três metas de design centrais (veja a lista abaixo).

1. *Mantenha a simplicidade dos sistemas de arquivos baseados em FAT.*

   > Dois dos pontos fortes dos sistemas de arquivos baseados em FAT são sua simplicidade relativa e facilidade de implementação. No final de seus antecessores, os implementadores devem achar o exFAT relativamente simples e fácil de implementar.

2. *Habilitar arquivos e dispositivos de armazenamento muito grandes.*

   > O sistema de arquivos exFAT usa 64 bits para descrever o tamanho do arquivo, permitindo assim aplicativos que dependem de arquivos muito grandes. O sistema de arquivos exFAT também permite clusters tão grandes quanto 32 MB, habilitando efetivamente dispositivos de armazenamento muito grandes.

3. *Incorporar extensibilidade para inovação futura.*

   > O sistema de arquivos exFAT incorpora extensibilidade em seu design, permitindo que o sistema de arquivos acompanhe as inovações no armazenamento e as alterações no uso.

### <a name="12-specific-terminology"></a>1.2 Terminologia específica

No contexto dessa especificação, determinados termos (consulte Tabela [1](#table-1-definition-of-terms-which-carry-very-specific-meaning)) têm significado específico para o design e a implementação do sistema de arquivos exFAT.

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**Tabela 1 Definição de termos que têm um significado muito específico**

<table>
<thead>
<tr class="header">
<th><strong>Termo</strong></th>
<th><strong>Definição</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Deve</td>
<td>Essa especificação usa o termo "deve" para descrever um comportamento obrigatório.</td>
</tr>
<tr class="even">
<td>Deve</td>
<td>Essa especificação usa o termo "deve" para descrever um comportamento que ele recomenda fortemente, mas não torna obrigatório.</td>
</tr>
<tr class="odd">
<td>Mai</td>
<td>Essa especificação usa o termo "pode" para descrever um comportamento opcional.</td>
</tr>
<tr class="even">
<td>Obrigatório</td>
<td>Esse termo descreve um campo ou estrutura que uma implementação deve modificar e interpretar como essa especificação descreve.</td>
</tr>
<tr class="odd">
<td>Opcional</td>
<td>Este termo descreve um campo ou estrutura que uma implementação pode ou não dar suporte. Se uma implementação dá suporte a um determinado campo ou estrutura opcional, ela deve modificar e interpretar o campo ou a estrutura, conforme descrito por essa especificação.</td>
</tr>
<tr class="even">
<td>Indefinido</td>
<td>Este termo descreve o conteúdo de campo ou estrutura que uma implementação pode modificar conforme necessário (ou seja, limpar para zero ao definir estruturas ou campos ao redor) e não deve interpretar para conter nenhum significado específico.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td><p>Este termo descreve o conteúdo de campo ou estrutura que implementa:</p>
<ol type="1">
<li><p>Deve inicializar como zero e não deve usar para nenhuma finalidade</p></li>
<li><p>Não deve interpretar, exceto ao computar as verificações</p></li>
<li><p>Deve preservar entre operações que modificam estruturas ou campos ao redor</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1.3 Texto completo de acrônimos comuns

Essa especificação usa acrônimos em uso comum no setor de computadores pessoais (consulte [Tabela 2](#table-2-full-text-of-common-acronyms)).

<div id="table-2-full-text-of-common-acronyms" />

**Tabela 2 Texto completo de acrônimos comuns**

| **Acrônimo** | **Texto Completo**                                      |
|-------------|----------------------------------------------------|
| ASCII       | American Standard Code for Information Interchange |
| BIOS        | Sistema de saída de entrada básico                          |
| CPU         | Unidade de Processamento Central                            |
| exFAT       | Tabela de alocação de arquivos extensível                   |
| FAT         | Tabela de alocação de arquivo                              |
| FAT12       | Tabela de Alocação de Arquivos, índices de cluster de 12 bits      |
| FAT16       | Tabela de Alocação de Arquivos, índices de cluster de 16 bits      |
| FAT32       | Tabela de Alocação de Arquivos, índices de cluster de 32 bits      |
| GPT         | Tabela de partição GUID                               |
| GUID        | Identificador global exclusivo (consulte [a Seção 10.1](#101-globally-unique-identifiers-guids))      |
| INT         | Interromper                                          |
| ativa a         | MBR (Registro Mestre de Inicialização)                                 |
| Texfat      | ExFAT seguro para transações                             |
| UTC         | Tempo Universal Coordenado UTC                         |

### <a name="14-default-field-and-structure-qualifiers"></a>1.4 Qualificadores padrão de campo e estrutura

Os campos e estruturas nesta especificação têm os qualificadores a seguir (veja a lista abaixo), a menos que a especificação adoeça o contrário.

1. Não assinados

2. Use a notação decimal para descrever valores, em que não foi notado de outra forma; essa especificação usa a letra pós-correção "h" para denotar números hexadecimais e inclui GUIDs entre chaves

3. Estão no formato little-endian

4. Não exigir um caractere de terminação nula para cadeias de caracteres

### <a name="15-windows-ce-and-texfat"></a>1,5 Windows CE e TexFAT

O TexFAT é uma extensão para exFAT que adiciona semântica operacional segura de transação sobre o sistema de arquivos base. O TexFAT é usado por Windows CE.
O TexFAT requer o uso dos dois FATs e bitmaps de alocação para uso em transações. Ele também define várias estruturas adicionais, incluindo descritores de preenchimento e descritores de segurança.

## <a name="2-volume-structure"></a>2 Estrutura de Volume

Um volume é o conjunto de todas as estruturas do sistema de arquivos e o espaço de dados necessário para armazenar e recuperar dados do usuário. Todos os volumes exFAT contêm quatro regiões (consulte [a Tabela 3](#table-3-volume-structure)).

<div id="table-3-volume-structure" />

**Estrutura de volume da Tabela 3**

<table>
<thead>
<tr class="header">
<th><strong>Nome da sub-região</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(setor)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(setores)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Região de inicialização principal</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Setor de inicialização principal</td>
<td>0</td>
<td>1</td>
<td>Essa sub-região é obrigatória e <a href="#31-main-and-backup-boot-sector-sub-regions">a Seção 3.1</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Principais setores de inicialização estendida</td>
<td>1</td>
<td>8</td>
<td>Essa sub-região é obrigatória e <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">a Seção 3.2</a>) define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Parâmetros principais do OEM</td>
<td>9</td>
<td>1</td>
<td>Essa sub-região é obrigatória e <a href="#33-main-and-backup-oem-parameters-sub-regions">a Seção 3.3</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Principal Reservado</td>
<td>10</td>
<td>1</td>
<td>Essa sub-região é obrigatória e seu conteúdo é reservado.</td>
</tr>
<tr class="even">
<td>Verificação de inicialização principal</td>
<td>11</td>
<td>1</td>
<td>Essa sub-região é obrigatória e <a href="#34-main-and-backup-boot-checksum-sub-regions">a Seção 3.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td><strong>Região de inicialização de backup</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Setor de inicialização de backup</td>
<td>12</td>
<td>1</td>
<td>Essa sub-região é obrigatória e <a href="#31-main-and-backup-boot-sector-sub-regions">a Seção 3.1</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Setores de inicialização estendida de backup</td>
<td>13</td>
<td>8</td>
<td>Essa sub-região é obrigatória e <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">a Seção 3.2</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Fazer backup de parâmetros OEM</td>
<td>21</td>
<td>1</td>
<td>Essa sub-região é obrigatória e <a href="#33-main-and-backup-oem-parameters-sub-regions">a Seção 3.3</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Backup Reservado</td>
<td>22</td>
<td>1</td>
<td>Essa sub-região é obrigatória e seu conteúdo é reservado.</td>
</tr>
<tr class="even">
<td>Verificação de inicialização de backup</td>
<td>23</td>
<td>1</td>
<td>Essa sub-região é obrigatória e <a href="#34-main-and-backup-boot-checksum-sub-regions">a Seção 3.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td><strong>Região fat</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Alinhamento fat</td>
<td>24</td>
<td>FatOffset – 24</td>
<td><p>Essa sub-região é obrigatória e seu conteúdo, se algum, é indefinido.</p>
<p>Observação: os setores principal e de inicialização de backup contêm o campo FatOffset.</p></td>
</tr>
<tr class="odd">
<td>Primeira FAT</td>
<td>FatOffset</td>
<td>FatLength</td>
<td><p>Essa sub-região é obrigatória e <a href="#41-first-and-second-fat-sub-regions">a Seção 4.1</a> define seu conteúdo.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm os campos FatOffset e FatLength.</p></td>
</tr>
<tr class="even">
<td>Segundo FAT</td>
<td>FatOffset + FatLength</td>
<td>FatLength * (NumberOfFats – 1)</td>
<td><p>Essa sub-região é obrigatória e <a href="#41-first-and-second-fat-sub-regions">a Seção 4.1</a> define seu conteúdo, se for o caso.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm os campos FatOffset, FatLength e NumberOfFats. O campo NumberOfFats só pode conter os valores 1 e 2.</p></td>
</tr>
<tr class="odd">
<td><strong>Região de dados</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Alinhamento do heap de cluster</td>
<td>FatOffset + FatLength * NumberOfFats</td>
<td>ClusterHeapOffset – (FatOffset + FatLength * NumberOfFats)</td>
<td><p>Essa sub-região é obrigatória e seu conteúdo, se algum, é indefinido.</p>
<p>Observação: os setores de inicialização principal e de backup contêm os campos FatOffset, FatLength, NumberOfFats e ClusterHeapOffset. Os valores válidos do campo NumberOfFats são 1 e 2.</p></td>
</tr>
<tr class="odd">
<td>Cluster Heap</td>
<td>ClusterHeapOffset</td>
<td>ClusterCount * 2<sup>SetoresPerClusterShift</sup></td>
<td><p>Essa sub-região é obrigatória e <a href="#51-cluster-heap-sub-region">a Seção 5.1</a> define seu conteúdo.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm os campos ClusterHeapOffset, ClusterCount e SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td>Espaço em excesso</td>
<td>ClusterHeapOffset + ClusterCount * 2<sup>SetoresPerClusterShift</sup></td>
<td>VolumeLength – (ClusterHeapOffset + ClusterCount * 2<sup>SetoresPerClusterShift</sup>)</td>
<td><p>Essa sub-região é obrigatória e seu conteúdo, se algum, é indefinido.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm os campos ClusterHeapOffset, ClusterCount, SectorsPerClusterShift e VolumeLength.</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3 Regiões de inicialização principal e de backup

A região inicialização principal fornece todas as instruções necessárias de inicialização, identificando informações e parâmetros do sistema de arquivos para permitir que uma implementação execute o seguinte:

1. Inicializar um sistema de computador de um volume exFAT.

2. Identifique o sistema de arquivos no volume como exFAT.

3. Descubra o local das estruturas do sistema de arquivos exFAT.

A região inicialização de backup é um backup da região inicialização principal. Ele auxilia na recuperação do volume exFAT no caso da região inicialização principal estar em um estado inconsistente. Exceto em circunstâncias pouco frequentes, como atualizar instruções de depuração de inicialização, as implementações não devem modificar o conteúdo da região de Inicialização de Backup.

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>3.1 Sub-regiões do setor de inicialização principal e de backup

O Setor de Inicialização Principal contém código para a desapropriação de inicialização de um volume exFAT e parâmetros exFAT fundamentais que descrevem a estrutura do volume (consulte [a Tabela 4](#table-4-main-and-backup-boot-sector-structure)). BIOS, MBR ou outros agentes de desinformação de inicialização podem inspecionar esse setor e podem carregar e executar as instruções de desinformação de inicialização contidas nele.

O Setor de Inicialização de Backup é um backup do Setor de Inicialização Principal e tem a mesma estrutura (consulte [Tabela 4](#table-4-main-and-backup-boot-sector-structure)). O Setor de Inicialização de Backup pode auxiliar nas operações de recuperação; No entanto, as implementações devem tratar o conteúdo dos campos VolumeFlags e PercentInUse como desalocar.

Antes de usar o conteúdo do Setor principal ou de inicialização de backup, as implementações deverão verificar seu conteúdo validando sua respectiva Verificação de Inicialização e garantindo que todos os seus campos estão dentro de seu intervalo de valor válido.

Embora a operação de formato inicialize o conteúdo dos Setores principal e de inicialização de backup, as implementações podem atualizar esses setores (e também atualizar a respectiva Verificação de Inicialização), conforme necessário. No entanto, as implementações podem atualizar os campos VolumeFlags ou PercentInUse sem atualizar sua respectiva Soma de Verificação de Inicialização (a soma de verificação exclui especificamente esses dois campos).

<div id="table-4-main-and-backup-boot-sector-structure" />

**Tabela 4 Principal e Estrutura do Setor de Inicialização de Backup**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JumpBoot</td>
<td>0</td>
<td>3</td>
<td>Esse campo é obrigatório e <a href="#311-jumpboot-field">a Seção 3.1.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>FileSystemName</td>
<td>3</td>
<td>8</td>
<td>Esse campo é obrigatório e <a href="#312-filesystemname-field">a Seção 3.1.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>MustBeZero</td>
<td>11</td>
<td>53</td>
<td>Esse campo é obrigatório e <a href="#313-mustbezero-field">a Seção 3.1.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>PartitionOffset</td>
<td>64</td>
<td>8</td>
<td>Esse campo é obrigatório e <a href="#314-partitionoffset-field">a Seção 3.1.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>VolumeLength</td>
<td>72</td>
<td>8</td>
<td>Esse campo é obrigatório <a href="#315-volumelength-field">e a Seção 3.1.5</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>FatOffset</td>
<td>80</td>
<td>4</td>
<td>Esse campo é obrigatório <a href="#316-fatoffset-field">e a Seção 3.1.6</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>FatLength</td>
<td>84</td>
<td>4</td>
<td>Esse campo é obrigatório <a href="#317-fatlength-field">e a Seção 3.1.7</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>ClusterHeapOffset</td>
<td>88</td>
<td>4</td>
<td>Esse campo é obrigatório <a href="#318-clusterheapoffset-field">e a Seção 3.1.8</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>ClusterCount</td>
<td>92</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#319-clustercount-field">a Seção 3.1.9</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>FirstClusterOfRootDirectory</td>
<td>96</td>
<td>4</td>
<td>Esse campo é obrigatório <a href="#3110-firstclusterofrootdirectory-field">e a Seção 3.1.10</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>Esse campo é obrigatório <a href="#3111-volumeserialnumber-field">e a Seção 3.1.11</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>FileSystemRevision</td>
<td>104</td>
<td>2</td>
<td>Esse campo é obrigatório <a href="#3112-filesystemrevision-field">e a Seção 3.1.12</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>VolumeFlags</td>
<td>106</td>
<td>2</td>
<td>Esse campo é obrigatório <a href="#3113-volumeflags-field">e a Seção 3.1.13</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>BytesPerSectorShift</td>
<td>108</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#3114-bytespersectorshift-field">e a Seção 3.1.14</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>SectorsPerClusterShift</td>
<td>109</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#3115-sectorsperclustershift-field">e a Seção 3.1.15</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>NumberOfFats</td>
<td>110</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#3116-numberoffats-field">e a Seção 3.1.16</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>DriveSelect</td>
<td>111</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#3117-driveselect-field">a Seção 3.1.17</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>PercentInUse</td>
<td>112</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#3118-percentinuse-field">a Seção 3.1.18</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>113</td>
<td>7</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="even">
<td>BootCode</td>
<td>120</td>
<td>390</td>
<td>Esse campo é obrigatório <a href="#3119-bootcode-field">e a Seção 3.1.19</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>BootSignature</td>
<td>510</td>
<td>2</td>
<td>Esse campo é obrigatório e <a href="#3120-bootsignature-field">a Seção 3.1.20</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Espaço em Excesso</td>
<td>512</td>
<td>2<sup>BytesPerSectorShift</sup> – 512</td>
<td><p>Esse campo é obrigatório e seu conteúdo, se algum, é indefinido.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm o campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 JumpBoot Field

O campo JumpBoot deve conter a instrução jump para CPUs comuns em computadores pessoais, que, quando executados, "salta" a CPU para executar as instruções de inicialização no campo BootCode.

O valor válido para esse campo é (na ordem de byte de ordem baixa para byte de ordem alta) EBh 76h 90h.

#### <a name="312-filesystemname-field"></a>3.1.2 Campo FileSystemName

O campo FileSystemName deve conter o nome do sistema de arquivos no volume.

O valor válido para esse campo é, em caracteres ASCII, "EXFAT", que inclui três espaços em branco à parte final.

#### <a name="313-mustbezero-field"></a>3.1.3 Campo MustBeZero

O campo MustBeZero deve corresponder diretamente ao intervalo de bytes que o bloco de parâmetro BIOS empacotado consome em volumes FAT12/16/32.

O valor válido para esse campo é 0, o que ajuda a impedir que implementações FAT12/16/32 montagem de um volume exFAT por engano.

#### <a name="314-partitionoffset-field"></a>3.1.4 Campo PartitionOffset

O campo PartitionOffset deve descrever o deslocamento de setor relativo à mídia da partição que hospeda o volume exFAT determinado. Esse campo auxilia na eliminação de problemas de inicialização do volume usando o INT estendido 13h em computadores pessoais.

Todos os valores possíveis para esse campo são válidos; no entanto, o valor 0 indica que as implementações deverão ignorar esse campo.

#### <a name="315-volumelength-field"></a>3.1.5 Campo VolumeLength

O campo VolumeLength deve descrever o tamanho do volume exFAT determinado em setores.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 2<sup>20/2</sup><sup>BytesPerSectorShift,</sup>o que garante que o menor volume não seja menor que 1 MB

- No máximo 2<sup>64</sup>a 1, o maior valor que esse campo pode descrever

No entanto, se o tamanho da sub-região Espaço em Excesso for 0, o valor desse campo será ClusterHeapOffset + (2<sup>32</sup>- 11) \* 2<sup>SectorsPerClusterShift</sup>.

#### <a name="316-fatoffset-field"></a>3.1.6 Campo FatOffset

O campo FatOffset deve descrever o deslocamento de setor relativo ao volume da Primeira FAT. Esse campo permite que as implementações alinhem o Primeiro FAT às características da mídia de armazenamento subjacente.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 24, que é responsável pelos setores que as regiões inicialização principal e inicialização de backup consomem

- No máximo ClusterHeapOffset – (FatLength NumberOfFats), que é responsável pelos setores que \* o Heap de Cluster consome

#### <a name="317-fatlength-field"></a>3.1.7 Campo FatLength

O campo FatLength deve descrever o comprimento, em setores, de cada tabela FAT (o volume pode conter até dois FATs).

O intervalo válido de valores para esse campo deve ser:

- Pelo menos (ClusterCount + 2) \* <sup>2 2/2</sup><sup>BytesPerSectorShift</sup>arredondado para cima até o inteiro mais próximo, o que garante que cada FAT tenha espaço suficiente para descrever todos os clusters no Heap de Cluster

- No máximo (ClusterHeapOffset – FatOffset) / NumberOfFats arredondado para baixo até o inteiro mais próximo, o que garante que as FATs existam antes do Heap de Cluster

Esse campo pode conter um valor além de seu limite inferior (conforme descrito acima) para permitir que a Segunda FAT, se presente, também seja alinhada às características da mídia de armazenamento subjacente. O conteúdo do espaço que excede o que o FAT em si exige, se algum, é indefinido.

#### <a name="318-clusterheapoffset-field"></a>3.1.8 Campo ClusterHeapOffset

O campo ClusterHeapOffset deve descrever o deslocamento de setor relativo ao volume do Heap de Cluster. Esse campo permite que as implementações alinhem o Heap de Cluster às características da mídia de armazenamento subjacente.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos FatOffset + FatLength NumberOfFats, para levar em conta os setores que \* todas as regiões anteriores consomem

- No máximo 2<sup>32</sup>- 1 ou VolumeLength - (ClusterCount \* 2<sup>SectorsPerClusterShift</sup>), o cálculo que for menor

#### <a name="319-clustercount-field"></a>3.1.9 Campo ClusterCount

O campo ClusterCount deve descrever o número de clusters que o Heap de Cluster contém.

O valor válido para esse campo deve ser o menor dos seguintes:

- (VolumeLength – ClusterHeapOffset) /2<sup>SectorsPerClusterShift</sup>arredondado para baixo até o inteiro mais próximo, que é exatamente o número de clusters que podem se ajustar entre o início do Heap de Cluster e o final do volume

- 2<sup>32</sup>a 11, que é o número máximo de clusters que uma FAT pode descrever

O valor do campo ClusterCount determina o tamanho mínimo de uma FAT. Para evitar faTs extremamente grandes, as implementações podem controlar o número de clusters no Heap de Cluster aumentando o tamanho do cluster (por meio do campo SectorsPerClusterShift). Essa especificação não recomenda mais de 2<sup>clusters 24</sup>a 2 no Heap de Cluster. No entanto, as implementações devem ser capazes de lidar com volumes com até 2<sup>clusters de 32</sup>a 11 no Heap de Cluster.

#### <a name="3110-firstclusterofrootdirectory-field"></a>3.1.10 Campo FirstClusterOfRootDirectory

O campo FirstClusterOfRootDirectory deve conter o índice de cluster do primeiro cluster do diretório raiz. As implementações devem fazer todos os esforços para colocar o primeiro cluster do diretório raiz no primeiro cluster não ruim após os clusters que o Bitmap de Alocação e a Tabela de Caso Up consomem.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 2, o índice do primeiro cluster no Heap de Cluster

- No máximo ClusterCount + 1, o índice do último cluster no Heap de Cluster

#### <a name="3111-volumeserialnumber-field"></a>3.1.11 Campo VolumeSerialNumber

O campo VolumeSerialNumber deve conter um número de série exclusivo. Isso ajuda as implementações a distinguir entre diferentes volumes exFAT.
As implementações devem gerar o número de série combinando a data e a hora da formatação do volume exFAT. O mecanismo para combinar data e hora para formar um número de série é específico da implementação.

Todos os valores possíveis para esse campo são válidos.

#### <a name="3112-filesystemrevision-field"></a>3.1.12 Campo FileSystemRevision

O campo FileSystemRevision deve descrever os números de revisão principais e secundários das estruturas exFAT no volume determinado.

O byte de ordem alta é o número de revisão principal e o byte de ordem baixa é o número de revisão secundária. Por exemplo, se o byte de ordem alta contiver o valor 01h e se o byte de ordem baixa contiver o valor 05h, o campo FileSystemRevision descreverá o número de revisão 1,05.
Da mesma forma, se o byte de ordem alta contiver o valor 0Ah e se o byte de ordem baixa contiver o valor 0Fh, o campo FileSystemRevision descreverá o número de revisão 10,15.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 0 para o byte de ordem baixa e 1 para o byte de ordem alta

- No máximo 99 para o byte de ordem baixa e 99 para o byte de ordem alta

O número de revisão de exFAT que essa especificação descreve é 1,00.
Implementações dessa especificação devem montar qualquer volume exFAT com o número de revisão principal 1 e não devem montar nenhum volume exFAT com qualquer outro número de revisão principal. As implementações devem cumprir o número de revisão secundária e não devem executar operações ou criar estruturas do sistema de arquivos não descritas na especificação correspondente do número de revisão secundária determinado.

#### <a name="3113-volumeflags-field"></a>3.1.13 Campo VolumeFlags

O campo VolumeFlags deve conter sinalizadores que indicam o status de várias estruturas do sistema de arquivos no volume exFAT (consulte [a Tabela 5](#table-5-volumeflags-field-structure)).

As implementações não devem incluir esse campo ao computar sua respectiva inicialização principal ou uma verificação de região de inicialização de backup. Ao fazer referência ao Setor de Inicialização de Backup, as implementações deverão tratar esse campo como desaloqueado.

<div id="table-5-volumeflags-field-structure" />

**Estrutura do campo VolumeFlags da Tabela 5**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ActiveFat</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#31131-activefat-field">e a Seção 3.1.13.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#31132-volumedirty-field">e a Seção 3.1.13.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>MediaFailure</td>
<td>2</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#31133-mediafailure-field">e a Seção 3.1.13.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>ClearToZero</td>
<td>3</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#31134-cleartozero-field">e a Seção 3.1.13.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>4</td>
<td>12</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>Campo ActiveFat 3.1.13.1

O campo ActiveFat deve descrever qual FAT e Bitmap de Alocação estão ativos (e as implementações devem usar), da seguinte forma:

- 0, o que significa que o primeiro fat e o bitmap de primeira alocação estão ativos

- 1, o que significa que o segundo fat e o segundo bitmap de alocação estão ativos e só é possível quando o campo NumberOfFats contém o valor 2

As implementações devem considerar o FAT inativo e o Bitmap de Alocação como desleis. Somente as implementações com conhecimento de TexFAT devem alternar os bitmaps fat e alocação ativos (consulte [a Seção 7.1](#71-allocation-bitmap-directory-entry)).

##### <a name="31132-volumedirty-field"></a>3.1.13.2 Campo VolumeDirty

O campo VolumeDirty deve descrever se o volume está sujo ou não, da seguinte forma:

- 0, o que significa que o volume provavelmente está em um estado consistente

- 1, o que significa que o volume provavelmente está em um estado inconsistente

As implementações devem definir o valor desse campo como 1 ao encontrar inconsistências de metadados do sistema de arquivos que elas não resolvem. Se, ao montar um volume, o valor desse campo for 1, somente implementações que resolvem inconsistências de metadados do sistema de arquivos poderão limpar o valor desse campo como 0. Essas implementações só deverão limpar o valor desse campo para 0 depois de garantir que o sistema de arquivos está em um estado consistente.

Se, ao montar um volume, o valor desse campo for 0, as implementações deverão definir esse campo como 1 antes de atualizar os metadados do sistema de arquivos e limpar esse campo como 0 posteriormente, semelhante à ordenação de gravação recomendada descrita na Seção [8.1](#81-recommended-write-ordering).

##### <a name="31133-mediafailure-field"></a>3.1.13.3 Campo MediaFailure

O campo MediaFailure deve descrever se uma implementação descobriu falhas de mídia ou não, da seguinte forma:

- 0, o que significa que a mídia de hospedagem não relatou falhas ou nenhuma falha conhecida já está registrada no FAT como clusters "ruins"

- 1, o que significa que a mídia de hospedagem relatou falhas (ou seja, operações de leitura ou gravação com falha)

Uma implementação deve definir esse campo como 1 quando:

1. A mídia de hospedagem falha nas tentativas de acesso a qualquer região no volume

2. A implementação esgotou os algoritmos de repetição de acesso, se houver

Se, após a montagem de um volume, o valor desse campo for 1, implementações que verificam o volume inteiro em busca de falhas de mídia e registram todas as falhas como clusters "ruins" na FAT (ou, caso contrário, resolvem falhas de mídia) podem limpar o valor desse campo como 0.

##### <a name="31134-cleartozero-field"></a>Campo 3.1.13.4 ClearToZero

O campo ClearToZero não tem significado significativo nessa especificação.

Os valores válidos para esse campo são:

- 0, que não tem nenhum significado específico

- 1, o que significa que as implementações devem limpar esse campo para 0 antes de modificar quaisquer estruturas, diretórios ou arquivos do sistema de arquivos

#### <a name="3114-bytespersectorshift-field"></a>Campo 3.1.14 BytesPerSectorShift

O campo BytesPerSectorShift deve descrever os bytes por setor, expressos como log<sub>2</sub>(N), em que N é o número de bytes por setor. Por exemplo, para 512 bytes por setor, o valor desse campo é 9.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 9 (tamanho de setor de 512 bytes), que é o menor setor possível para um volume exFAT

- No máximo 12 (tamanho do setor de 4096 bytes), que é o tamanho da página de memória de CPUs comuns em computadores pessoais

#### <a name="3115-sectorsperclustershift-field"></a>Campo 3.1.15 SectorsPerClusterShift

O campo SectorsPerClusterShift deve descrever os setores por cluster expressos como log<sub>2</sub>(N), em que N é o número de setores por cluster. Por exemplo, para 8 setores por cluster, o valor desse campo é 3.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 0 (1 setor por cluster), que é o menor cluster possível

- No máximo 25 BytesPerSectorShift, que é avaliado como um tamanho de cluster de 32 MB

#### <a name="3116-numberoffats-field"></a>Campo 3.1.16 NumberOfFats

O campo NumberOfFats deve descrever o número de bitmaps de alocação e de FATs que o volume contém.

O intervalo válido de valores para esse campo deve ser:

- 1, que indica que o volume contém apenas o primeiro bitmap de FAT e primeiro de alocação

- 2, que indica que o volume contém o primeiro FAT, segundo FAT, primeiro bitmap de alocação e bitmap de segunda alocação; Esse valor só é válido para volumes TexFAT

#### <a name="3117-driveselect-field"></a>Campo 3.1.17 DriveSelect

O campo DriveSelect deve conter o número da unidade INT 13h estendida, que ajuda o boot-Strapping desse volume usando INT estendida em computadores pessoais.

Todos os valores possíveis para esse campo são válidos. Campos semelhantes em sistemas de arquivos baseados em FAT anteriores continham com frequência o valor 80h.

#### <a name="3118-percentinuse-field"></a>Campo 3.1.18 PercentInUse

O campo PercentInUse deve descrever a porcentagem de clusters no heap de cluster que são alocados.

O intervalo válido de valores para esse campo deve ser:

- Entre 0 e 100, inclusive, que é a porcentagem de clusters alocados no heap de cluster, arredondado para baixo até o número inteiro mais próximo

- Exatamente FFh, que indica que a porcentagem de clusters alocados no heap de cluster não está disponível

As implementações devem alterar o valor desse campo para refletir as alterações na alocação de clusters no heap de cluster ou alterá-lo para FFh.

As implementações não devem incluir esse campo ao calcular sua respectiva soma de verificação de inicialização principal ou de região de inicialização de backup. Ao fazer referência ao setor de inicialização de backup, as implementações devem tratar esse campo como obsoleto.

#### <a name="3119-bootcode-field"></a>Campo de inicialização do 3.1.19

O campo inicialização deve conter instruções boot-Strapping.
As implementações podem preencher esse campo com as instruções de CPU necessárias para o boot-Strapping um sistema de computador. As implementações que não fornecem instruções boot-Strapping devem inicializar cada byte nesse campo para F4h (a instrução Halt para CPUs comuns em computadores pessoais) como parte de sua operação de formatação.

#### <a name="3120-bootsignature-field"></a>Campo 3.1.20 BootSignature

O campo BootSignature deve descrever se a intenção de um determinado setor é que ele seja um setor de inicialização ou não.

O valor válido para esse campo é AA55h. Qualquer outro valor neste campo invalida seu respectivo setor de inicialização. As implementações devem verificar o conteúdo desse campo antes de depender de qualquer outro campo em seu respectivo setor de inicialização.

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3,2 principais e fazer backup de subregiãos de setores de inicialização estendida

Cada setor dos principais setores de inicialização estendida tem a mesma estrutura; no entanto, cada setor pode conter instruções distintas de inicialização Strapping (consulte a tabela 6). Os agentes boot-Strapping, como as instruções boot-Strapping no setor de inicialização principal, implementações alternativas de BIOS ou um firmware de sistema incorporado, podem carregar esses setores e executar as instruções que eles contêm.

Os setores de inicialização estendidos de backup são um backup dos principais setores de inicialização estendidos e têm a mesma estrutura (consulte a [tabela 6](#table-6-extended-boot-sector-structure)).

Antes de executar as instruções dos setores de inicialização principal ou de backup estendidos, as implementações devem verificar seu conteúdo garantindo que o campo ExtendedBootSignature de cada setor contenha seu valor prescrito.

Enquanto a operação de formatação inicial inicializará o conteúdo dos setores de inicialização estendidos principal e de backup, as implementações poderão atualizar esses setores (e também atualizarão sua respectiva soma de verificação de inicialização) conforme necessário.

<div id="table-6-extended-boot-sector-structure" />

**Tabela 6 estrutura do setor de inicialização estendida**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>minuciosa</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ExtendedBootCode</td>
<td>0</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td><p>Esse campo é obrigatório e a <a href="#321-extendedbootcode-field">seção 3.2.1</a> define seu conteúdo.</p>
<p>Observação: os setores de inicialização principal e de backup contêm o campo BytesPerSectorShift.</p></td>
</tr>
<tr class="even">
<td>ExtendedBootSignature</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td>4</td>
<td><p>Esse campo é obrigatório e a <a href="#322-extendedbootsignature-field">seção 3.2.2</a> define seu conteúdo.</p>
<p>Observação: os setores de inicialização principal e de backup contêm o campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 campo ExtendedBootCode

O campo ExtendedBootCode deve conter instruções boot-Strapping.
As implementações podem preencher esse campo com as instruções de CPU necessárias para o boot-Strapping um sistema de computador. As implementações que não fornecem instruções boot-Strapping devem inicializar cada byte nesse campo para 17h como parte de sua operação de formatação.

#### <a name="322-extendedbootsignature-field"></a>Campo 3.2.2 ExtendedBootSignature

O campo ExtendedBootSignature deve descrever se a intenção de um determinado setor é que ele seja um setor de inicialização estendido ou não.

O valor válido para esse campo é AA550000h. Qualquer outro valor neste campo invalida seu respectivo setor de inicialização principal ou de backup estendido.
As implementações devem verificar o conteúdo deste campo antes de depender de qualquer outro campo em seu respectivo setor de inicialização estendido.

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>3,3 sub-regiões de parâmetros de OEM principal e de backup

A sub-região de parâmetros OEM principal contém dez estruturas de parâmetros que podem conter informações específicas do fabricante (consulte a [tabela 7](#table-7-oem-parameters-structure)). Cada uma das dez estruturas de parâmetros deriva do modelo de parâmetros genéricos (consulte a [seção 3.3.2](#332-generic-parameters-template)). Os fabricantes podem derivar suas próprias estruturas de parâmetros personalizados do modelo de parâmetros genéricos. Essa especificação em si define duas estruturas de parâmetros: parâmetros nulos (consulte a [seção 3.3.3](#333-null-parameters)) e os parâmetros do flash (consulte a [seção 3.3.4](#334-flash-parameters)).

Os parâmetros OEM de backup são um backup dos parâmetros principais do OEM e têm a mesma estrutura (consulte a [tabela 7](#table-7-oem-parameters-structure)).

Antes de usar o conteúdo dos parâmetros de OEM principal ou de backup, as implementações devem verificar seu conteúdo Validando sua respectiva soma de verificação de inicialização.

Os fabricantes devem preencher os parâmetros de OEM principal e de backup com suas próprias estruturas de parâmetros personalizados, se houver, e quaisquer outras estruturas de parâmetro. As operações de formato subsequentes devem preservar o conteúdo dos parâmetros de OEM principal e de backup.

As implementações podem atualizar os parâmetros de OEM principal e de backup conforme necessário (e também devem atualizar sua respectiva soma de verificação de inicialização).

<div id="table-7-oem-parameters-structure" />

**Estrutura de parâmetros OEM da tabela 7**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>minuciosa</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parâmetros [0]</td>
<td>0</td>
<td>48</td>
<td>Esse campo é obrigatório e a <a href="#331-parameters0--parameters9">seção 3.3.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Parâmetros [9]</td>
<td>432</td>
<td>48</td>
<td>Esse campo é obrigatório e a <a href="#331-parameters0--parameters9">seção 3.3.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>480</td>
<td>2<sup>BytesPerSectorShift</sup> – 480</td>
<td><p>Esse campo é obrigatório e seu conteúdo é reservado.</p>
<p>Observação: os setores de inicialização principal e de backup contêm o campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>parâmetros de 3.3.1 \[ 0 \] ... Parâmetros \[ 9\]

Cada campo de parâmetros nessa matriz contém uma estrutura de parâmetros, que deriva do modelo de parâmetros genéricos (consulte a [seção 3.3.2](#332-generic-parameters-template)).
Qualquer campo de parâmetros não utilizados deve ser descrito como contendo uma estrutura de parâmetros nulos (consulte a [seção 3.3.3](#333-null-parameters)).

#### <a name="332-generic-parameters-template"></a>Modelo de parâmetros genéricos do 3.3.2

O modelo de parâmetros genéricos fornece a definição de base de uma estrutura de parâmetros (consulte a [tabela 8](#table-8-generic-parameters-template)). Todas as estruturas de parâmetros derivam deste modelo. O suporte para este modelo de parâmetros genéricos é obrigatório.

<div id="table-8-generic-parameters-template" />

**Tabela 8 modelo de parâmetros genéricos**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>minuciosa</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Esse campo é obrigatório e a <a href="#3321-parametersguid-field">seção 3.3.2.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>16</td>
<td>32</td>
<td>Esse campo é obrigatório e as estruturas que derivam desse modelo definem seu conteúdo.</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>Campo 3.3.2.1 ParametersGuid

O campo ParametersGuid deve descrever um GUID, que determina o layout do restante da estrutura de parâmetros especificada.

Todos os valores possíveis para esse campo são válidos; no entanto, os fabricantes devem usar uma ferramenta de geração de GUID, como GuidGen.exe, para selecionar um GUID ao derivar estruturas de parâmetros personalizados desse modelo.

#### <a name="333-null-parameters"></a>3.3.3 parâmetros nulos

A estrutura de parâmetros nulos deriva do modelo de parâmetros genéricos (consulte a [seção 3.3.2](#332-generic-parameters-template)) e deve descrever um campo de parâmetros não utilizados (consulte a [tabela 9](#table-9-null-parameters-structure)). Ao criar ou atualizar a estrutura de parâmetros OEM, as implementações devem preencher os campos de parâmetros não utilizados com a estrutura de parâmetros NULL. Além disso, ao criar ou atualizar a estrutura de parâmetros OEM, as implementações devem consolidar as estruturas de parâmetros nulos no final da matriz, deixando, assim, todas as outras estruturas de parâmetros no início da estrutura de parâmetros OEM.

O suporte para a estrutura de parâmetros nulos é obrigatório.

<div id="table-9-null-parameters-structure" />

**Tabela 9 estrutura de parâmetros nulos**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>minuciosa</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Esse campo é obrigatório e a <a href="#3331-parametersguid-field">seção 3.3.3.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>16</td>
<td>32</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>Campo 3.3.3.1 ParametersGuid

O campo ParametersGuid deve estar em conformidade com a definição fornecida pelo modelo de parâmetros genéricos (consulte a [seção 3.3.2.1](#3321-parametersguid-field)).

O valor válido para esse campo, em notação GUID, é {00000000-0000-0000-0000-000000000000} .

#### <a name="334-flash-parameters"></a>Parâmetros do 3.3.4 Flash

A estrutura do parâmetro flash deriva do modelo de parâmetros genéricos (consulte a [seção 3.3.2](#332-generic-parameters-template)) e contém parâmetros para mídia flash (consulte a [tabela 10](#table-10-flash-parameters-structure)). Os fabricantes de dispositivos de armazenamento baseados em Flash podem preencher um campo de parâmetros (preferivelmente o \[ campo parâmetros 0 \] ) com essa estrutura de parâmetros. As implementações podem usar as informações na estrutura de parâmetros do flash para otimizar as operações de acesso durante leituras/gravações e para o alinhamento das estruturas do sistema de arquivos Durning formatação da mídia.

O suporte para a estrutura de parâmetros flash é opcional.

<div id="table-10-flash-parameters-structure" />

**Tabela 10-estrutura de parâmetros flash**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>minuciosa</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Esse campo é obrigatório e a <a href="#3341-parametersguid-field">seção 3.3.4.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>EraseBlockSize</td>
<td>16</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#3342-eraseblocksize-field">seção 3.3.4.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#3343-pagesize-field">seção 3.3.4.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>SpareSectors</td>
<td>24</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#3344-sparesectors-field">seção 3.3.4.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>RandomAccessTime</td>
<td>28</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#3345-randomaccesstime-field">seção 3.3.4.5</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Programaçãotime</td>
<td>32</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#3346-programmingtime-field">seção 3.3.4.6</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>ReadCycle</td>
<td>36</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#3347-readcycle-field">seção 3.3.4.7</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>WriteCycle</td>
<td>40</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#3348-writecycle-field">seção 3.3.4.8</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>44</td>
<td>4</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
</tbody>
</table>

Todos os valores possíveis para todos os campos de parâmetros de flash, exceto para o campo ParametersGuid, são válidos. No entanto, o valor 0 indica que o campo é, na verdade, sem sentido (as implementações devem ignorar o campo fornecido).

##### <a name="3341-parametersguid-field"></a>Campo 3.3.4.1 ParametersGuid

O campo ParametersGuid deve estar em conformidade com a definição fornecida no modelo de parâmetros genéricos (consulte a [seção 3.3.2.1](#3321-parametersguid-field)).

O valor válido para esse campo, na notação GUID, é {0A0C7E46-3399-4021-90C8-FA6D389C4BA2}.

##### <a name="3342-eraseblocksize-field"></a>Campo 3.3.4.2 EraseBlockSize

O campo EraseBlockSize deve descrever o tamanho, em bytes, do bloco erase da mídia flash.

##### <a name="3343-pagesize-field"></a>Campo 3.3.4.3 PageSize

O campo PageSize deve descrever o tamanho, em bytes da página da mídia flash.

##### <a name="3344-sparesectors-field"></a>Campo 3.3.4.4 SpareSectors

O campo SpareSectors deve descrever o número de setores que a mídia flash está disponível para suas operações de sparing internas.

##### <a name="3345-randomaccesstime-field"></a>Campo 3.3.4.5 RandomAccessTime

O campo RandomAccessTime deve descrever o tempo médio de acesso aleatório da mídia flash, em nanossegundos.

##### <a name="3346-programmingtime-field"></a>3.3.4.6 campo de programação

O campo Programaçãotime deve descrever o tempo médio de programação da mídia flash, em nanossegundos.

##### <a name="3347-readcycle-field"></a>Campo 3.3.4.7 ReadCycle

O campo ReadCycle deve descrever o tempo médio de ciclo de leitura da mídia flash, em nanossegundos.

##### <a name="3348-writecycle-field"></a>Campo 3.3.4.8 WriteCycle

O campo WriteCycle deve descrever o tempo médio do ciclo de gravação, em nanossegundos.

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3,4 sub-regiões de soma de verificação de inicialização de backup e principal

As somas de verificação de inicialização principal e de backup contêm um padrão de repetição da soma de verificação de quatro bytes do conteúdo de todas as outras subregiãos em suas respectivas regiões de inicialização. O cálculo da soma de verificação não deve incluir os campos VolumeFlags e PercentInUse em seu respectivo setor de inicialização (consulte a [Figura 1](#figure-1-boot-checksum-computation)). O padrão de repetição da soma de verificação de quatro bytes preenche sua respectiva sub-região de soma de verificação de inicialização do início ao fim da sub-região.

Antes de usar o conteúdo de qualquer uma das outras subregiãos nas regiões de inicialização principal ou de backup, as implementações devem verificar seu conteúdo Validando sua respectiva soma de verificação de inicialização.

Enquanto a operação de formatação inicial preencherá as somas de verificação de inicialização principal e de backup com o padrão de soma de verificação repetida, as implementações deverão atualizar esses setores à medida que o conteúdo dos outros setores em suas respectivas regiões de inicialização forem alterados.

<div id="figure-1-boot-checksum-computation" />

**Figura 1 computação da soma de verificação de inicialização**

```c
UInt32 BootChecksum
(
    UCHAR  * Sectors,        // points to an in-memory copy of the 11 sectors
    USHORT   BytesPerSector
)
{
    UInt32 NumberOfBytes = (UInt32)BytesPerSector * 11;
    UInt32 Checksum = 0;
    UInt32 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 106) || (Index == 107) || (Index == 112))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Sectors[Index];
    }

    return Checksum;
}
```

## <a name="4-file-allocation-table-region"></a>4 região da tabela de alocação de arquivos

A região da tabela de alocação de arquivo (FAT) pode conter até duas FATs, uma na primeira sub-região de FAT e outra na segunda sub-região de FAT.
O campo NumberOfFats descreve quantas FATs esta região contém. Os valores válidos para o campo NumberOfFats são 1 e 2. Portanto, a primeira sub-região de FAT sempre contém um FAT. Se o campo NumberOfFats for dois, a segunda sub-região de FAT também conterá um FAT.

O campo ActiveFat do campo VolumeFlags descreve qual FAT está ativo. Somente o campo VolumeFlags no setor de inicialização principal é atual.
As implementações devem tratar o FAT que não está ativo como obsoleto. O uso do FAT inativo e a alternância entre FATs é específico da implementação.

### <a name="41-first-and-second-fat-sub-regions"></a>4,1 primeira e segunda subregiãos de FAT

Uma FAT deve descrever as cadeias de cluster no heap de cluster (consulte a [tabela 11](#table-11-file-allocation-table-structure)).
Uma cadeia de cluster é uma série de clusters que fornece espaço para gravar o conteúdo de arquivos, diretórios e outras estruturas do sistema de arquivos. Um FAT representa uma cadeia de cluster como uma lista vinculada individualmente de índices de cluster. Com exceção das duas primeiras entradas, cada entrada em uma FAT representa exatamente um cluster.

<div id="table-11-file-allocation-table-structure" />

**Tabela 11 estrutura da tabela de alocação de arquivos**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>minuciosa</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FatEntry [0]</td>
<td>0</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#412-fatentry1-field">seção 4.1.2</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>FatEntry [1]</td>
<td>4</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#412-fatentry1-field">seção 4.1.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>FatEntry [2]</td>
<td>8</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#413-fatentry2--fatentryclustercount1-fields">seção 4.1.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>FatEntry [ClusterCount + 1]</td>
<td>(ClusterCount + 1) * 4</td>
<td>4</td>
<td><p>Esse campo é obrigatório e a <a href="#413-fatentry2--fatentryclustercount1-fields">seção 4.1.3</a> define seu conteúdo.</p>
<p>ClusterCount + 1 nunca pode exceder FFFFFFF6h.</p>
<p>Observação: os setores de inicialização principal e de backup contêm o campo ClusterCount.</p></td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>(ClusterCount + 2) * 4</td>
<td>(FatLength * 2<sup>BytesPerSectorShift</sup>) – ((ClusterCount + 2) * 4)</td>
<td><p>Esse campo é obrigatório e seu conteúdo, se houver, é indefinido.</p>
<p>Observação: os setores de inicialização principal e de backup contêm os campos ClusterCount, FatLength e BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>Campo 4.1.1 FatEntry \[ 0 \]

O \[ campo FatEntry 0 \] deve descrever o tipo de mídia no primeiro byte (o byte de ordem mais baixo) e deve conter FFH nos três bytes restantes.

O tipo de mídia (o primeiro byte) deve ser F8h.

#### <a name="412-fatentry1-field"></a>Campo 4.1.2 FatEntry \[ 1 \]

O \[ campo FatEntry 1 \] existe apenas devido à precedência histórica e não descreve nada de interesse.

O valor válido para esse campo é FFFFFFFFh. As implementações deverão inicializar esse campo para seu valor prescrito e não deve usar esse campo para qualquer finalidade. As implementações não devem interpretar esse campo e preservar seu conteúdo entre operações que modificam campos ao redor.

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 FatEntry \[ 2 \] ... FatEntry \[ ClusterCount + 1 \] campos

Cada campo FatEntry nessa matriz deve representar um cluster no heap de cluster. FatEntry \[ 2 \] representa o primeiro cluster no heap de cluster e FatEntry \[ ClusterCount + 1 \] representa o último cluster no heap de cluster.

O intervalo válido de valores para esses campos deve ser:

- Entre 2 e ClusterCount + 1, inclusive, que aponta para o próximo FatEntry na cadeia de cluster determinada; o FatEntry fornecido não deve apontar para nenhum FatEntry que o preceda na cadeia de clusters especificada

- Exatamente FFFFFFF7h, que marca o cluster correspondente do FatEntry especificado como "Bad"

- Exatamente FFFFFFFFh, que marca o cluster correspondente do FatEntry como o último cluster de uma cadeia de cluster; Esse é o único valor válido para a última FatEntry de qualquer cadeia de cluster determinada

## <a name="5-data-region"></a>5 região de dados

A região de dados contém o heap de cluster, que fornece espaço gerenciado para estruturas, diretórios e arquivos do sistema de arquivos.

### <a name="51-cluster-heap-sub-region"></a>5,1 sub-região de heap de cluster

A estrutura do heap de cluster é muito simples (consulte a [tabela 12](#table-12-cluster-heap-structure)); cada série de setores consecutivos descreve um cluster, como o campo SectorsPerClusterShift define. Importante, o primeiro cluster do heap de cluster tem o índice dois, que corresponde diretamente ao índice de FatEntry \[ 2 \] .

Em um volume exFAT, um bitmap de alocação (consulte a [seção 7.1.5](#715-allocation-bitmap)) mantém o registro do estado de alocação de todos os clusters. Essa é uma diferença significativa das predecessoras do exFAT (FAT12, FAT16 e FAT32), em que uma FAT manteve um registro do estado de alocação de todos os clusters no heap de cluster.

<div id="table-12-cluster-heap-structure" />

**Tabela 12 estrutura de heap de cluster**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(setor)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(setores)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cluster[2]</td>
<td>ClusterHeapOffset</td>
<td>2<sup>SetoresPerClusterShift</sup></td>
<td><p>Esse campo é obrigatório e <a href="#511-cluster2--clusterclustercount1-fields">a Seção 5.1.1</a> define seu conteúdo.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm os campos ClusterHeapOffset e SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Cluster[ClusterCount+1]</td>
<td>ClusterHeapOffset + (ClusterCount – 1) * 2<sup>SectorsPerClusterShift</sup></td>
<td>2<sup>SetoresPerClusterShift</sup></td>
<td><p>Esse campo é obrigatório e <a href="#511-cluster2--clusterclustercount1-fields">a Seção 5.1.1</a> define seu conteúdo.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm os campos ClusterCount, ClusterHeapOffset e SectorsPerClusterShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 Cluster \[ \] 2... Cluster \[ ClusterCount+1 \] Campos

Cada campo cluster nessa matriz é uma série de setores contíguos, cujo tamanho é definido pelo campo SectorsPerClusterShift.

## <a name="6-directory-structure"></a>Estrutura de 6 diretórios

O sistema de arquivos exFAT usa uma abordagem de árvore de diretório para gerenciar as estruturas e arquivos do sistema de arquivos que existem no Heap de Cluster. Os diretórios têm uma relação um-para-muitos entre pai e filho na árvore de diretórios.

O diretório ao qual o campo FirstClusterOfRootDirectory se refere é a raiz da árvore de diretórios. Todos os outros diretórios são descendentes do diretório raiz de maneira vinculada.

Cada diretório consiste em uma série de entradas de diretório (consulte [Tabela 13](#table-13-directory-structure)).

Uma ou mais entradas de diretório são combinadas em um conjunto de entradas de diretório que descreve algo de interesse, como uma estrutura do sistema de arquivos, subdados ou arquivo.

<div id="table-13-directory-structure" />

**Estrutura de diretório da Tabela 13**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DirectoryEntry[0]</td>
<td>0</td>
<td>32</td>
<td>Esse campo é obrigatório e <a href="#61-directoryentry0--directoryentryn--1">a Seção 6.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>DirectoryEntry[N-1]</td>
<td>(N – 1) * 32</td>
<td>32</td>
<td><p>Esse campo é obrigatório e <a href="#61-directoryentry0--directoryentryn--1">a Seção 6.1</a> define seu conteúdo.</p>
<p>N, o número de campos DirectoryEntry, é o tamanho, em bytes, da cadeia de clusters que contém o diretório determinado, dividido pelo tamanho de um campo DirectoryEntry, 32 bytes.</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6.1 DirectoryEntry \[ 0 \] ... DirectoryEntry \[ N--1\]

Cada campo DirectoryEntry nessa matriz deriva do modelo DirectoryEntry Genérico (consulte [a Seção 6.2](#62-generic-directoryentry-template)).

### <a name="62-generic-directoryentry-template"></a>6.2 Modelo directoryentry genérico

O modelo Generic DirectoryEntry fornece a definição base para entradas de diretório (consulte [Tabela 14](#table-14-generic-directoryentry-template)). Todas as estruturas de entrada de diretório derivam desse modelo e somente as estruturas de entrada de diretório definidas pela Microsoft são válidas (o exFAT não tem provisionamentos para estruturas de entrada de diretório definidas pelo fabricante, exceto conforme definido nas Seções [7.8](#78-vendor-extension-directory-entry) e [7.9](#79-vendor-allocation-directory-entry)). A capacidade de interpretar o modelo DirectoryEntry Genérico é obrigatória.

<div id="table-14-generic-directoryentry-template" />

**Tabela 14 Modelo directoryentry genérico**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#621-entrytype-field">e a Seção 6.2.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>1</td>
<td>19</td>
<td>Esse campo é obrigatório e as estruturas que derivam desse modelo podem definir seu conteúdo.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#622-firstcluster-field">a Seção 6.2.2</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Datalength</td>
<td>24</td>
<td>8</td>
<td>Esse campo é obrigatório e <a href="#623-datalength-field">a Seção 6.2.3</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>Campo EntryType 6.2.1

O campo EntryType tem três modos de uso que o valor do campo define (consulte a lista abaixo).

- 00h, que é um marcador de fim de diretório e as seguintes condições se aplicam:

  - Todos os outros campos no DirectoryEntry determinado são realmente reservados

  - Todas as entradas de diretório subsequentes no diretório determinado também são marcadores de fim de diretório

  - Marcadores de fim de diretório são válidos apenas fora dos conjuntos de entrada de diretório

  - As implementações podem substituir marcadores de fim de diretório conforme necessário

- Entre 01h e 7Fh, inclusive, que é um marcador de entrada de diretório não usuário e as seguintes condições se aplicam:

  - Todos os outros campos no DirectoryEntry determinado são, na verdade, indefinido

  - Entradas de diretório nãousadas só são válidas fora dos conjuntos de entrada de diretório

  - As implementações podem substituir entradas de diretório nãousadas conforme necessário

  - Esse intervalo de valores corresponde ao campo InUse (consulte a Seção [6.2.1.4](#6214-inuse-field)) que contém o valor 0

- Entre 81h e FFh, inclusive, que é uma entrada de diretório regular e as seguintes condições se aplicam:

  - O conteúdo do campo EntryType (consulte [Tabela 15](#table-15-generic-entrytype-field-structure)) determina o layout do restante da estrutura DirectoryEntry

  - Esse intervalo de valores e apenas esse intervalo de valores são válidos dentro de um conjunto de entradas de diretório

  - Esse intervalo de valores corresponde diretamente ao campo InUse (consulte a Seção [6.2.1.4](#6214-inuse-field)) que contém o valor 1

Para evitar modificações no campo InUse (consulte a Seção [6.2.1.4](#6214-inuse-field)) resultando erroneamente em um marcador de fim de diretório, o valor 80h é inválido.

<div id="table-15-generic-entrytype-field-structure" />

**Estrutura de campo EntryType Genérico da Tabela 15**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>Esse campo é obrigatório e <a href="#6211-typecode-field">a Seção 6.2.1.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>TypeImportance</td>
<td>5</td>
<td>1</td>
<td>Esse campo é obrigatório e a <a href="#6212-typeimportance-field">Seção 6.2.1.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>TypeCategory</td>
<td>6</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#6213-typecategory-field">a Seção 6.2.1.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#6214-inuse-field">a Seção 6.2.1.4</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>Campo TypeCode 6.2.1.1

O campo TypeCode descreve parcialmente o tipo específico da entrada de diretório determinada. Esse campo, além dos campos TypeImportance e TypeCategory (consulte Seção [6.2.1.2](#6212-typeimportance-field) e [Seção 6.2.1.3](#6213-typecategory-field), respectivamente) identificam exclusivamente o tipo da entrada de diretório determinada.

Todos os valores possíveis desse campo são válidos, a menos que os campos TypeImportance e TypeCategory contenham o valor 0; nesse caso, o valor 0 é inválido para esse campo.

##### <a name="6212-typeimportance-field"></a>Campo TypeImportance 6.2.1.2

O campo TypeImportance deve descrever a importância da entrada de diretório determinada.

Os valores válidos para esse campo devem ser:

- 0, o que significa que a entrada de diretório determinada é crítica (consulte a Seção [6.3.1.2.1](#63121-critical-primary-directory-entries) e a [Seção 6.4.1.2.1](#64121-critical-secondary-directory-entries) para entradas de diretórios secundários críticos e críticos, respectivamente)

- 1, o que significa que a entrada de diretório determinada é benigna (consulte a Seção [6.3.1.2.2 e](#63122-benign-primary-directory-entries) Seção [6.4.1.2.2](#64122-benign-secondary-directory-entries) para entradas de diretório secundário benigno e primário benigno, respectivamente)

##### <a name="6213-typecategory-field"></a>Campo TypeCategory 6.2.1.3

O campo TypeCategory deve descrever a categoria da entrada de diretório determinada.

Os valores válidos para esse campo devem ser:

- 0, o que significa que a entrada de diretório determinada é primária (consulte [a Seção 6.3](#63-generic-primary-directoryentry-template))

- 1, o que significa que a entrada de diretório determinada é secundária (consulte [a Seção 6.4](#64-generic-secondary-directoryentry-template))

##### <a name="6214-inuse-field"></a>6.2.1.4 Campo de inutilização

O campo InUse deve descrever se a entrada de diretório determinada está em uso ou não.

Os valores válidos para esse campo devem ser:

- 0, o que significa que a entrada de diretório determinada não está em uso; isso significa que a estrutura determinada, na verdade, é uma entrada de diretório nãoutilizada

- 1, o que significa que a entrada de diretório determinada está em uso; isso significa que a estrutura determinada é uma entrada de diretório regular

#### <a name="622-firstcluster-field"></a>6.2.2 FirstCluster Field

O campo FirstCluster deve conter o índice do primeiro cluster de uma alocação no Heap de Cluster associado à entrada de diretório determinada.

O intervalo válido de valores para esse campo deve ser:

- Exatamente 0, o que significa que não existe nenhuma alocação de cluster

- Entre 2 e ClusterCount + 1, que é o intervalo de índices de cluster válidos

Estruturas que derivam desse modelo poderão redefinir os campos FirstCluster e DataLength, se uma alocação de cluster não for compatível com a estrutura derivada.

#### <a name="623-datalength-field"></a>6.2.3 Campo DataLength

O campo DataLength descreve o tamanho, em bytes, dos dados que a alocação de cluster associada contém.

O intervalo válido de valor para este campo é:

- Pelo menos 0; se o campo FirstCluster contiver o valor 0, o único valor válido desse campo será 0

- No máximo ClusterCount \* 2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>

Estruturas que derivam desse modelo poderão redefinir os campos FirstCluster e DataLength, se uma alocação de cluster não for possível para a estrutura derivada.

### <a name="63-generic-primary-directoryentry-template"></a>6.3 Modelo de Directory Primário Genérico

A primeira entrada de diretório em um conjunto de entrada de diretório deve ser uma entrada de diretório primário. Todas as entradas de diretório subsequentes, se alguma, no conjunto de entradas de diretório deverão ser entradas de diretório secundário (consulte [a Seção 6.4](#64-generic-secondary-directoryentry-template)).

A capacidade de interpretar o modelo Directory Primário GenéricoEntrada é obrigatória.

Todas as estruturas de entrada de diretório primário derivam do modelo Directory Primário GenéricoEntrada (consulte Tabela [16](#table-16-generic-primary-directoryentry-template)), que deriva do modelo DirectoryEntry Genérico (consulte a [Seção 6.2](#62-generic-directoryentry-template)).

<div id="table-16-generic-primary-directoryentry-template" />

**Tabela 16 Modelo de Diretório Primário Genérico**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#631-entrytype-field">a Seção 6.3.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#632-secondarycount-field">e a Seção 6.3.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Esse campo é obrigatório <a href="#633-setchecksum-field">e a Seção 6.3.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Esse campo é obrigatório e <a href="#634-generalprimaryflags-field">a Seção 6.3.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>6</td>
<td>14</td>
<td>Esse campo é obrigatório e as estruturas que derivam desse modelo definem seu conteúdo.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Esse campo é obrigatório <a href="#635-firstcluster-field">e a Seção 6.3.5</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Datalength</td>
<td>24</td>
<td>8</td>
<td>Esse campo é obrigatório e <a href="#636-datalength-field">a Seção 6.3.6</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>Campo EntryType 6.3.1

O campo EntryType deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.1](#621-entrytype-field)).

##### <a name="6311-typecode-field"></a>Campo TypeCode 6.3.1.1

O campo TypeCode deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.1.1](#6211-typecode-field)).

##### <a name="6312-typeimportance-field"></a>Campo TypeImportance 6.3.1.2

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a [Seção 6.2.1.2](#6212-typeimportance-field)).

###### <a name="63121-critical-primary-directory-entries"></a>6.3.1.2.1 Entradas críticas do diretório primário

Entradas de diretório primário críticas contêm informações que são essenciais para o gerenciamento adequado de um volume exFAT. Somente o diretório raiz contém entradas críticas de diretório primário (entradas de diretório de arquivo são uma exceção, consulte [a Seção 7.4](#74-file-directory-entry)).

A definição de entradas de diretório primário críticas se correlaciona com o número de revisão exFAT principal. As implementações devem dar suporte a todas as entradas de diretório primário críticas e devem registrar apenas as estruturas de entrada de diretório primário críticas definidas por essa especificação.

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 Entradas benignas do diretório primário

Entradas de diretório primário benignas contêm informações adicionais que podem ser úteis para gerenciar um volume exFAT. Qualquer diretório pode conter entradas de diretório primário benignas.

A definição de entradas de diretório primário benigna correlaciona-se ao número de revisão exFAT secundário. O suporte para qualquer entrada de diretório primário benigno que essa especificação ou qualquer especificação subsequente definir é opcional. Uma entrada de diretório primário benigno não reconhecedo renderiza todo o conjunto de entradas de diretório como não reconheceu (além da definição dos modelos de entrada de diretório aplicáveis).

##### <a name="6313-typecategory-field"></a>Campo TypeCategory 6.3.1.3

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a [Seção 6.2.1.3](#6213-typecategory-field)).

Para esse modelo, o valor válido para esse campo deve ser 0.

##### <a name="6314-inuse-field"></a>6.3.1.4 Campo de inutilização

O campo InUse deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.1.4](#6214-inuse-field)).

#### <a name="632-secondarycount-field"></a>Campo SecondaryCount 6.3.2

O campo SecondaryCount deve descrever o número de entradas de diretório secundário que seguem imediatamente a entrada de diretório primário determinada. Essas entradas de diretório secundário, juntamente com a entrada de diretório primário determinada, compõem o conjunto de entradas de diretório.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 0, o que significa que essa entrada de diretório primário é a única entrada no conjunto de entrada de diretório

- No máximo 255, o que significa que as próximas 255 entradas de diretório e essa entrada de diretório primário compõem o conjunto de entrada de diretório

Estruturas de entrada de diretório primário críticas que derivam desse modelo podem redefinir os campos SecondaryCount e SetChecksum.

#### <a name="633-setchecksum-field"></a>6.3.3 Campo SetChecksum

O campo SetChecksum deve conter a verificação de todas as entradas de diretório no conjunto de entrada de diretório determinado. No entanto, a verificação exclui esse campo (consulte [a Figura 2](#figure-2-entrysetchecksum-computation)). As implementações deverão verificar se o conteúdo desse campo é válido antes de usar qualquer outra entrada de diretório no conjunto de entrada de diretório determinado.

Estruturas de entrada de diretório primário críticas que derivam desse modelo podem redefinir os campos SecondaryCount e SetChecksum.

<div id="figure-2-entrysetchecksum-computation" />

**Figura 2 EntrySetChecksum Computation**

```C
UInt16 EntrySetChecksum
(
    UCHAR * Entries,       // points to an in-memory copy of the directory entry set
    UCHAR   SecondaryCount
)
{
    UInt16 NumberOfBytes = ((UInt16)SecondaryCount + 1) * 32;
    UInt16 Checksum = 0;
    UInt16 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 2) || (Index == 3))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x8000 : 0) + (Checksum>>1) +  (UInt16)Entries[Index];
    }
    return Checksum;
}
```

#### <a name="634-generalprimaryflags-field"></a>6.3.4 Campo GeneralPrimaryFlags

O campo GeneralPrimaryFlags contém sinalizadores (consulte [Tabela 17](#table-17-generic-generalprimaryflags-field-structure)).

Estruturas de entrada de diretório primário críticas que derivam desse modelo podem redefinir esse campo.

<div id="table-17-generic-generalprimaryflags-field-structure" />

**Estrutura de campo GeneralPrimaryFlags genérica da Tabela 17**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#6341-allocationpossible-field">a Seção 6.3.4.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#6342-nofatchain-field">a Seção 6.3.4.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>14</td>
<td>Esse campo é obrigatório e as estruturas que derivam desse modelo podem definir esse campo.</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>6.3.4.1 Campo AllocationPossible

O campo AllocationPossible deve descrever se uma alocação no Heap de Cluster é possível ou não para a entrada de diretório determinada.

Os valores válidos para esse campo devem ser:

- 0, o que significa que uma alocação associada de clusters não é possível e os campos FirstCluster e DataLength são realmente indefinido (estruturas que derivam desse modelo podem redefinir esses campos)

- 1, o que significa que uma alocação associada de clusters é possível e os campos FirstCluster e DataLength são definidos

##### <a name="6342-nofatchain-field"></a>Campo NoFatChain 6.3.4.2

O campo NoFatChain deve indicar se o FAT ativo descreve ou não a cadeia de cluster da alocação determinada.

Os valores válidos para esse campo devem ser:

- 0, o que significa que as entradas FAT correspondentes para a cadeia de clusters da alocação são válidas e as implementações deverão interpretá-las; se o campo AllocationPossible contiver o valor 0 ou se o campo AllocationPossible contiver o valor 1 e o campo FirstCluster contiver o valor 0, o único valor válido desse campo será 0

- 1, o que significa que a alocação associada é uma série contígua de clusters; as entradas FAT correspondentes para os clusters são inválidas e as implementações não devem interpretá-las; as implementações podem usar a equação a seguir para calcular o tamanho da alocação associada: DataLength / (2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>) arredondado para cima até o inteiro mais próximo

Se as estruturas de entrada de diretório primário críticas que derivam desse modelo redefinirem o campo GeneralPrimaryFlags, as entradas FAT correspondentes para a cadeia de cluster de qualquer alocação associada serão válidas.

#### <a name="635-firstcluster-field"></a>6.3.5 Campo FirstCluster

O campo FirstCluster deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.2](#622-firstcluster-field)).

Se o bit NoFatChain for 1, FirstCluster deverá apontar para um cluster válido no heap de cluster.

Estruturas de entrada de diretório primário críticas que derivam desse modelo podem redefinir os campos FirstCluster e DataLength. Outras estruturas que derivam desse modelo poderão redefinir os campos FirstCluster e DataLength somente se o campo AllocationPossible contiver o valor 0.

#### <a name="636-datalength-field"></a>6.3.6 Campo DataLength

O campo DataLength deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.3](#623-datalength-field)).

Se o bit NoFatChain for 1, DataLength não deverá ser zero. Se o campo FirstCluster for zero, DataLength também deverá ser zero.

Estruturas de entrada de diretório primário críticas que derivam desse modelo podem redefinir os campos FirstCluster e DataLength. Outras estruturas que derivam desse modelo poderão redefinir os campos FirstCluster e DataLength somente se o campo AllocationPossible contiver o valor 0.

### <a name="64-generic-secondary-directoryentry-template"></a>6.4 Modelo directory secundário genérico

A finalidade central das entradas de diretório secundário é fornecer informações adicionais sobre um conjunto de entradas de diretório. A capacidade de interpretar o modelo Directory Secundário GenéricoEntrada é obrigatória.

A definição de entradas de diretório secundário críticas e benignas correlaciona-se ao número de revisão exFAT secundário. O suporte para qualquer entrada de diretório secundário crítico ou benigno que essa especificação ou especificações subsequentes definirem é opcional.

Todas as estruturas de entrada de diretório secundário derivam do modelo DirectoryEntry Secundário Genérico (consulte Tabela [18](#table-18-generic-secondary-directoryentry-template)), que deriva do modelo DirectoryEntry Genérico (consulte a [Seção 6.2](#62-generic-directoryentry-template)).

<div id="table-18-generic-secondary-directoryentry-template" />

**Tabela 18 Modelo directory secundário genérico**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e a <a href="#641-entrytype-field">Seção 6.4.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#642-generalsecondaryflags-field">a Seção 6.4.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>18</td>
<td>Esse campo é obrigatório e as estruturas que derivam desse modelo definem seu conteúdo.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#643-firstcluster-field">a Seção 6.4.3</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Datalength</td>
<td>24</td>
<td>8</td>
<td>Esse campo é obrigatório e <a href="#644-datalength-field">a Seção 6.4.4</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>Campo EntryType 6.4.1

O campo EntryType deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.1](#621-entrytype-field))

##### <a name="6411-typecode-field"></a>Campo TypeCode 6.4.1.1

O campo TypeCode deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.1.1](#6211-typecode-field)).

##### <a name="6412-typeimportance-field"></a>Campo TypeImportance 6.4.1.2

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a [Seção 6.2.1.2](#6212-typeimportance-field)).

###### <a name="64121-critical-secondary-directory-entries"></a>6.4.1.2.1 Entradas críticas do diretório secundário

Entradas críticas de diretório secundário contêm informações que são críticas para o gerenciamento adequado de seu conjunto de entrada de diretório que o contém.
Embora o suporte para qualquer entrada de diretório secundário crítico específica seja opcional, uma entrada de diretório crítico não marcada renderiza todo o conjunto de entradas de diretório como não reconheceu (além da definição dos modelos de entrada de diretório aplicáveis).

No entanto, se um conjunto de entradas de diretório contiver pelo menos uma entrada de diretório secundário crítica que uma implementação não reconheça, a implementação deverá, no máximo, interpretar os modelos das entradas de diretório no conjunto de entradas de diretório e não os dados que qualquer alocação associada a qualquer entrada de diretório no conjunto de entradas de diretório contiver (entradas de diretório de arquivo são uma exceção, consulte a Seção [7.4](#74-file-directory-entry)).

###### <a name="64122-benign-secondary-directory-entries"></a>6.4.1.2.2 Entradas benignas do diretório secundário

Entradas de diretório secundário benignas contêm informações adicionais que podem ser úteis para gerenciar seu conjunto de entrada de diretório que o contém. O suporte para qualquer entrada de diretório secundário benigno específica é opcional.
Entradas de diretório secundário benignas não reconhecedas não renderiza todo o conjunto de entrada de diretório como não marcado.

As implementações podem ignorar qualquer entrada secundária benigna que ela não reconheça.

##### <a name="6413-typecategory-field"></a>Campo TypeCategory 6.4.1.3

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a [Seção 6.2.1.3](#6213-typecategory-field)).

Para esse modelo, o valor válido para esse campo é 1.

##### <a name="6414-inuse-field"></a>6.4.1.4 Campo de inutilização

O campo InUse deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.1.4](#6214-inuse-field)).

#### <a name="642-generalsecondaryflags-field"></a>6.4.2 Campo GeneralSecondaryFlags

O campo GeneralSecondaryFlags contém sinalizadores (consulte [Tabela 19](#table-19-generic-generalsecondaryflags-field-structure)).

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**Estrutura de campo GeneralSecondaryFlags genérica da Tabela 19**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#6421-allocationpossible-field">e a Seção 6.4.2.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#6422-nofatchain-field">e a Seção 6.4.2.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>6</td>
<td>Esse campo é obrigatório e as estruturas que derivam desse modelo podem definir esse campo.</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>6.4.2.1 Campo AllocationPossible

O campo AllocationPossible deve ter a mesma definição que o mesmo campo nomeado no modelo DirectoryEntry Primário Genérico (consulte a [Seção 6.3.4.1](#6341-allocationpossible-field)).

##### <a name="6422-nofatchain-field"></a>Campo NoFatChain 6.4.2.2

O campo NoFatChain deve ter a mesma definição que o campo de mesmo nome no modelo DirectoryEntry Primário Genérico (consulte a [Seção 6.3.4.2](#6342-nofatchain-field)).

#### <a name="643-firstcluster-field"></a>6.4.3 Campo FirstCluster

O campo FirstCluster deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.2](#622-firstcluster-field)).

Se o bit NoFatChain for 1, FirstCluster deverá apontar para um cluster válido no heap de cluster.

#### <a name="644-datalength-field"></a>6.4.4 Campo DataLength

O campo DataLength deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte [a Seção 6.2.3](#623-datalength-field)).

Se o bit NoFatChain for 1, DataLength não deverá ser zero. Se o campo FirstCluster for zero, DataLength também deverá ser zero.

## <a name="7-directory-entry-definitions"></a>7 Definições de entrada de diretório

A revisão 1.00 do sistema de arquivos exFAT define as seguintes entradas de diretório:

- Primário crítico

  - Bitmap de alocação ([Seção 7.1](#71-allocation-bitmap-directory-entry))

  - Tabela de caso up-case ([Seção 7.2](#72-up-case-table-directory-entry))

  - Rótulo do volume ([Seção 7.3](#73-volume-label-directory-entry))

  - Arquivo ([Seção 7.4](#74-file-directory-entry))

- Primário benigno

  - GUID do volume ([Seção 7.5](#75-volume-guid-directory-entry))

  - Preenchimento de TexFAT ([Seção 7.10](#710-texfat-padding-directory-entry))

<!-- -->

- Secundário crítico

  - Extensão de fluxo ([Seção 7.6](#76-stream-extension-directory-entry))

  - Nome do arquivo ([Seção 7.7](#77-file-name-directory-entry))

- Secundário benigno

  - Extensão de fornecedor ([Seção 7.8](#78-vendor-extension-directory-entry))

  - Alocação de fornecedor ([Seção 7.9](#79-vendor-allocation-directory-entry))

### <a name="71-allocation-bitmap-directory-entry"></a>7.1 Entrada de diretório bitmap de alocação

No sistema de arquivos exFAT, uma FAT não descreve o estado de alocação de clusters; em vez disso, um Bitmap de Alocação faz. Bitmaps de alocação existem no Heap de Cluster (consulte a Seção [7.1.5](#715-allocation-bitmap)) e têm entradas de diretório primário críticas correspondentes no diretório raiz (consulte [a Tabela 20](#table-20-allocation-bitmap-directoryentry-structure)).

O campo NumberOfFats determina o número de entradas de diretório bitmap de alocação válidas no diretório raiz. Se o campo NumberOfFats contiver o valor 1, o único número válido de entradas de diretório bitmap de alocação será 1. Além disso, a única entrada de diretório bitmap de alocação só será válida se descrever o Bitmap de Primeira Alocação (consulte a [Seção 7.1.2.1](#7121-bitmapidentifier-field)). Se o campo NumberOfFats contiver o valor 2, o único número válido de entradas de diretório de Bitmap de Alocação será 2.
Além disso, as duas entradas de diretório bitmap de alocação só serão válidas se uma descrever o Bitmap de Primeira Alocação e a outra descrever o Segundo Bitmap de Alocação.

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**Tabela 20 Alocação Diretório bitmap Estrutura de entrada**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#711-entrytype-field">a Seção 7.1.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>BitmapFlags</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#712-bitmapflags-field">a Seção 7.1.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>2</td>
<td>18</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#713-firstcluster-field">a Seção 7.1.3</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Datalength</td>
<td>24</td>
<td>8</td>
<td>Esse campo é obrigatório e <a href="#714-datalength-field">a Seção 7.1.4</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>Campo EntryType 7.1.1

O campo EntryType deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Primário Genérico (consulte [a Seção 6.3.1](#631-entrytype-field)).

##### <a name="7111-typecode-field"></a>Campo TypeCode 7.1.1.1

O campo TypeCode deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.1.1](#6311-typecode-field)).

Para uma entrada de diretório bitmap de alocação, o valor válido para esse campo é 1.

##### <a name="7112-typeimportance-field"></a>Campo TypeImportance 7.1.1.2

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.1.2](#6312-typeimportance-field)).

Para uma entrada de diretório bitmap de alocação, o valor válido para esse campo é 0.

##### <a name="7113-typecategory-field"></a>Campo TypeCategory 7.1.1.3

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.1.3](#6313-typecategory-field)).

##### <a name="7114-inuse-field"></a>7.1.1.4 Campo de inutilização

O campo InUse deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a [Seção 6.3.1.4](#6314-inuse-field)).

#### <a name="712-bitmapflags-field"></a>7.1.2 Campo BitmapFlags

O campo BitmapFlags contém sinalizadores (consulte [Tabela 21](#table-21-bitmapflags-field-structure)).

<div id="table-21-bitmapflags-field-structure" />

**Estrutura do campo BitmapFlags da Tabela 21**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapIdentifier</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#7121-bitmapidentifier-field">a Seção 7.1.2.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>1</td>
<td>7</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>7.1.2.1 Campo BitmapIdentifier

O campo BitmapIdentifier deve indicar qual Bitmap de Alocação a entrada de diretório determinada descreve. As implementações devem usar o Bitmap de Primeira Alocação em conjunto com a Primeira FAT e devem usar o Segundo Bitmap de Alocação em conjunto com o segundo FAT. O campo ActiveFat descreve qual FAT e Bitmap de Alocação estão ativos.

Os valores válidos para esse campo devem ser:

- 0, o que significa que a entrada de diretório determinada descreve o bitmap de primeira alocação

- 1, o que significa que a entrada de diretório determinada descreve o Segundo Bitmap de Alocação e só é possível quando NumberOfFats contém o valor 2

#### <a name="713-firstcluster-field"></a>7.1.3 Campo FirstCluster

O campo FirstCluster deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.5](#635-firstcluster-field)).

Esse campo contém o índice do primeiro cluster da cadeia de clusters, como descreve o FAT, que hospeda o Bitmap de Alocação.

#### <a name="714-datalength-field"></a>7.1.4 Campo DataLength

O campo DataCluster deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.6](#636-datalength-field)).

#### <a name="715-allocation-bitmap"></a>7.1.5 Bitmap de alocação

Um Bitmap de Alocação registra o estado de alocação dos clusters no Heap de Cluster. Cada bit em um Bitmap de Alocação indica se seu cluster correspondente está disponível para alocação ou não.

Um Bitmap de Alocação representa clusters do índice mais baixo para o mais alto (consulte [a Tabela 22](#table-22-allocation-bitmap-structure)). Por motivos históricos, o primeiro cluster tem o índice 2.
Observação: o primeiro bit no bitmap é o bit de ordem mais baixa do primeiro byte.

<div id="table-22-allocation-bitmap-structure" />

**Estrutura de bitmap de alocação da Tabela 22**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapEntry[2]</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e a <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">Seção 7.1.5.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>BitmapEntry[ClusterCount+1]</td>
<td>ClusterCount – 1</td>
<td>1</td>
<td><p>Esse campo é obrigatório e <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">a Seção 7.1.5.1</a> define seu conteúdo.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm o campo ClusterCount.</p></td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>ClusterCount</td>
<td>(DataLength * 8) – ClusterCount</td>
<td><p>Esse campo é obrigatório e seu conteúdo, se algum, é reservado.</p>
<p>Observação: os Setores de Inicialização principal e de backup contêm o campo ClusterCount.</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 BitmapEntry \[ \] 2... Campos BitmapEntry \[ ClusterCount+1 \]

Cada campo BitmapEntry nessa matriz representa um cluster no Heap de Cluster. O BitmapEntry 2 representa o primeiro cluster no Heap de Cluster e \[ \] o Cluster BitmapEntryCount+1 representa o último \[ cluster no Heap de \] Cluster.

Os valores válidos para esses campos devem ser:

- 0, que descreve o cluster correspondente como disponível para alocação

- 1, que descreve o cluster correspondente como não disponível para alocação (uma alocação de cluster já pode consumir o cluster correspondente ou o FAT ativo pode descrever o cluster correspondente como ruim)

### <a name="72-up-case-table-directory-entry"></a>7.2 Entrada de diretório de tabela de caso up-case

A Tabela de Maiúsculas e Maiúsculas define a conversão de caracteres de letras maiúsculas em letras maiúsculas. Isso é importante devido à entrada do diretório Nome do Arquivo (consulte a Seção 7.7) usando caracteres Unicode e o sistema de arquivos exFAT não importando maiúsculas de minúsculas e preservando maiúsculas de minúsculas. A Tabela de Caso Up existe no Heap de Cluster (consulte a Seção [7.2.5](#725-up-case-table)) e tem uma entrada de diretório primário crítica correspondente no diretório raiz (consulte Tabela [23](#table-23-up-case-table-directoryentry-structure)). O número válido de entradas de diretório tabela de caso up-case é 1.

Devido à relação entre os nomes de tabela de caso up-case e de arquivo, as implementações não devem modificar a Tabela de Caso Up, exceto como resultado de operações de formato.

<div id="table-23-up-case-table-directoryentry-structure" />

**Tabela 23 Diretório de tabela de caso up-case Estrutura de entrada**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#721-entrytype-field">a Seção 7.2.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>1</td>
<td>3</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="odd">
<td>TableChecksum</td>
<td>4</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#722-tablechecksum-field">a Seção 7.2.2</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>8</td>
<td>12</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#723-firstcluster-field">a Seção 7.2.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Datalength</td>
<td>24</td>
<td>8</td>
<td>Esse campo é obrigatório e <a href="#724-datalength-field">a Seção 7.2.4</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>Campo EntryType 7.2.1

O campo EntryType deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Primário Genérico (consulte [a Seção 6.3.1](#631-entrytype-field)).

##### <a name="7211-typecode-field"></a>Campo TypeCode 7.2.1.1

O campo TypeCode deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.1.1](#6311-typecode-field)).

Para a entrada do diretório Up-case Table, o valor válido para esse campo é
2.

##### <a name="7212-typeimportance-field"></a>Campo TypeImportance 7.2.1.2

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.1.2](#6312-typeimportance-field)).

Para a entrada do diretório Up-case Table, o valor válido para esse campo é
0.

##### <a name="7213-typecategory-field"></a>Campo TypeCategory 7.2.1.3

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.1.3](#6313-typecategory-field)).

##### <a name="7214-inuse-field"></a>7.2.1.4 Campo de inutilização

O campo InUse deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a [Seção 6.3.1.4](#6314-inuse-field)).

#### <a name="722-tablechecksum-field"></a>7.2.2 Campo TableChecksum

O campo TableChecksum contém a verificação da Tabela de Caso Up (que os campos FirstCluster e DataLength descrevem). As implementações deverão verificar se o conteúdo desse campo é válido antes de usar a Tabela de Caso Up.

<div id="figure-3-tablechecksum-computation" />

**Figura 3 TableChecksum Computation**

```C
UInt32 TableChecksum
(
    UCHAR  * Table,    // points to an in-memory copy of the up-case table
    UInt64   DataLength
)
{
    UInt32 Checksum = 0;
    UInt64 Index;

    for (Index = 0; Index < DataLength; Index++)
    {
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Table[Index];
    }

    return Checksum;
}
```

#### <a name="723-firstcluster-field"></a>7.2.3 Campo FirstCluster

O campo FirstCluster deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.5](#635-firstcluster-field)).

Esse campo contém o índice do primeiro cluster da cadeia de clusters, como descreve o FAT, que hospeda a Tabela de Caso Up.

#### <a name="724-datalength-field"></a>7.2.4 Campo DataLength

O campo DataCluster deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.6](#636-datalength-field)).

#### <a name="725-up-case-table"></a>7.2.5 Tabela de caso up-case

Uma tabela de caso up é uma série de mapeamentos de caracteres Unicode. Um mapeamento de caracteres consiste em um campo de 2 byte, com o índice do campo na tabela de caso para cima que representa o caractere Unicode a ser em caso up-case e o campo de 2 byte que representa o caractere Unicode em caso acima.

Os primeiros 128 caracteres Unicode têm mapeamentos obrigatórios (consulte [Tabela 24](#table-24-mandatory-first-128-up-case-table-entries)).
Uma tabela de caso up que tem qualquer outro mapeamento de caracteres para qualquer um dos primeiros 128 caracteres Unicode é inválida.

Implementações que só suportam caracteres do intervalo de mapeamento obrigatório podem ignorar os mapeamentos do restante da tabela de caso acima. Essas implementações só devem usar caracteres do intervalo de mapeamento obrigatório ao criar ou renomear arquivos (por meio da entrada do diretório Nome do Arquivo, consulte [a Seção 7.7](#77-file-name-directory-entry)). Quando há nomes de arquivo existentes com uso de caixa de dados, essas implementações não devem ter caracteres de caso up-case do intervalo de mapeamento não obrigatório, mas devem deixá-los intactos no nome de arquivo com caso acima resultante (esse é um uso parcial de caixa de caracteres). Ao comparar nomes de arquivo, essas implementações devem tratar nomes de arquivo que diferem do nome em comparação apenas por caracteres Unicode do intervalo de mapeamento não obrigatório como equivalente. Embora esses nomes de arquivo sejam potencialmente equivalentes, essas implementações não podem garantir que o nome de arquivo totalmente em caso de caso não colida com o nome em comparação.

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Tabela 24 As primeiras 128 entradas da tabela de caso up-case obrigatórias**

| Índice de tabela | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| **0000h**       | 0000h             | 0001h     | 0002h     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000Ah     | 000Bh     | 000Ch     | 000Dh     | 000Eh     | 000Fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001Ah     | 001Bh     | 001Ch     | 001Dh     | 001Eh     | 001Fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002Ah     | 002Bh     | 002Ch     | 002Dh     | 002Eh     | 002Fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003Ah     | 003Bh     | 003Ch     | 003Dh     | 003Eh     | 003Fh     |
| **0040h**       | 0040h             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004Ah     | 004Bh     | 004Ch     | 004Dh     | 004Eh     | 004Fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005Ah     | 005Bh     | 005Ch     | 005Dh     | 005Eh     | 005Fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004Ah** | **004Bh** | **004Ch** | **004Dh** | **004Eh** | **004Fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005Ah** | 007Bh     | 007Ch     | 007Dh     | 007Eh     | 007Fh     |

**(Observação: as entradas com mapeamentos de caso up-case que não são de identidade estão em negrito)**

Após a formatação de um volume, as implementações podem gerar uma tabela em maiúsculas em um formato compactado usando a compactação de mapeamento de identidade, já que uma grande parte do espaço de caracteres Unicode não tem nenhum conceito de maiúsculas e vírgulas (o que significa que os caracteres "letras maiúsculas" e "letras maiúsculas" são equivalentes).
As implementações compactam uma tabela em caso up representando uma série de mapeamentos de identidade com o valor FFFFh seguido pelo número de mapeamentos de identidade.

Por exemplo, uma implementação pode representar os primeiros mapeamentos de 100 (64h) de caracteres com as oito entradas a seguir de uma tabela compactada de caso:

> FFFFh, 0061h, 0041h, 0042h, 0043h

As duas primeiras entradas indicam que os primeiros 97 (61h) caracteres (de 0000h a 0060h) têm mapeamentos de identidade. Os caracteres subsequentes, 0061h a 0063h, mapeiam para os caracteres 0041h a 0043h, respectivamente.

A capacidade de fornecer uma tabela compactada em caso de ocorrência ao formatar um volume é opcional. No entanto, a capacidade de interpretar uma tabela de caso compactada e compactada é obrigatória. O valor do campo TableChecksum sempre está em conformidade com a forma como a tabela de maiúsculas e minúsculas existe no volume, que pode estar no formato compactado ou descompactado.

##### <a name="7251-recommended-up-case-table"></a>Tabela de casos de 7.2.5.1 recomendado

Ao Formatar um volume, as implementações devem registrar a tabela recomendada de caso ativo no formato compactado (consulte a [tabela 25](#table-25-recommended-up-case-table-in-compressed-format)), para a qual o valor do campo TableChecksum é E619D30Dh.

Se uma implementação definir sua própria tabela de casos ativos, compactada ou descompactada, essa tabela deverá cobrir o intervalo de caracteres Unicode completo (de códigos de caracteres 0000h para FFFFh inclusivo).

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**Tabela 25 tabela de maiúsculas e minúsculas recomendada no formato compactado**

| Deslocamento bruto | + 0 |  + 1       |  + 2       |  + 3       |  + 4       | + 5        |  + 6       | + 7        |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
| **0000h**      | 0000h                        | 0001h   | 0002h   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000Ah   | 000Bh   | 000Ch   | 000Dh   | 000Eh   | 000Fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001Ah   | 001Bh   | 001Ch   | 001Dh   | 001Eh   | 001Fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002Ah   | 002Bh   | 002Ch   | 002Dh   | 002Eh   | 002Fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003Ah   | 003Bh   | 003Ch   | 003Dh   | 003Eh   | 003Fh   |
| **0040h**      | 0040h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0048h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0050h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0058h**      | 0058h                        | 0059h   | 005Ah   | 005Bh   | 005Ch   | 005Dh   | 005Eh   | 005Fh   |
| **0060h**      | 0060h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0068h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0070h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0078h**      | 0058h                        | 0059h   | 005Ah   | 007Bh   | 007Ch   | 007Dh   | 007Eh   | 007Fh   |
| **0080h**      | 0080h                        | 0081h   | 0082h   | 0083h   | 0084h   | 0085h   | 0086h   | 0087h   |
| **0088h**      | 0088h                        | 0089h   | 008Ah   | 008Bh   | 008Ch   | 008Dh   | 008Eh   | 008Fh   |
| **0090h**      | 0090h                        | 0091h   | 0092h   | 0093h   | 0094h   | 0095h   | 0096h   | 0097h   |
| **0098h**      | 0098h                        | 0099h   | 009Ah   | 009Bh   | 009Ch   | 009Dh   | 009Eh   | 009Fh   |
| **00A0h**      | 00A0h                        | 00A1h   | 00A2h   | 00A3h   | 00A4h   | 00A5h   | 00A6h   | 00A7h   |
| **00A8h**      | 00A8h                        | 00A9h   | 00AAh   | 00ABh   | 00ACh   | 00ADh   | 00AEh   | 00AFh   |
| **00B0h**      | 00B0h                        | 00B1h   | 00B2h   | 00B3h   | 00B4h   | 00B5h   | 00B6h   | 00B7h   |
| **00B8h**      | 00B8h                        | 00B9h   | 00BAh   | 00BBh   | 00BCh   | 00BDh   | 00BEh   | 00BFh   |
| **00C0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00C8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00D0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00D7h   |
| **00D8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 00DFh   |
| **00E0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00E8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00F0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00F7h   |
| **00F8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 0178h   |
| **0100h**      | 0100h                        | 0100h   | 0102h   | 0102h   | 0104h   | 0104h   | 0106h   | 0106h   |
| **0108h**      | 0108h                        | 0108h   | 010Ah   | 010Ah   | 010Ch   | 010Ch   | 010Eh   | 010Eh   |
| **0110h**      | 0110h                        | 0110h   | 0112h   | 0112h   | 0114h   | 0114h   | 0116h   | 0116h   |
| **0118h**      | 0118h                        | 0118h   | 011Ah   | 011Ah   | 011Ch   | 011Ch   | 011Eh   | 011Eh   |
| **0120h**      | 0120h                        | 0120h   | 0122h   | 0122h   | 0124h   | 0124h   | 0126h   | 0126h   |
| **0128h**      | 0128h                        | 0128h   | 012Ah   | 012Ah   | 012Ch   | 012Ch   | 012Eh   | 012Eh   |
| **0130h**      | 0130h                        | 0131h   | 0132h   | 0132h   | 0134h   | 0134h   | 0136h   | 0136h   |
| **0138h**      | 0138h                        | 0139h   | 0139h   | 013Bh   | 013Bh   | 013Dh   | 013Dh   | 013Fh   |
| **0140h**      | 013Fh                        | 0141h   | 0141h   | 0143h   | 0143h   | 0145h   | 0145h   | 0147h   |
| **0148h**      | 0147h                        | 0149h   | 014Ah   | 014Ah   | 014Ch   | 014Ch   | 014Eh   | 014Eh   |
| **0150h**      | 0150h                        | 0150h   | 0152h   | 0152h   | 0154h   | 0154h   | 0156h   | 0156h   |
| **0158h**      | 0158h                        | 0158h   | 015Ah   | 015Ah   | 015Ch   | 015Ch   | 015Eh   | 015Eh   |
| **0160h**      | 0160h                        | 0160h   | 0162h   | 0162h   | 0164h   | 0164h   | 0166h   | 0166h   |
| **0168h**      | 0168h                        | 0168h   | 016Ah   | 016Ah   | 016Ch   | 016Ch   | 016Eh   | 016Eh   |
| **0170h**      | 0170h                        | 0170h   | 0172h   | 0172h   | 0174h   | 0174h   | 0176h   | 0176h   |
| **0178h**      | 0178h                        | 0179h   | 0179h   | 017Bh   | 017Bh   | 017Dh   | 017Dh   | 017Fh   |
| **0180h**      | 0243h                        | 0181h   | 0182h   | 0182h   | 0184h   | 0184h   | 0186h   | 0187h   |
| **0188h**      | 0187h                        | 0189h   | 018Ah   | 018Bh   | 018Bh   | 018Dh   | 018Eh   | 018Fh   |
| **0190h**      | 0190h                        | 0191h   | 0191h   | 0193h   | 0194h   | 01F6h   | 0196h   | 0197h   |
| **0198h**      | 0198h                        | 0198h   | 023Dh   | 019Bh   | 019Ch   | 019Dh   | 0220h   | 019Fh   |
| **01A0h**      | 01A0h                        | 01A0h   | 01A2h   | 01A2h   | 01A4h   | 01A4h   | 01A6h   | 01A7h   |
| **01A8h**      | 01A7h                        | 01A9h   | 01AAh   | 01ABh   | 01ACh   | 01ACh   | 01AEh   | 01AFh   |
| **01B0h**      | 01AFh                        | 01B1h   | 01B2h   | 01B3h   | 01B3h   | 01B5h   | 01B5h   | 01B7h   |
| **01B8h**      | 01B8h                        | 01B8h   | 01BAh   | 01BBh   | 01BCh   | 01BCh   | 01BEh   | 01F7h   |
| **01C0h**      | 01C0h                        | 01C1h   | 01C2h   | 01C3h   | 01C4h   | 01C5h   | 01C4h   | 01C7h   |
| **01C8h**      | 01C8h                        | 01C7h   | 01CAh   | 01CBh   | 01CAh   | 01CDh   | 01CDh   | 01CFh   |
| **01D0h**      | 01CFh                        | 01D1h   | 01D1h   | 01D3h   | 01D3h   | 01D5h   | 01D5h   | 01D7h   |
| **01D8h**      | 01D7h                        | 01D9h   | 01D9h   | 01DBh   | 01DBh   | 018Eh   | 01DEh   | 01DEh   |
| **01E0h**      | 01E0h                        | 01E0h   | 01E2h   | 01E2h   | 01E4h   | 01E4h   | 01E6h   | 01E6h   |
| **01E8h**      | 01E8h                        | 01E8h   | 01EAh   | 01EAh   | 01ECh   | 01ECh   | 01EEh   | 01EEh   |
| **01F0h**      | 01F0h                        | 01F1h   | 01F2h   | 01F1h   | 01F4h   | 01F4h   | 01F6h   | 01F7h   |
| **01F8h**      | 01F8h                        | 01F8h   | 01FAh   | 01FAh   | 01FCh   | 01FCh   | 01FEh   | 01FEh   |
| **0200h**      | 0200h                        | 0200h   | 0202h   | 0202h   | 0204h   | 0204h   | 0206h   | 0206h   |
| **0208h**      | 0208h                        | 0208h   | 020Ah   | 020Ah   | 020Ch   | 020Ch   | 020Eh   | 020Eh   |
| **0210h**      | 0210h                        | 0210h   | 0212h   | 0212h   | 0214h   | 0214h   | 0216h   | 0216h   |
| **0218h**      | 0218h                        | 0218h   | 021Ah   | 021Ah   | 021Ch   | 021Ch   | 021Eh   | 021Eh   |
| **0220h**      | 0220h                        | 0221h   | 0222h   | 0222h   | 0224h   | 0224h   | 0226h   | 0226h   |
| **0228h**      | 0228h                        | 0228h   | 022Ah   | 022Ah   | 022Ch   | 022Ch   | 022Eh   | 022Eh   |
| **0230h**      | 0230h                        | 0230h   | 0232h   | 0232h   | 0234h   | 0235h   | 0236h   | 0237h   |
| **0238h**      | 0238h                        | 0239h   | 2C65h   | 023Bh   | 023Bh   | 023Dh   | 2C66h   | 023Fh   |
| **0240h**      | 0240h                        | 0241h   | 0241h   | 0243h   | 0244h   | 0245h   | 0246h   | 0246h   |
| **0248h**      | 0248h                        | 0248h   | 024Ah   | 024Ah   | 024Ch   | 024Ch   | 024Eh   | 024Eh   |
| **0250h**      | 0250h                        | 0251h   | 0252h   | 0181h   | 0186h   | 0255h   | 0189h   | 018Ah   |
| **0258h**      | 0258h                        | 018Fh   | 025Ah   | 0190h   | 025Ch   | 025Dh   | 025Eh   | 025Fh   |
| **0260h**      | 0193h                        | 0261h   | 0262h   | 0194h   | 0264h   | 0265h   | 0266h   | 0267h   |
| **0268h**      | 0197h                        | 0196h   | 026Ah   | 2C62h   | 026Ch   | 026Dh   | 026Eh   | 019Ch   |
| **0270h**      | 0270h                        | 0271h   | 019Dh   | 0273h   | 0274h   | 019Fh   | 0276h   | 0277h   |
| **0278h**      | 0278h                        | 0279h   | 027Ah   | 027Bh   | 027Ch   | 2C64h   | 027Eh   | 027Fh   |
| **0280h**      | 01A6h                        | 0281h   | 0282h   | 01A9h   | 0284h   | 0285h   | 0286h   | 0287h   |
| **0288h**      | 01AEh                        | 0244h   | 01B1h   | 01B2h   | 0245h   | 028Dh   | 028Eh   | 028Fh   |
| **0290h**      | 0290h                        | 0291h   | 01B7h   | 0293h   | 0294h   | 0295h   | 0296h   | 0297h   |
| **0298h**      | 0298h                        | 0299h   | 029Ah   | 029Bh   | 029Ch   | 029Dh   | 029Eh   | 029Fh   |
| **02A0h**      | 02A0h                        | 02A1h   | 02A2h   | 02A3h   | 02A4h   | 02A5h   | 02A6h   | 02A7h   |
| **02A8h**      | 02A8h                        | 02A9h   | 02AAh   | 02ABh   | 02ACh   | 02ADh   | 02AEh   | 02AFh   |
| **02B0h**      | 02B0h                        | 02B1h   | 02B2h   | 02B3h   | 02B4h   | 02B5h   | 02B6h   | 02B7h   |
| **02B8h**      | 02B8h                        | 02B9h   | 02BAh   | 02Bh   | 02BCh   | 02BDh   | 02BEh   | 02BFh   |
| **02C0h**      | 02C0h                        | 02C1h   | 02C2h   | 02C3h   | 02C4h   | 02C5h   | 02C6h   | 02C7h   |
| **02C8h**      | 02C8h                        | 02C9h   | 02CAh   | 02CBh   | 02CCh   | 02CDh   | 02CEh   | 02CFh   |
| **02D0h**      | 02D0h                        | 02D1h   | 02D2h   | 02D3h   | 02D4h   | 02D5h   | 02D6h   | 02D7h   |
| **02D8h**      | 02D8h                        | 02D9h   | 02DAh   | 02DBh   | 02DCh   | 02DDh   | 02DEh   | 02DFh   |
| **02E0h**      | 02E0h                        | 02E1h   | 02E2h   | 02E3h   | 02E4h   | 02E5h   | 02E6h   | 02E7h   |
| **02E8h**      | 02E8h                        | 02E9h   | 02EAh   | 02EBh   | 02ECh   | 02EDh   | 02EEh   | 02EFh   |
| **02F0h**      | 02F0h                        | 02F1h   | 02F2h   | 02F3h   | 02F4h   | 02F5h   | 02F6h   | 02F7h   |
| **02F8h**      | 02F8h                        | 02F9h   | 02FAh   | 02FBh   | 02FCh   | 02FDh   | 02FEh   | 02FFh   |
| **0300h**      | 0300h                        | 0301h   | 0302h   | 0303h   | 0304h   | 0305h   | 0306h   | 0307h   |
| **0308h**      | 0308h                        | 0309h   | 030Ah   | 030Bh   | 030Ch   | 030Dh   | 030Eh   | 030Fh   |
| **0310h**      | 0310h                        | 0311h   | 0312h   | 0313h   | 0314h   | 0315h   | 0316h   | 0317h   |
| **0318h**      | 0318h                        | 0319h   | 031Ah   | 031Bh   | 031Ch   | 031Dh   | 031Eh   | 031Fh   |
| **0320h**      | 0320h                        | 0321h   | 0322h   | 0323h   | 0324h   | 0325h   | 0326h   | 0327h   |
| **0328h**      | 0328h                        | 0329h   | 032Ah   | 032Bh   | 032Ch   | 032Dh   | 032Eh   | 032Fh   |
| **0330h**      | 0330h                        | 0331h   | 0332h   | 0333h   | 0334h   | 0335h   | 0336h   | 0337h   |
| **0338h**      | 0338h                        | 0339h   | 033Ah   | 033Bh   | 033Ch   | 033Dh   | 033Eh   | 033Fh   |
| **0340h**      | 0340h                        | 0341h   | 0342h   | 0343h   | 0344h   | 0345h   | 0346h   | 0347h   |
| **0348h**      | 0348h                        | 0349h   | 034Ah   | 034Bh   | 034Ch   | 034Dh   | 034Eh   | 034Fh   |
| **0350h**      | 0350h                        | 0351h   | 0352h   | 0353h   | 0354h   | 0355h   | 0356h   | 0357h   |
| **0358h**      | 0358h                        | 0359h   | 035Ah   | 035Bh   | 035Ch   | 035Dh   | 035Eh   | 035Fh   |
| **0360h**      | 0360h                        | 0361h   | 0362h   | 0363h   | 0364h   | 0365h   | 0366h   | 0367h   |
| **0368h**      | 0368h                        | 0369h   | 036Ah   | 036Bh   | 036Ch   | 036Dh   | 036Eh   | 036Fh   |
| **0370h**      | 0370h                        | 0371h   | 0372h   | 0373h   | 0374h   | 0375h   | 0376h   | 0377h   |
| **0378h**      | 0378h                        | 0379h   | 037Ah   | 03FDh   | 03FEh   | 03FFh   | 037Eh   | 037Fh   |
| **0380h**      | 0380h                        | 0381h   | 0382h   | 0383h   | 0384h   | 0385h   | 0386h   | 0387h   |
| **0388h**      | 0388h                        | 0389h   | 038Ah   | 038Bh   | 038Ch   | 038Dh   | 038Eh   | 038Fh   |
| **0390h**      | 0390h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **0398h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03A0h**      | 03A0h                        | 03A1h   | 03A2h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03A8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 0386h   | 0388h   | 0389h   | 038Ah   |
| **03B0h**      | 03B0h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **03B8h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03C0h**      | 03A0h                        | 03A1h   | 03A3h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03C8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 038Ch   | 038Eh   | 038Fh   | 03CFh   |
| **03D0h**      | 03D0h                        | 03D1h   | 03D2h   | 03D3h   | 03D4h   | 03D5h   | 03D6h   | 03D7h   |
| **03D8h**      | 03D8h                        | 03D8h   | 03DAh   | 03DAh   | 03DCh   | 03DCh   | 03DEh   | 03DEh   |
| **03E0h**      | 03E0h                        | 03E0h   | 03E2h   | 03E2h   | 03E4h   | 03E4h   | 03E6h   | 03E6h   |
| **03E8h**      | 03E8h                        | 03E8h   | 03EAh   | 03EAh   | 03ECh   | 03ECh   | 03EEh   | 03EEh   |
| **03F0h**      | 03F0h                        | 03F1h   | 03F9h   | 03F3h   | 03F4h   | 03F5h   | 03F6h   | 03F7h   |
| **03F8h**      | 03F7h                        | 03F9h   | 03FAh   | 03FAh   | 03FCh   | 03FDh   | 03FEh   | 03FFh   |
| **0400h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0408h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0410h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0418h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0420h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0428h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0430h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0438h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0440h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0448h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0450h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0458h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0460h**      | 0460h                        | 0460h   | 0462h   | 0462h   | 0464h   | 0464h   | 0466h   | 0466h   |
| **0468h**      | 0468h                        | 0468h   | 046Ah   | 046Ah   | 046Ch   | 046Ch   | 046Eh   | 046Eh   |
| **0470h**      | 0470h                        | 0470h   | 0472h   | 0472h   | 0474h   | 0474h   | 0476h   | 0476h   |
| **0478h**      | 0478h                        | 0478h   | 047Ah   | 047Ah   | 047Ch   | 047Ch   | 047Eh   | 047Eh   |
| **0480h**      | 0480h                        | 0480h   | 0482h   | 0483h   | 0484h   | 0485h   | 0486h   | 0487h   |
| **0488h**      | 0488h                        | 0489h   | 048Ah   | 048Ah   | 048Ch   | 048Ch   | 048Eh   | 048Eh   |
| **0490h**      | 0490h                        | 0490h   | 0492h   | 0492h   | 0494h   | 0494h   | 0496h   | 0496h   |
| **0498h**      | 0498h                        | 0498h   | 049Ah   | 049Ah   | 049Ch   | 049Ch   | 049Eh   | 049Eh   |
| **04A0h**      | 04A0h                        | 04A0h   | 04A2h   | 04A2h   | 04A4h   | 04A4h   | 04A6h   | 04A6h   |
| **04A8h**      | 04A8h                        | 04A8h   | 04AAh   | 04AAh   | 04ACh   | 04ACh   | 04AEh   | 04AEh   |
| **04B0h**      | 04B0h                        | 04B0h   | 04B2h   | 04B2h   | 04B4h   | 04B4h   | 04B6h   | 04B6h   |
| **04B8h**      | 04B8h                        | 04B8h   | 04BAh   | 04BAh   | 04BCh   | 04BCh   | 04BEh   | 04BEh   |
| **04C0h**      | 04C0h                        | 04C1h   | 04C1h   | 04C3h   | 04C3h   | 04C5h   | 04C5h   | 04C7h   |
| **04C8h**      | 04C7h                        | 04C9h   | 04C9h   | 04CBh   | 04CBh   | 04CDh   | 04CDh   | 04C0h   |
| **04D0h**      | 04D0h                        | 04D0h   | 04D2h   | 04D2h   | 04D4h   | 04D4h   | 04D6h   | 04D6h   |
| **04D8h**      | 04D8h                        | 04D8h   | 04DAh   | 04DAh   | 04DCh   | 04DCh   | 04DEh   | 04DEh   |
| **04E0h**      | 04E0h                        | 04E0h   | 04E2h   | 04E2h   | 04E4h   | 04E4h   | 04E6h   | 04E6h   |
| **04E8h**      | 04E8h                        | 04E8h   | 04EAh   | 04EAh   | 04ECh   | 04ECh   | 04EEh   | 04EEh   |
| **04F0h**      | 04F0h                        | 04F0h   | 04F2h   | 04F2h   | 04F4h   | 04F4h   | 04F6h   | 04F6h   |
| **04F8h**      | 04F8h                        | 04F8h   | 04FAh   | 04FAh   | 04FCh   | 04FCh   | 04FEh   | 04FEh   |
| **0500h**      | 0500h                        | 0500h   | 0502h   | 0502h   | 0504h   | 0504h   | 0506h   | 0506h   |
| **0508h**      | 0508h                        | 0508h   | 050Ah   | 050Ah   | 050Ch   | 050Ch   | 050Eh   | 050Eh   |
| **0510h**      | 0510h                        | 0510h   | 0512h   | 0512h   | 0514h   | 0515h   | 0516h   | 0517h   |
| **0518h**      | 0518h                        | 0519h   | 051Ah   | 051Bh   | 051Ch   | 051Dh   | 051Eh   | 051Fh   |
| **0520h**      | 0520h                        | 0521h   | 0522h   | 0523h   | 0524h   | 0525h   | 0526h   | 0527h   |
| **0528h**      | 0528h                        | 0529h   | 052Ah   | 052Bh   | 052Ch   | 052Dh   | 052Eh   | 052Fh   |
| **0530h**      | 0530h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0538h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0540h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0548h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0550h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | 0557h   |
| **0558h**      | 0558h                        | 0559h   | 055Ah   | 055Bh   | 055Ch   | 055Dh   | 055Eh   | 055Fh   |
| **0560h**      | 0560h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0568h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0570h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0578h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0580h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | FFFFh   |
| **0588h**      | 17F6h                        | 2C63h   | 1D7Eh   | 1D7Fh   | 1D80h   | 1D81h   | 1D82h   | 1D83h   |
| **0590h**      | 1D84h                        | 1D85h   | 1D86h   | 1D87h   | 1D88h   | 1D89h   | 1D8Ah   | 1D8Bh   |
| **0598h**      | 1D8Ch                        | 1D8Dh   | 1D8Eh   | 1D8Fh   | 1D90h   | 1D91h   | 1D92h   | 1D93h   |
| **05A0h**      | 1D94h                        | 1D95h   | 1D96h   | 1D97h   | 1D98h   | 1D99h   | 1D9Ah   | 1D9Bh   |
| **05A8h**      | 1D9Ch                        | 1D9Dh   | 1D9Eh   | 1D9Fh   | 1DA0h   | 1DA1h   | 1DA2h   | 1DA3h   |
| **05B0h**      | 1DA4h                        | 1DA5h   | 1DA6h   | 1DA7h   | 1DA8h   | 1DA9h   | 1DAAh   | 1DABh   |
| **05B8h**      | 1DACh                        | 1DADh   | 1DAEh   | 1DAFh   | 1DB0h   | 1DB1h   | 1DB2h   | 1DB3h   |
| **05C0h**      | 1DB4h                        | 1DB5h   | 1DB6h   | 1DB7h   | 1DB8h   | 1DB9h   | 1DBAh   | 1DBBh   |
| **05C8h**      | 1DBCh                        | 1DBDh   | 1DBEh   | 1DBFh   | 1DC0h   | 1DC1h   | 1DC2h   | 1DC3h   |
| **05D0h**      | 1DC4h                        | 1DC5h   | 1DC6h   | 1DC7h   | 1DC8h   | 1DC9h   | 1DCAh   | 1DCBh   |
| **05D8h**      | 1DCCh                        | 1DCDh   | 1DCEh   | 1DCFh   | 1DD0h   | 1DD1h   | 1DD2h   | 1DD3h   |
| **05E0h**      | 1DD4h                        | 1DD5h   | 1DD6h   | 1DD7h   | 1DD8h   | 1DD9h   | 1DDAh   | 1DDBh   |
| **05E8h**      | 1DDCh                        | 1DDDh   | 1DDEh   | 1DDFh   | 1DE0h   | 1DE1h   | 1DE2h   | 1DE3h   |
| **05F0h**      | 1DE4h                        | 1DE5h   | 1DE6h   | 1DE7h   | 1DE8h   | 1DE9h   | 1DEAh   | 1DEBh   |
| **05F8h**      | 1DECh                        | 1DEDh   | 1DEEh   | 1DEFh   | 1DF0h   | 1DF1h   | 1DF2h   | 1DF3h   |
| **0600h**      | 1DF4h                        | 1DF5h   | 1DF6h   | 1DF7h   | 1DF8h   | 1DF9h   | 1DFAh   | 1DFBh   |
| **0608h**      | 1DFCh                        | 1DFDh   | 1DFEh   | 1DFFh   | 1E00h   | 1E00h   | 1E02h   | 1E02h   |
| **0610h**      | 1E04h                        | 1E04h   | 1E06h   | 1E06h   | 1E08h   | 1E08h   | 1E0Ah   | 1E0Ah   |
| **0618h**      | 1E0Ch                        | 1E0Ch   | 1E0Eh   | 1E0Eh   | 1E10h   | 1E10h   | 1E12h   | 1E12h   |
| **0620h**      | 1E14h                        | 1E14h   | 1E16h   | 1E16h   | 1E18h   | 1E18h   | 1E1Ah   | 1E1Ah   |
| **0628h**      | 1E1Ch                        | 1E1Ch   | 1E1Eh   | 1E1Eh   | 1E20h   | 1E20h   | 1E22h   | 1E22h   |
| **0630h**      | 1E24h                        | 1E24h   | 1E26h   | 1E26h   | 1E28h   | 1E28h   | 1E2Ah   | 1E2Ah   |
| **0638h**      | 1E2Ch                        | 1E2Ch   | 1E2Eh   | 1E2Eh   | 1E30h   | 1E30h   | 1E32h   | 1E32h   |
| **0640h**      | 1E34h                        | 1E34h   | 1E36h   | 1E36h   | 1E38h   | 1E38h   | 1E3Ah   | 1E3Ah   |
| **0648h**      | 1E3Ch                        | 1E3Ch   | 1E3Eh   | 1E3Eh   | 1E40h   | 1E40h   | 1E42h   | 1E42h   |
| **0650h**      | 1E44h                        | 1E44h   | 1E46h   | 1E46h   | 1E48h   | 1E48h   | 1E4Ah   | 1E4Ah   |
| **0658h**      | 1E4Ch                        | 1E4Ch   | 1E4Eh   | 1E4Eh   | 1E50h   | 1E50h   | 1E52h   | 1E52h   |
| **0660h**      | 1E54h                        | 1E54h   | 1E56h   | 1E56h   | 1E58h   | 1E58h   | 1E5Ah   | 1E5Ah   |
| **0668h**      | 1E5Ch                        | 1E5Ch   | 1E5Eh   | 1E5Eh   | 1E60h   | 1E60h   | 1E62h   | 1E62h   |
| **0670h**      | 1E64h                        | 1E64h   | 1E66h   | 1E66h   | 1E68h   | 1E68h   | 1E6Ah   | 1E6Ah   |
| **0678h**      | 1E6Ch                        | 1E6Ch   | 1E6Eh   | 1E6Eh   | 1E70h   | 1E70h   | 1E72h   | 1E72h   |
| **0680h**      | 1E74h                        | 1E74h   | 1E76h   | 1E76h   | 1E78h   | 1E78h   | 1E7Ah   | 1E7Ah   |
| **0688h**      | 1E7Ch                        | 1E7Ch   | 1E7Eh   | 1E7Eh   | 1E80h   | 1E80h   | 1E82h   | 1E82h   |
| **0690h**      | 1E84h                        | 1E84h   | 1E86h   | 1E86h   | 1E88h   | 1E88h   | 1E8Ah   | 1E8Ah   |
| **0698h**      | 1E8Ch                        | 1E8Ch   | 1E8Eh   | 1E8Eh   | 1E90h   | 1E90h   | 1E92h   | 1E92h   |
| **06A0h**      | 1E94h                        | 1E94h   | 1E96h   | 1E97h   | 1E98h   | 1E99h   | 1E9Ah   | 1E9Bh   |
| **06A8h**      | 1E9Ch                        | 1E9Dh   | 1E9Eh   | 1E9Fh   | 1EA0h   | 1EA0h   | 1EA2h   | 1EA2h   |
| **06B0h**      | 1EA4h                        | 1EA4h   | 1EA6h   | 1EA6h   | 1EA8h   | 1EA8h   | 1EAAh   | 1EAAh   |
| **06B8h**      | 1EACh                        | 1EACh   | 1EAEh   | 1EAEh   | 1EB0h   | 1EB0h   | 1EB2h   | 1EB2h   |
| **06C0h**      | 1EB4h                        | 1EB4h   | 1EB6h   | 1EB6h   | 1EB8h   | 1EB8h   | 1EBAh   | 1EBAh   |
| **06C8h**      | 1EBCh                        | 1EBCh   | 1EBEh   | 1EBEh   | 1EC0h   | 1EC0h   | 1EC2h   | 1EC2h   |
| **06D0h**      | 1EC4h                        | 1EC4h   | 1EC6h   | 1EC6h   | 1EC8h   | 1EC8h   | 1ECAh   | 1ECAh   |
| **06D8h**      | 1ECCh                        | 1ECCh   | 1ECEh   | 1ECEh   | 1ED0h   | 1ED0h   | 1ED2h   | 1ED2h   |
| **06E0h**      | 1ED4h                        | 1ED4h   | 1ED6h   | 1ED6h   | 1ED8h   | 1ED8h   | 1EDAh   | 1EDAh   |
| **06E8h**      | 1EDCh                        | 1EDCh   | 1EDEh   | 1EDEh   | 1EE0h   | 1EE0h   | 1EE2h   | 1EE2h   |
| **06F0h**      | 1EE4h                        | 1EE4h   | 1EE6h   | 1EE6h   | 1EE8h   | 1EE8h   | 1EEAh   | 1EEAh   |
| **06F8h**      | 1EECh                        | 1EECh   | 1EEEh   | 1EEEh   | 1EF0h   | 1EF0h   | 1EF2h   | 1EF2h   |
| **0700h**      | 1EF4h                        | 1EF4h   | 1EF6h   | 1EF6h   | 1EF8h   | 1EF8h   | 1EFAh   | 1EFBh   |
| **0708h**      | 1EFCh                        | 1EFDh   | 1EFEh   | 1EFFh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0710h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0718h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0720h**      | 1F1Ch                        | 1F1Dh   | 1F16h   | 1F17h   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0728h**      | 1F1Ch                        | 1F1Dh   | 1F1Eh   | 1F1Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0730h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0738h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0740h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0748h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0750h**      | 1F4Ch                        | 1F4Dh   | 1F46h   | 1F47h   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0758h**      | 1F4Ch                        | 1F4Dh   | 1F4Eh   | 1F4Fh   | 1F50h   | 1F59h   | 1F52h   | 1F5Bh   |
| **0760h**      | 1F54h                        | 1F5Dh   | 1F56h   | 1F5Fh   | 1F58h   | 1F59h   | 1F5Ah   | 1F5Bh   |
| **0768h**      | 1F5Ch                        | 1F5Dh   | 1F5Eh   | 1F5Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0770h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0778h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1FBAh   | 1FBBh   | 1FC8h   | 1FC9h   |
| **0780h**      | 1FCAh                        | 1FCBh   | 1FDAh   | 1FDBh   | 1FF8h   | 1FF9h   | 1FEAh   | 1FEBh   |
| **0788h**      | 1FFAh                        | 1FFBh   | 1F7Eh   | 1F7Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0790h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0798h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A0h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A8h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B0h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B8h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FB8h   | 1FB9h   | 1FB2h   | 1FBCh   |
| **07C0h**      | 1FB4h                        | 1FB5h   | 1FB6h   | 1FB7h   | 1FB8h   | 1FB9h   | 1FBAh   | 1FBBh   |
| **07C8h**      | 1FBCh                        | 1FBDh   | 1FBEh   | 1FBFh   | 1FC0h   | 1FC1h   | 1FC2h   | 1FC3h   |
| **07D0h**      | 1FC4h                        | 1FC5h   | 1FC6h   | 1FC7h   | 1FC8h   | 1FC9h   | 1FCAh   | 1FCBh   |
| **07D8h**      | 1FC3h                        | 1FCDh   | 1FCEh   | 1FCFh   | 1FD8h   | 1FD9h   | 1FD2h   | 1FD3h   |
| **07E0h**      | 1FD4h                        | 1FD5h   | 1FD6h   | 1FD7h   | 1FD8h   | 1FD9h   | 1FDAh   | 1FDBh   |
| **07E8h**      | 1FDCh                        | 1FDDh   | 1FDEh   | 1FDFh   | 1FE8h   | 1FE9h   | 1FE2h   | 1FE3h   |
| **07F0h**      | 1FE4h                        | 1FECh   | 1FE6h   | 1FE7h   | 1FE8h   | 1FE9h   | 1FEAh   | 1FEBh   |
| **07F8h**      | 1FECh                        | 1FEDh   | 1FEEh   | 1FEFh   | 1FF0h   | 1FF1h   | 1FF2h   | 1FF3h   |
| **0800h**      | 1FF4h                        | 1FF5h   | 1FF6h   | 1FF7h   | 1FF8h   | 1FF9h   | 1FFAh   | 1FFBh   |
| **0808h**      | 1FF3h                        | 1FFDh   | 1FFEh   | 1FFFh   | 2000h   | 2001h   | 2002h   | 2003h   |
| **0810h**      | 2004h                        | 2005h   | 2006h   | 2007h   | 2008h   | 2009h   | 200Ah   | 200Bh   |
| **0818h**      | 200Ch                        | 200Dh   | 200Eh   | 200Fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201Ah   | 201Bh   |
| **0828h**      | 201Ch                        | 201Dh   | 201Eh   | 201Fh   | 2020h   | 2021h   | 2022h   | 2023h   |
| **0830h**      | 2024h                        | 2025h   | 2026h   | 2027h   | 2028h   | 2029h   | 202Ah   | 202Bh   |
| **0838h**      | 202Ch                        | 202Dh   | 202Eh   | 202Fh   | 2030h   | 2031h   | 2032h   | 2033h   |
| **0840h**      | 2034h                        | 2035h   | 2036h   | 2037h   | 2038h   | 2039h   | 203Ah   | 203Bh   |
| **0848h**      | 203Ch                        | 203Dh   | 203Eh   | 203Fh   | 2040h   | 2041h   | 2042h   | 2043h   |
| **0850h**      | 2044h                        | 2045h   | 2046h   | 2047h   | 2048h   | 2049h   | 204Ah   | 204Bh   |
| **0858h**      | 204Ch                        | 204Dh   | 204Eh   | 204Fh   | 2050h   | 2051h   | 2052h   | 2053h   |
| **0860h**      | 2054h                        | 2055h   | 2056h   | 2057h   | 2058h   | 2059h   | 205Ah   | 205Bh   |
| **0868h**      | 205Ch                        | 205Dh   | 205Eh   | 205Fh   | 2060h   | 2061h   | 2062h   | 2063h   |
| **0870h**      | 2064h                        | 2065h   | 2066h   | 2067h   | 2068h   | 2069h   | 206Ah   | 206Bh   |
| **0878h**      | 206Ch                        | 206Dh   | 206Eh   | 206Fh   | 2070h   | 2071h   | 2072h   | 2073h   |
| **0880h**      | 2074h                        | 2075h   | 2076h   | 2077h   | 2078h   | 2079h   | 207Ah   | 207Bh   |
| **0888h**      | 207Ch                        | 207Dh   | 207Eh   | 207Fh   | 2080h   | 2081h   | 2082h   | 2083h   |
| **0890h**      | 2084h                        | 2085h   | 2086h   | 2087h   | 2088h   | 2089h   | 208Ah   | 208Bh   |
| **0898h**      | 208Ch                        | 208Dh   | 208Eh   | 208Fh   | 2090h   | 2091h   | 2092h   | 2093h   |
| **08A0h**      | 2094h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209Ah   | 209Bh   |
| **08A8h**      | 209Ch                        | 209Dh   | 209Eh   | 209Fh   | 20A0h   | 20A1h   | 20A2h   | 20A3h   |
| **08B0h**      | 20A4h                        | 20A5h   | 20A6h   | 20A7h   | 20A8h   | 20A9h   | 20AAh   | 20ABh   |
| **08B8h**      | 20ACh                        | 20ADh   | 20AEh   | 20AFh   | 20B0h   | 20B1h   | 20B2h   | 20B3h   |
| **08C0h**      | 20B4h                        | 20B5h   | 20B6h   | 20B7h   | 20B8h   | 20B9h   | 20BAh   | 20BBh   |
| **08C8h**      | 20BCh                        | 20BDh   | 20BEh   | 20BFh   | 20C0h   | 20C1h   | 20C2h   | 20C3h   |
| **08D0h**      | 20C4h                        | 20C5h   | 20C6h   | 20C7h   | 20C8h   | 20C9h   | 20CAh   | 20CBh   |
| **08D8h**      | 20CCh                        | 20CDh   | 20CEh   | 20CFh   | 20D0h   | 20D1h   | 20D2h   | 20D3h   |
| **08E0h**      | 20D4h                        | 20D5h   | 20D6h   | 20D7h   | 20D8h   | 20D9h   | 20DAh   | 20DBh   |
| **08E8h**      | 20DCh                        | 20DDh   | 20DEh   | 20DFh   | 20E0h   | 20E1h   | 20E2h   | 20E3h   |
| **08F0h**      | 20E4h                        | 20E5h   | 20E6h   | 20E7h   | 20E8h   | 20E9h   | 20EAh   | 20EBh   |
| **08F8h**      | 20ECh                        | 20EDh   | 20EEh   | 20EFh   | 20F0h   | 20F1h   | 20F2h   | 20F3h   |
| **0900h**      | 20F4h                        | 20F5h   | 20F6h   | 20F7h   | 20F8h   | 20F9h   | 20FAh   | 20FBh   |
| **0908h**      | 20FCh                        | 20FDh   | 20FEh   | 20FFh   | 2100h   | 2101h   | 2102h   | 2103h   |
| **0910h**      | 2104h                        | 2105h   | 2106h   | 2107h   | 2108h   | 2109h   | 210Ah   | 210Bh   |
| **0918h**      | 210Ch                        | 210Dh   | 210Eh   | 210Fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114h                        | 2115h   | 2116h   | 2117h   | 2118h   | 2119h   | 211Ah   | 211Bh   |
| **0928h**      | 211Ch                        | 211Dh   | 211Eh   | 211Fh   | 2120h   | 2121h   | 2122h   | 2123h   |
| **0930h**      | 2124h                        | 2125h   | 2126h   | 2127h   | 2128h   | 2129h   | 212Ah   | 212Bh   |
| **0938h**      | 212Ch                        | 212Dh   | 212Eh   | 212Fh   | 2130h   | 2131h   | 2132h   | 2133h   |
| **0940h**      | 2134h                        | 2135h   | 2136h   | 2137h   | 2138h   | 2139h   | 213Ah   | 213Bh   |
| **0948h**      | 213Ch                        | 213Dh   | 213Eh   | 213Fh   | 2140h   | 2141h   | 2142h   | 2143h   |
| **0950h**      | 2144h                        | 2145h   | 2146h   | 2147h   | 2148h   | 2149h   | 214H   | 214Bh   |
| **0958h**      | 214Ch                        | 214Dh   | 2132h   | 214Fh   | 2150h   | 2151h   | 2152h   | 2153h   |
| **0960h**      | 2154h                        | 2155h   | 2156h   | 2157h   | 2158h   | 2159h   | 215H   | 215Bh   |
| **0968h**      | 215Ch                        | 215Dh   | 215Eh   | 215Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0970h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216H   | 216Bh   |
| **0978h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0980h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216H   | 216Bh   |
| **0988h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2180h   | 2181h   | 2182h   | 2183h   |
| **0990h**      | 2183h                        | FFFFh   | 034Bh   | 24B6h   | 24B7h   | 24B8h   | 24B9h   | 24BAh   |
| **0998h**      | 24Bh                        | 24BCh   | 24BDh   | 24BEh   | 24BFh   | 24C0h   | 24C1h   | 24C2h   |
| **09A0h**      | 24C3h                        | 24C4h   | 24C5h   | 24C6h   | 24C7h   | 24C8h   | 24C9h   | 24CAh   |
| **09A8h**      | 24CBh                        | 24CCh   | 24CDh   | 24CEh   | 24CFh   | FFFFh   | 0746h   | 2C00h   |
| **09B0h**      | 2C01h                        | 2C02h   | 2C03h   | 2C04h   | 2C05h   | 2C06h   | 2C07h   | 2C08h   |
| **09B8h**      | 2C09h                        | 2C0Ah   | 2C0Bh   | 2C0Ch   | 2C0Dh   | 2C0Eh   | 2C0Fh   | 2C10h   |
| **09C0h**      | 2C11h                        | 2C12h   | 2C13h   | 2C14h   | 2C15h   | 2C16h   | 2C17h   | 2C18h   |
| **09C8h**      | 2C19h                        | 2C1Ah   | 2C1Bh   | 2C1Ch   | 2C1Dh   | 2C1Eh   | 2C1Fh   | 2C20h   |
| **09D0h**      | 2C21h                        | 2C22h   | 2C23h   | 2C24h   | 2C25h   | 2C26h   | 2C27h   | 2C28h   |
| **09D8h**      | 2C29h                        | 2C2Ah   | 2C2Bh   | 2C2Ch   | 2C2Dh   | 2C2Eh   | 2C5Fh   | 2C60h   |
| **09E0h**      | 2C60h                        | 2C62h   | 2C63h   | 2C64h   | 2C65h   | 2C66h   | 2C67h   | 2C67h   |
| **09E8h**      | 2C69h                        | 2C69h   | 2C6Bh   | 2C6Bh   | 2C6Dh   | 2C6Eh   | 2C6Fh   | 2C70h   |
| **09F0h**      | 2C71h                        | 2C72h   | 2C73h   | 2C74h   | 2C75h   | 2C75h   | 2C77h   | 2C78h   |
| **09F8h**      | 2C79h                        | 2C7Ah   | 2C7Bh   | 2C7Ch   | 2C7Dh   | 2C7Eh   | 2C7Fh   | 2C80h   |
| **0A00h**      | 2C80h                        | 2C82h   | 2C82h   | 2C84h   | 2C84h   | 2C86h   | 2C86h   | 2C88h   |
| **0A08h**      | 2C88h                        | 2C8Ah   | 2C8Ah   | 2C8Ch   | 2C8Ch   | 2C8Eh   | 2C8Eh   | 2C90h   |
| **0A10h**      | 2C90h                        | 2C92h   | 2C92h   | 2C94h   | 2C94h   | 2C96h   | 2C96h   | 2C98h   |
| **0A18h**      | 2C98h                        | 2C9Ah   | 2C9Ah   | 2C9Ch   | 2C9Ch   | 2C9Eh   | 2C9Eh   | 2CA0h   |
| **0A20h**      | 2CA0h                        | 2CA2h   | 2CA2h   | 2CA4h   | 2CA4h   | 2CA6h   | 2CA6h   | 2CA8h   |
| **0A28h**      | 2CA8h                        | 2CAAh   | 2CAAh   | 2CACh   | 2CACh   | 2CAEh   | 2CAEh   | 2CB0h   |
| **0A30h**      | 2CB0h                        | 2CB2h   | 2CB2h   | 2CB4h   | 2CB4h   | 2CB6h   | 2CB6h   | 2CB8h   |
| **0A38h**      | 2CB8h                        | 2CBAh   | 2CBAh   | 2CBCh   | 2CBCh   | 2CBEh   | 2CBEh   | 2CC0h   |
| **0A40h**      | 2CC0h                        | 2CC2h   | 2CC2h   | 2CC4h   | 2CC4h   | 2CC6h   | 2CC6h   | 2CC8h   |
| **0A48h**      | 2CC8h                        | 2CCAh   | 2CCAh   | 2CCCh   | 2CCCh   | 2CCEh   | 2CCEh   | 2CD0h   |
| **0A50h**      | 2CD0h                        | 2CD2h   | 2CD2h   | 2CD4h   | 2CD4h   | 2CD6h   | 2CD6h   | 2CD8h   |
| **0A58h**      | 2CD8h                        | 2CDAh   | 2CDAh   | 2CDCh   | 2CDCh   | 2CDEh   | 2CDEh   | 2CE0h   |
| **0A60h**      | 2CE0h                        | 2CE2h   | 2CE2h   | 2CE4h   | 2CE5h   | 2CE6h   | 2CE7h   | 2CE8h   |
| **0A68h**      | 2CE9h                        | 2CEAh   | 2CEBh   | 2CECh   | 2CEDh   | 2CEEh   | 2CEFh   | 2CF0h   |
| **0A70h**      | 2CF1h                        | 2CF2h   | 2CF3h   | 2CF4h   | 2CF5h   | 2CF6h   | 2CF7h   | 2CF8h   |
| **0A78h**      | 2CF9h                        | 2CFAh   | 2CFBh   | 2CFCh   | 2CFDh   | 2CFEh   | 2CFFh   | 10A0h   |
| **0A80h**      | 10A1h                        | 10A2h   | 10A3h   | 10A4h   | 10A5h   | 10A6h   | 10A7h   | 10A8h   |
| **0A88h**      | 10A9h                        | 10AAh   | 10ABh   | 10ACh   | 10ADh   | 10AEh   | 10AFh   | 10B0h   |
| **0A90h**      | 10B1h                        | 10B2h   | 10B3h   | 10B4h   | 10B5h   | 10B6h   | 10B7h   | 10B8h   |
| **0A98h**      | 10B9h                        | 10BAh   | 10Bh   | 10BCh   | 10BDh   | 10BEh   | 10BFh   | 10C0h   |
| **0AA0h**      | 10C1h                        | 10C2h   | 10C3h   | 10C4h   | 10C5h   | FFFFh   | D21Bh   | FF21h   |
| **0AA8h**      | FF22h                        | FF23h   | FF24h   | FF25h   | FF26h   | FF27h   | FF28h   | FF29h   |
| **0AB0h**      | FF2Ah                        | FF2Bh   | FF2Ch   | FF2Dh   | FF2Eh   | FF2Fh   | FF30h   | FF31h   |
| **0AB8h**      | FF32h                        | FF33h   | FF34h   | FF35h   | FF36h   | FF37h   | FF38h   | FF39h   |
| **0AC0h**      | FF3Ah                        | FF5Bh   | FF5Ch   | FF5Dh   | FF5Eh   | FF5Fh   | FF60h   | FF61h   |
| **0AC8h**      | FF62h                        | FF63h   | FF64h   | FF65h   | FF66h   | FF67h   | FF68h   | FF69h   |
| **0AD0h**      | FF6Ah                        | FF6Bh   | FF6Ch   | FF6Dh   | FF6Eh   | FF6Fh   | FF70h   | FF71h   |
| **0AD8h**      | FF72h                        | FF73h   | FF74h   | FF75h   | FF76h   | FF77h   | FF78h   | FF79h   |
| **0AE0h**      | FF7Ah                        | FF7Bh   | FF7Ch   | FF7Dh   | FF7Eh   | FF7Fh   | FF80h   | FF81h   |
| **0AE8h**      | FF82h                        | FF83h   | FF84h   | FF85h   | FF86h   | FF87h   | FF88h   | FF89h   |
| **0AF0h**      | FF8Ah                        | FF8Bh   | FF8Ch   | FF8Dh   | FF8Eh   | FF8Fh   | FF90h   | FF91h   |
| **0AF8h**      | FF92h                        | FF93h   | FF94h   | FF95h   | FF96h   | FF97h   | FF98h   | FF99h   |
| **0B00h**      | FF9Ah                        | FF9Bh   | FF9Ch   | FF9Dh   | FF9Eh   | FF9Fh   | FFA0h   | FFA1h   |
| **0B08h**      | FFA2h                        | FFA3h   | FFA4h   | FFA5h   | FFA6h   | FFA7h   | FFA8h   | FFA9h   |
| **0B10h**      | FFAAh                        | FFABh   | FFACh   | FFADh   | FFAEh   | FFAFh   | FFB0h   | FFB1h   |
| **0B18h**      | FFB2h                        | FFB3h   | FFB4h   | FFB5h   | FFB6h   | FFB7h   | FFB8h   | FFB9h   |
| **0B20h**      | FFBAh                        | FFBBh   | FFBCh   | FFBDh   | FFBEh   | FFBFh   | FFC0h   | FFC1h   |
| **0B28h**      | FFC2h                        | FFC3h   | FFC4h   | FFC5h   | FFC6h   | FFC7h   | FFC8h   | FFC9h   |
| **0B30h**      | FFCAh                        | FFCBh   | FFCCh   | FFCDh   | FFCEh   | FFCFh   | FFD0h   | FFD1h   |
| **0B38h**      | FFD2h                        | FFD3h   | FFD4h   | FFD5h   | FFD6h   | FFD7h   | FFD8h   | FFD9h   |
| **0B40h**      | FFDAh                        | FFDBh   | FFDCh   | FFDDh   | FFDEh   | FFDFh   | FFE0h   | FFE1h   |
| **0B48h**      | FFE2h                        | FFE3h   | FFE4h   | FFE5h   | FFE6h   | FFE7h   | FFE8h   | FFE9h   |
| **0B50h**      | FFEAh                        | FFEBh   | FFECh   | FFEDh   | FFEEh   | FFEFh   | FFF0h   | FFF1h   |
| **0B58h**      | FFF2h                        | FFF3h   | FFF4h   | FFF5h   | FFF6h   | FFF7h   | FFF8h   | FFF9h   |
| **0B60h**      | FFFAh                        | FFFBh   | FFFCh   | FFFDh   | FFFEh   | FFFFh   |         |         |

### <a name="73-volume-label-directory-entry"></a>7.3 Entrada de diretório de rótulo de volume

O Rótulo do Volume é uma cadeia de caracteres Unicode que permite que os usuários finais diferenciem seus volumes de armazenamento. No sistema de arquivos exFAT, o Rótulo do Volume existe como uma entrada de diretório primário crítica no diretório raiz (consulte [Tabela 26](#table-26-volume-label-directoryentry-structure)). O número válido de entradas de diretório de Rótulo de Volume varia de 0 a 1.

<div id="table-26-volume-label-directoryentry-structure" />

**Tabela 26 Diretório de Rótulo de VolumeE estrutura de entrada**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#731-entrytype-field">a Seção 7.3.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>CharacterCount</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#732-charactercount-field">a Seção 7.3.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>Esse campo é obrigatório e <a href="#733-volumelabel-field">a Seção 7.3.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>24</td>
<td>8</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>Campo EntryType 7.3.1

O campo EntryType deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Primário Genérico (consulte [a Seção 6.3.1](#631-entrytype-field)).

##### <a name="7311-typecode-field"></a>Campo TypeCode 7.3.1.1

O campo TypeCode deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.1.1](#6311-typecode-field)).

Para a entrada do diretório Rótulo do Volume, o valor válido para esse campo é
3.

##### <a name="7312-typeimportance-field"></a>Campo TypeImportance 7.3.1.2

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.1.2](#6312-typeimportance-field)).

Para a entrada do diretório Rótulo do Volume, o valor válido para esse campo é
0.

##### <a name="7313-typecategory-field"></a>Campo TypeCategory 7.3.1.3

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.1.3](#6313-typecategory-field)).

##### <a name="7314-inuse-field"></a>7.3.1.4 Campo de inutilização

O campo InUse deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a [Seção 6.3.1.4](#6314-inuse-field)).

#### <a name="732-charactercount-field"></a>Campo CharacterCount 7.3.2

O campo CharacterCount deve conter o comprimento da cadeia de caracteres Unicode que o campo VolumeLabel contém.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 0, o que significa que a cadeia de caracteres Unicode tem 0 caracteres (que é o equivalente a nenhum rótulo de volume)

- No máximo 11, o que significa que a cadeia de caracteres Unicode tem 11 caracteres

#### <a name="733-volumelabel-field"></a>7.3.3 Campo VolumeLabel

O campo VolumeLabel deve conter uma cadeia de caracteres Unicode, que é o nome amigável do volume. O campo VolumeLabel tem o mesmo conjunto de caracteres inválidos que o campo FileName da entrada do diretório Nome do Arquivo (consulte [a Seção 7.7.3](#773-filename-field)).

### <a name="74-file-directory-entry"></a>7.4 Entrada do Diretório de Arquivos

As entradas do diretório de arquivos descrevem arquivos e diretórios. Elas são entradas de diretório primário críticas e qualquer diretório pode conter zero ou mais entradas de diretório de arquivo (consulte [Tabela 27](#table-27-file-directoryentry)). Para que uma entrada de diretório de arquivo seja válida, exatamente uma entrada de diretório da Extensão de Fluxo e pelo menos uma entrada de diretório Nome de Arquivo devem seguir imediatamente a entrada Diretório de arquivos (consulte a Seção [7.6](#76-stream-extension-directory-entry) e a [Seção 7.7,](#77-file-name-directory-entry)respectivamente).

<div id="table-27-file-directoryentry" />

**Tabela 27 File DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório <a href="#741-entrytype-field">e a Seção 7.4.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#742-secondarycount-field">a Seção 7.4.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Esse campo é obrigatório e <a href="#743-setchecksum-field">a Seção 7.4.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Fileattributes</td>
<td>4</td>
<td>2</td>
<td>Esse campo é obrigatório e <a href="#744-fileattributes-field">a Seção 7.4.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>6</td>
<td>2</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="even">
<td>CreateTimestamp</td>
<td>8</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> a Seção 7.4.5 </
a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>LastModifiedTimestamp</td>
<td>12</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">a Seção 7.4.6</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>LastAccessedTimestamp</td>
<td>16</td>
<td>4</td>
<td>Esse campo é obrigatório e <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">a Seção 7.4.7</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Create10msIncrement</td>
<td>20</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> a Seção 7.4.5 </
a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>LastModified10msIncrement</td>
<td>21</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">a Seção 7.4.6</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>CreateUtcOffset</td>
<td>22</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> a Seção 7.4.5 </
a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>LastModifiedUtcOffset</td>
<td>23</td>
<td>1</td>
<td>Esse campo é obrigatório e a <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">seção 7.4.6</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>LastAccessedUtcOffset</td>
<td>24</td>
<td>1</td>
<td>Esse campo é obrigatório e a <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">seção 7.4.7</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>Campo EntryType 7.4.1

O campo EntryType deve estar de acordo com a definição fornecida no modelo DirectoryEntry primário genérico (consulte a [seção 6.3.1](#631-entrytype-field)).

##### <a name="7411-typecode-field"></a>Campo 7.4.1.1 TypeCode

O campo TypeCode deve estar de acordo com a definição fornecida no modelo DirectoryEntry primário genérico (consulte a [seção 6.3.1.1](#6311-typecode-field)).

Para uma entrada de diretório de arquivo, o valor válido para esse campo é 5.

##### <a name="7412-typeimportance-field"></a>Campo 7.4.1.2 TypeImportance

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo DirectoryEntry primário genérico (consulte a [seção 6.3.1.2](#6312-typeimportance-field)).

Para uma entrada de diretório de arquivo, o valor válido para esse campo é 0.

##### <a name="7413-typecategory-field"></a>Campo 7.4.1.3 TypeCategory

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo DirectoryEntry primário genérico (consulte a [seção 6.3.1.3](#6313-typecategory-field)).

##### <a name="7414-inuse-field"></a>Campo 7.4.1.4 InUse

O campo InUse deve estar de acordo com a definição fornecida no modelo DirectoryEntry primário genérico (consulte a [seção 6.3.1.4](#6314-inuse-field)).

#### <a name="742-secondarycount-field"></a>Campo 7.4.2 SecondaryCount

O campo SecondaryCount deve estar em conformidade com a definição fornecida no modelo DirectoryEntry primário genérico (consulte a [seção 6.3.2](#632-secondarycount-field)).

#### <a name="743-setchecksum-field"></a>Campo 7.4.3 SetChecksum

O campo SetChecksum deve estar de acordo com a definição fornecida no modelo DirectoryEntry primário genérico (consulte a [seção 6.3.3](#633-setchecksum-field)).

#### <a name="744-fileattributes-field"></a>Campo FileAttributes do 7.4.4

O campo FileAttributes contém sinalizadores (consulte a [tabela 28](#table-28-fileattributes-field-structure)).

<div id="table-28-fileattributes-field-structure" />

**Tabela 28 estrutura de campo FileAttributes**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>parte</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ReadOnly</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e está de acordo com a definição do MS-DOS.</td>
</tr>
<tr class="even">
<td>Hidden</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e está de acordo com a definição do MS-DOS.</td>
</tr>
<tr class="odd">
<td>Sistema</td>
<td>2</td>
<td>1</td>
<td>Esse campo é obrigatório e está de acordo com a definição do MS-DOS.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>3</td>
<td>1</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="odd">
<td>Diretório</td>
<td>4</td>
<td>1</td>
<td>Esse campo é obrigatório e está de acordo com a definição do MS-DOS.</td>
</tr>
<tr class="even">
<td>Arquivos</td>
<td>5</td>
<td>1</td>
<td>Esse campo é obrigatório e está de acordo com a definição do MS-DOS.</td>
</tr>
<tr class="odd">
<td>Reserved2</td>
<td>6</td>
<td>10</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
</tbody>
</table>

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>Campos 7.4.5 createtimestamp, Create10msIncrement e CreateUtcOffset

Em combinação, os campos createtimestamp e CreateTime10msIncrement devem descrever a data e a hora locais em que o arquivo/diretório determinado foi criado. O campo CreateUtcOffset descreve o deslocamento da data e hora locais do UTC. As implementações devem definir esses campos após a criação do conjunto de entradas de diretório fornecido.

Esses campos devem estar em conformidade com as definições dos campos TIMESTAMP, 10msIncrement e UtcOffset (consulte a [seção 7.4.8](#748-timestamp-fields), [seção 7.4.9](#749-10msincrement-fields)e [seção 7.4.10](#7410-utcoffset-fields), respectivamente).

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>Campos 7.4.6 LastModifiedTimestamp, LastModified10msIncrement e LastModifiedUtcOffset

Em combinação, os campos LastModifiedTimestamp e LastModifiedTime10msIncrement devem descrever a data e a hora locais que o conteúdo de qualquer um dos clusters associados à entrada de diretório de extensão de fluxo fornecida foi modificado pela última vez. O campo LastModifiedUtcOffset descreve o deslocamento da data e hora locais do UTC. As implementações devem atualizar esses campos:

1. Depois de modificar o conteúdo de qualquer um dos clusters associados à entrada de diretório de extensão de fluxo determinada (exceto pelo conteúdo que existe além do ponto que o campo ValidDataLength descreve)

2. Após alterar os valores dos campos ValidDataLength ou DATALENGTH

Esses campos devem estar em conformidade com as definições dos campos TIMESTAMP, 10msIncrement e UtcOffset (consulte a [seção 7.4.8](#748-timestamp-fields), [seção 7.4.9](#749-10msincrement-fields)e [seção 7.4.10](#7410-utcoffset-fields), respectivamente).

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>Campos 7.4.7 LastAccessedTimestamp e LastAccessedUtcOffset

O campo LastAccessedTimestamp deve descrever a data e a hora locais em que o conteúdo de qualquer um dos clusters associados à entrada de diretório de extensão de fluxo fornecida foi acessado pela última vez. O campo LastAccessedUtcOffset descreve o deslocamento da data e hora locais do UTC.
As implementações devem atualizar esses campos:

1. Depois de modificar o conteúdo de qualquer um dos clusters associados à entrada de diretório de extensão de fluxo determinada (exceto pelo conteúdo que existe além do ValidDataLength)

2. Após alterar os valores dos campos ValidDataLength ou DATALENGTH

As implementações devem atualizar esses campos depois de ler o conteúdo de qualquer um dos clusters associados à entrada de diretório de extensão de fluxo fornecida.

Esses campos devem estar em conformidade com as definições dos campos TIMESTAMP e UtcOffset (consulte a [seção 7.4.8](#748-timestamp-fields) e a [seção 7.4.10](#7410-utcoffset-fields), respectivamente).

#### <a name="748-timestamp-fields"></a>Campos de carimbo de data/hora 7.4.8

Os campos de carimbo de hora descrevem a data e a hora locais, até uma resolução de dois segundos (consulte a [tabela 29](#table-29-timestamp-field-structure)).

<div id="table-29-timestamp-field-structure" />

**Tabela 29 estrutura de campo de carimbo de data/hora**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>parte</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DoubleSeconds</td>
<td>0</td>
<td>5</td>
<td>Esse campo é obrigatório e a <a href="#7481-doubleseconds-field">seção 7.4.8.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Minuto</td>
<td>5</td>
<td>6</td>
<td>Esse campo é obrigatório e a <a href="#7482-minute-field">seção 7.4.8.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Hora</td>
<td>11</td>
<td>5</td>
<td>Esse campo é obrigatório e a <a href="#7483-hour-field">seção 7.4.8.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Dia</td>
<td>16</td>
<td>5</td>
<td>Esse campo é obrigatório e a <a href="#7484-day-field">seção 7.4.8.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Mês</td>
<td>21</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#7485-month-field">seção 7.4.8.5</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>Esse campo é obrigatório e a <a href="#7486-year-field">seção 7.4.8.6</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>Campo 7.4.8.1 DoubleSeconds

O campo DoubleSeconds deve descrever a parte de segundos do campo timestamp, em múltiplos dois segundos.

O intervalo válido de valores para esse campo deve ser:

- 0, que representa 0 segundo

- 29, que representa 58 segundos

##### <a name="7482-minute-field"></a>Campo 7.4.8.2 minute

O campo de minuto deve descrever a parte de minutos do campo de carimbo de data/hora.

O intervalo válido de valores para esse campo deve ser:

- 0, que representa 0 minutos

- 59, que representa 59 minutos

##### <a name="7483-hour-field"></a>Campo de hora 7.4.8.3

O campo de hora deve descrever a parte de horas do campo de carimbo de data/hora.

O intervalo válido de valores para esse campo deve ser:

- 0, que representa 00:00 horas

- 23, que representa 23:00 horas

##### <a name="7484-day-field"></a>Campo dia do 7.4.8.4

O campo dia deve descrever a parte do dia do campo de carimbo de data/hora.

O intervalo válido de valores para esse campo deve ser:

- 1, que é o primeiro dia do mês determinado

- O último dia do mês determinado (o mês determinado define o número de dias válidos)

##### <a name="7485-month-field"></a>Campo 7.4.8.5 mês

O campo mês deve descrever a parte do mês do campo de carimbo de data/hora.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 1, que representa janeiro

- No máximo 12, que representa dezembro

##### <a name="7486-year-field"></a>Campo 7.4.8.6 year

O campo year deve descrever a parte do ano do campo timestamp, em relação ao ano 1980. Este campo representa o ano 1980 com o valor 0 e o ano 2107 com o valor 127.

Todos os valores possíveis para esse campo são válidos.

#### <a name="749-10msincrement-fields"></a>7.4.9 campos 10msIncrement

os campos 10msIncrement devem fornecer resolução de tempo adicional para seus campos de carimbo de data/hora correspondentes em múltiplos milissegundos.

O intervalo válido de valores para esses campos deve ser:

- Pelo menos 0, que representa 0 milissegundos

- No máximo 199, que representa 1990 milissegundos

#### <a name="7410-utcoffset-fields"></a>7.4.10 campos UtcOffset

Os campos UtcOffset (consulte a [tabela 30](#table-30-utcoffset-field-structure)) devem descrever o deslocamento do UTC para a data local e a hora em que os campos TIMESTAMP e 10msIncrement correspondentes são descritos. O deslocamento do UTC para a data e hora local inclui os efeitos dos fusos horários e de outros ajustes de data e hora, como o horário de verão e as alterações de horário de verão regionais.

<div id="table-30-utcoffset-field-structure" />

**Estrutura de campo de 30 UtcOffset da tabela**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>parte</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OffsetFromUtc</td>
<td>0</td>
<td>7</td>
<td>Esse campo é obrigatório e a <a href="#74101-offsetfromutc-field">seção 7.4.10.1</a>define seu conteúdo.</td>
</tr>
<tr class="even">
<td>OffsetValid</td>
<td>7</td>
<td>1</td>
<td>Esse campo é obrigatório e a <a href="#74102-offsetvalid-field">seção 7.4.10.2</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>Campo 7.4.10.1 OffsetFromUtc

O campo OffsetFromUtc deve descrever o deslocamento do UTC da data e hora locais em que os campos TIMESTAMP e 10msIncrement relacionados contêm.
Este campo descreve o deslocamento do UTC em intervalos de 15 minutos (consulte a tabela 31).

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**Tabela 31 significando os valores do campo OffsetFromUtc**

<table>
<thead>
<tr class="header">
<th><strong>Valor</strong></th>
<th><strong>Equivalente decimal assinado</strong></th>
<th><strong>Descrição</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3Fh</td>
<td>63</td>
<td>Data e hora local são UTC + 15:45</td>
</tr>
<tr class="even">
<td>3Eh</td>
<td>62</td>
<td>Data e hora local são UTC + 15:30</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>01h</td>
<td>1</td>
<td>Data e hora local são UTC + 00:15</td>
</tr>
<tr class="odd">
<td>17h</td>
<td>0</td>
<td>Data e hora local são UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>Data e hora local é UTC – 00:15</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>41h</td>
<td>-63</td>
<td>Data e hora local é UTC – 15:45</td>
</tr>
<tr class="odd">
<td>40h</td>
<td>-64</td>
<td>Data e hora local é UTC – 16:00</td>
</tr>
</tbody>
</table>

Como a tabela acima indica, todos os valores possíveis para esse campo são válidos. No entanto, as implementações só devem registrar o valor 17h para esse campo quando:

1. A data e hora locais são, na verdade, iguais às do UTC; nesse caso, o valor do campo OffsetValid deve ser 1

2. Data e hora locais não são conhecidas; nesse caso, o valor do campo OffsetValid deve ser 1 e as implementações devem considerar UTC como data e hora locais

3. UTC não é conhecido, nesse caso, o valor do campo OffsetValid deve ser 0

Se o deslocamento de data e hora local de UTC não for um múltiplo de intervalos de 15 minutos, as implementações deverão registrar 00h no campo OffsetFromUtc e considerar o UTC como data e hora locais.

##### <a name="74102-offsetvalid-field"></a>Campo OffsetValid 7.4.10.2

O campo OffsetValid deve descrever se o conteúdo do campo OffsetFromUtc é válido ou não, da seguinte forma:

- 0, o que significa que o conteúdo do campo OffsetFromUtc é inválido
    > e devem ser 00h

- 1, o que significa que o conteúdo do campo OffsetFromUtc é válido

As implementações só devem definir esse campo como o valor 0 quando UTC não estiver disponível para calcular o valor do campo OffsetFromUtc. Se esse campo contiver o valor 0, as implementações deverão tratar os campos Timestamp e 10msIncrement como tendo o mesmo deslocamento UTC que a data e hora locais atuais.

### <a name="75-volume-guid-directory-entry"></a>7.5 Entrada do diretório GUID do volume

A entrada do diretório GUID do volume contém um GUID que permite que as implementações diferenciem volumes de forma exclusiva e programática.
O GUID do Volume existe como uma entrada de diretório primário benigno no diretório raiz (consulte [Tabela 32](#table-32-volume-guid-directoryentry)). O número válido de entradas de diretório GUID de volume varia de 0 a 1.

<div id="table-32-volume-guid-directoryentry" />

**Tabela 32 Volume GUID DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#751-entrytype-field">a Seção 7.5.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#752-secondarycount-field">a Seção 7.5.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Esse campo é obrigatório e <a href="#753-setchecksum-field">a Seção 7.5.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Esse campo é obrigatório e <a href="#754-generalprimaryflags-field">a Seção 7.5.4</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>Esse campo é obrigatório e <a href="#755-volumeguid-field">a Seção 7.5.5</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>22</td>
<td>10</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>Campo EntryType 7.5.1

O campo EntryType deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Primário Genérico (consulte [a Seção 6.3.1](#631-entrytype-field)).

##### <a name="7511-typecode-field"></a>Campo TypeCode 7.5.1.1

O campo TypeCode deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.1.1](#6311-typecode-field)).

Para a entrada do diretório GUID do volume, o valor válido para esse campo é
0.

##### <a name="7512-typeimportance-field"></a>Campo TypeImportance 7.5.1.2

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.1.2](#6312-typeimportance-field)).

Para a entrada do diretório GUID do volume, o valor válido para esse campo é
1.

##### <a name="7513-typecategory-field"></a>Campo TypeCategory 7.5.1.3

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.1.3](#6313-typecategory-field)).

##### <a name="7514-inuse-field"></a>7.5.1.4 Campo de inutilização

O campo InUse deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a [Seção 6.3.1.4](#6314-inuse-field)).

#### <a name="752-secondarycount-field"></a>7.5.2 Campo SecondaryCount

O campo SecondaryCount deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.2](#632-secondarycount-field)).

Para a entrada do diretório GUID do volume, o valor válido para esse campo é
0.

#### <a name="753-setchecksum-field"></a>7.5.3 Campo SetChecksum

O campo SetChecksum deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte [a Seção 6.3.3](#633-setchecksum-field)).

#### <a name="754-generalprimaryflags-field"></a>7.5.4 Campo GeneralPrimaryFlags

O campo GeneralPrimaryFlags deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a Seção [6.3.4)](#634-generalprimaryflags-field)e define o conteúdo do campo CustomDefined a ser reservado.

##### <a name="7541-allocationpossible-field"></a>7.5.4.1 Campo AllocationPossible

O campo AllocationPossible deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.4.1](#6341-allocationpossible-field)).

Para a entrada do diretório GUID do volume, o valor válido para esse campo é
0.

##### <a name="7542-nofatchain-field"></a>7.5.4.2 Campo NoFatChain

O campo NoFatChain deve estar em conformidade com a definição fornecida no modelo Directory Primário GenéricoEntry (consulte a [Seção 6.3.4.2](#6342-nofatchain-field)).

#### <a name="755-volumeguid-field"></a>7.5.5 Campo VolumeGuid

O campo VolumeGuid deve conter um GUID que identifica exclusivamente o volume determinado.

Todos os valores possíveis para esse campo são válidos, exceto o GUID nulo, que é {00000000-0000-0000-0000-000000000000} .

### <a name="76-stream-extension-directory-entry"></a>7.6 Entrada do diretório de extensão de fluxo

A entrada do diretório Extensão de Fluxo é uma entrada de diretório secundário crítica em Conjuntos de entradas de diretório de arquivos (consulte [Tabela 33](#table-33-stream-extension-directoryentry)). O número válido de entradas de diretório da Extensão de Fluxo em um conjunto de entradas do diretório Arquivo é 1.
Além disso, essa entrada de diretório só será válida se seguir imediatamente a entrada Diretório de arquivos.

<div id="table-33-stream-extension-directoryentry" />

**Tabela 33 Diretório de Extensão de FluxoEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#761-entrytype-field">a Seção 7.6.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#762-generalsecondaryflags-field">a Seção 7.6.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>2</td>
<td>1</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="even">
<td>NameLength</td>
<td>3</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#763-namelength-field">a Seção 7.6.3</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>NameHash</td>
<td>4</td>
<td>2</td>
<td>Esse campo é obrigatório e a <a href="#764-namehash-field">seção 7.6.4</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>6</td>
<td>2</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="odd">
<td>ValidDataLength</td>
<td>8</td>
<td>8</td>
<td>Esse campo é obrigatório e a <a href="#765-validdatalength-field">seção 7.6.5</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>Reserved3</td>
<td>16</td>
<td>4</td>
<td>Esse campo é obrigatório e seu conteúdo é reservado.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#766-firstcluster-field">seção 7.6.6</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Esse campo é obrigatório e a <a href="#767-datalength-field">seção 7.6.7</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>Campo EntryType 7.6.1

O campo EntryType deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1](#641-entrytype-field)).

##### <a name="7611-typecode-field"></a>Campo 7.6.1.1 TypeCode

O campo TypeCode deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.1](#6411-typecode-field)).

Para a entrada de diretório de extensão de fluxo, o valor válido para esse campo é 0.

##### <a name="7612-typeimportance-field"></a>Campo 7.6.1.2 TypeImportance

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.2](#6412-typeimportance-field)).

Para a entrada de diretório de extensão de fluxo, o valor válido para esse campo é 0.

##### <a name="7613-typecategory-field"></a>Campo 7.6.1.3 TypeCategory

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.3](#6413-typecategory-field)).

##### <a name="7614-inuse-field"></a>Campo 7.6.1.4 InUse

O campo InUse deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.4](#6414-inuse-field)).

#### <a name="762-generalsecondaryflags-field"></a>Campo 7.6.2 GeneralSecondaryFlags

O campo GeneralSecondaryFlags deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.2](#642-generalsecondaryflags-field)) e define o conteúdo do campo CustomDefined a ser reservado.

##### <a name="7621-allocationpossible-field"></a>Campo 7.6.2.1 AllocationPossible

O campo AllocationPossible deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.2.1](#6421-allocationpossible-field)).

Para a entrada de diretório de extensão de fluxo, o valor válido para esse campo é 1.

##### <a name="7622-nofatchain-field"></a>Campo 7.6.2.2 NoFatChain

O campo NoFatChain deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.2.2](#6422-nofatchain-field)).

#### <a name="763-namelength-field"></a>Campo 7.6.3 NameLength

O campo NameLength deve conter o comprimento da cadeia de caracteres Unicode nas entradas do diretório de nome de arquivo subsequentes (consulte a [seção 7,7](#77-file-name-directory-entry)) coletivamente.

O intervalo válido de valores para esse campo deve ser:

- Pelo menos 1, que é o nome de arquivo mais curto possível

- No máximo 255, que é o nome de arquivo mais longo possível

O valor do campo NameLength também afeta as entradas de diretório de nome de arquivo de número (consulte a [seção 7,7](#77-file-name-directory-entry)).

#### <a name="764-namehash-field"></a>Campo 7.6.4 NameHash

O campo NameHash deve conter um hash de 2 bytes (consulte a [Figura 4](#figure-4-namehash-computation)) do nome de arquivo mais ativo. Isso permite que as implementações executem uma comparação rápida ao pesquisar um arquivo por nome. O mais importante é que o NameHash fornece uma verificação de uma incompatibilidade. As implementações devem verificar todas as correspondências de NameHash com uma comparação do nome de arquivo mais ativo.

<div id="figure-4-namehash-computation" />

**Figura 4 computação NameHash**

```C
UInt16 NameHash
(
    WCHAR * FileName,    // points to an in-memory copy of the up-cased file name
    UCHAR   NameLength
)
{
    UCHAR  * Buffer = (UCHAR *)FileName;
    UInt16   NumberOfBytes = (UInt16)NameLength * 2;
    UInt16   Hash = 0;
    UInt16   Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        Hash = ((Hash&1) ? 0x8000 : 0) + (Hash>>1) + (UInt16)Buffer[Index];
    }
    return Hash;
}
```

#### <a name="765-validdatalength-field"></a>Campo 7.6.5 ValidDataLength

O campo ValidDataLength deve descrever o quanto nos dados do usuário do fluxo de dados foram gravados. As implementações devem atualizar esse campo à medida que eles gravam os dados mais detalhadamente no fluxo de dados. Na mídia de armazenamento, os dados entre o comprimento de dados válido e o comprimento dos dados do fluxo de dados são indefinidos. As implementações devem retornar zeros para operações de leitura além do comprimento de dados válido.

Se a entrada do diretório de arquivos correspondente descrever um diretório, o único valor válido para esse campo será igual ao valor do campo DATALENGTH. Caso contrário, o intervalo de valores válidos para esse campo deverá ser:

- Pelo menos 0, o que significa que nenhum dado de usuário foi gravado no fluxo de dados

- No máximo, o DATALENGTH, que significa que os dados do usuário foram gravados em todo o tamanho do fluxo de dados

#### <a name="766-firstcluster-field"></a>Campo 7.6.6 FirstCluster

O campo FirstCluster deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.3](#643-firstcluster-field)).

Esse campo deve conter o índice do primeiro cluster do fluxo de dados, que hospeda os dados do usuário.

#### <a name="767-datalength-field"></a>Campo de comprimento de 7.6.7

O campo DATALENGTH deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.4](#644-datalength-field)).

Se a entrada do diretório de arquivos correspondente descrever um diretório, o valor válido para esse campo será o tamanho inteiro da alocação associada, em bytes, que pode ser 0. Além disso, para diretórios, o valor máximo para esse campo é 256 MB.

### <a name="77-file-name-directory-entry"></a>7,7 entrada de diretório de nome de arquivo

As entradas de diretório de nome de arquivo são entradas de diretório secundárias críticas em conjuntos de entrada de diretório de arquivos (consulte a [tabela 34](#table-34-file-name-directoryentry)). O número válido de entradas de diretório de nome de arquivo em um conjunto de entrada de diretório de arquivo é NameLength/15, arredondado para o número inteiro mais próximo. Além disso, as entradas de diretório de nome de arquivo serão válidas somente se eles seguirem imediatamente a entrada de diretório de extensão de fluxo como uma série consecutiva. As entradas de diretório de nome de arquivo são combinadas para formar o nome de arquivo para a entrada de diretório de arquivo definida.

Todos os filhos de uma determinada entrada de diretório devem ter conjuntos de entrada de diretório de nome de arquivo exclusivos. Isso significa que não pode haver nenhum nome de arquivo ou diretório duplicado após o uso de um diretório.

<div id="table-34-file-name-directoryentry" />

**Tabela 34 nome do arquivo DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>minuciosa</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>minuciosa</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e a <a href="#771-entrytype-field">seção 7.7.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e a <a href="#772-generalsecondaryflags-field">seção 7.7.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>Esse campo é obrigatório e a <a href="#773-filename-field">seção 7.7.3</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>Campo EntryType 7.7.1

O campo EntryType deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1](#641-entrytype-field)).

##### <a name="7711-typecode-field"></a>Campo 7.7.1.1 TypeCode

O campo TypeCode deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.1](#6411-typecode-field)).

Para a entrada do diretório Extensão de Fluxo, o valor válido para esse campo é 1.

##### <a name="7712-typeimportance-field"></a>Campo TypeImportance 7.7.1.2

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.1.2](#6412-typeimportance-field)).

Para a entrada do diretório Extensão de Fluxo, o valor válido para esse campo é 0.

##### <a name="7713-typecategory-field"></a>Campo TypeCategory 7.7.1.3

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.1.3](#6413-typecategory-field)).

##### <a name="7714-inuse-field"></a>7.7.1.4 Campo de inutilização

O campo InUse deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.1.4](#6414-inuse-field)).

#### <a name="772-generalsecondaryflags-field"></a>7.7.2 Campo GeneralSecondaryFlags

O campo GeneralSecondaryFlags deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a Seção [6.4.2](#642-generalsecondaryflags-field)) e define o conteúdo do campo CustomDefined a ser reservado.

##### <a name="7721-allocationpossible-field"></a>7.7.2.1 Campo AllocationPossible

O campo AllocationPossible deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.2.1](#6421-allocationpossible-field)).

Para a entrada do diretório Extensão de Fluxo, o valor válido para esse campo é 0.

##### <a name="7722-nofatchain-field"></a>7.7.2.2 Campo NoFatChain

O campo NoFatChain deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.2.2](#6422-nofatchain-field)).

#### <a name="773-filename-field"></a>Campo FileName 7.7.3

O campo FileName deve conter uma cadeia de caracteres Unicode, que é uma parte do nome do arquivo. Na ordem em que as entradas do diretório Nome do Arquivo existem em um conjunto de entradas do diretório Arquivo, os campos FileName concatenam para formar o nome do arquivo para o conjunto de entradas do diretório Arquivo. Considerando o comprimento do campo FileName, 15 caracteres e o número máximo de entradas de diretório nome de arquivo, 17, o comprimento máximo do nome de arquivo final concatenado é
255.

O nome do arquivo concatenado tem o mesmo conjunto de caracteres ilícitos que outros sistemas de arquivos baseados em FAT (consulte [a Tabela 35](#table-35-invalid-filename-characters)). As implementações devem definir os caracteres nãoutilados dos campos FileName com o valor 0000h.

<div id="table-35-invalid-filename-characters" />

**Tabela 35 Caracteres de FileName inválidos**

| **Código de caractere** | **Descrição** | **Código de caractere** | **Descrição**   | **Código de caractere** | **Descrição** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000h              | Código de controle    | 0001h              | Código de controle      | 0002h              | Código de controle    |
| 0003h              | Código de controle    | 0004h              | Código de controle      | 0005h              | Código de controle    |
| 0006h              | Código de controle    | 0007h              | Código de controle      | 0008h              | Código de controle    |
| 0009h              | Código de controle    | 000Ah              | Código de controle      | 000Bh              | Código de controle    |
| 000Ch              | Código de controle    | 000Dh              | Código de controle      | 000Eh              | Código de controle    |
| 000Fh              | Código de controle    | 0010h              | Código de controle      | 0011h              | Código de controle    |
| 0012h              | Código de controle    | 0013h              | Código de controle      | 0014h              | Código de controle    |
| 0015h              | Código de controle    | 0016h              | Código de controle      | 0017h              | Código de controle    |
| 0018h              | Código de controle    | 0019h              | Código de controle      | 001Ah              | Código de controle    |
| 001Bh              | Código de controle    | 001Ch              | Código de controle      | 001Dh              | Código de controle    |
| 001Eh              | Código de controle    | 001Fh              | Código de controle      | 0022h              | Aspas  |
| 002Ah              | Asterisk        | 002Fh              | Barra     | 003Ah              | Dois pontos           |
| 003Ch              | Sinal de menor que  | 003Eh              | Sinal de maior que | 003Fh              | Ponto de interrogação   |
| 005Ch              | Barra ind.      | 007Ch              | Barra vertical      |                    |                 |

Os nomes de arquivo "." e ".." têm o significado especial de "this directory" e "containing directory", respectivamente. As implementações não devem registrar nenhum desses nomes de arquivo reservados no campo FileName.
No entanto, as implementações podem gerar esses dois nomes de arquivo em listagem de diretório para fazer referência ao diretório que está sendo listado e ao diretório que o contém.

As implementações podem querer restringir nomes de arquivo e diretório apenas ao conjunto de caracteres ASCII. Nesse caso, eles devem limitar o uso de caracteres ao intervalo de caracteres válidos nas primeiras 128 entradas Unicode. Eles ainda devem armazenar nomes de arquivo e diretório em Unicode no volume e converter para/de ASCII/Unicode ao intercalar com o usuário.

### <a name="78-vendor-extension-directory-entry"></a>7.8 Entrada de diretório de extensão de fornecedor

A entrada do diretório Extensão de Fornecedor é uma entrada de diretório secundário benigna em Conjuntos de entradas de diretório de arquivos (consulte [Tabela 36](#table-36-vendor-extension-directoryentry)). Um conjunto de entradas do diretório Arquivo pode conter qualquer número de entradas de diretório de Extensão de Fornecedor, até o limite de entradas de diretório secundário, menos o número de outras entradas de diretório secundário. Além disso, as entradas de diretório da Extensão de Fornecedor serão válidas somente se não precederem as entradas de diretório extensão de fluxo e nome de arquivo necessárias.

Entradas de diretório de extensão de fornecedor permitem que os fornecedores tenham entradas de diretório exclusivas específicas do fornecedor em conjuntos de entrada de diretório de arquivo individuais por meio do campo VendorGuid (consulte [a Tabela 36](#table-36-vendor-extension-directoryentry)). Entradas de diretório exclusivas permitem efetivamente que os fornecedores estendam o sistema de arquivos exFAT. Os fornecedores podem definir o conteúdo do campo VendorDefined (consulte [a Tabela 36](#table-36-vendor-extension-directoryentry)). As implementações de fornecedor podem manter o conteúdo do campo VendorDefined e podem fornecer funcionalidade específica do fornecedor.

Implementações que não reconhecem o GUID de uma entrada de diretório de Extensão de Fornecedor devem tratar a entrada de diretório da mesma forma que qualquer outra entrada de diretório secundário benigno não reconhecido (consulte a Seção [8.2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-36-vendor-extension-directoryentry" />

**Diretório de extensão do fornecedor da Tabela 36Entrada**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#781-entrytype-field">a Seção 7.8.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#782-generalsecondaryflags-field">a Seção 7.8.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Esse campo é obrigatório e <a href="#783-vendorguid-field">a Seção 7.8.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>14</td>
<td>Esse campo é obrigatório e os fornecedores podem definir seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>Campo EntryType 7.8.1

O campo EntryType deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte [a Seção 6.4.1](#641-entrytype-field)).

##### <a name="7811-typecode-field"></a>Campo TypeCode 7.8.1.1

O campo TypeCode deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.1.1](#6411-typecode-field)).

Para a entrada do diretório Extensão de Fornecedor, o valor válido para esse campo é 0.

##### <a name="7812-typeimportance-field"></a>Campo TypeImportance 7.8.1.2

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.1.2](#6412-typeimportance-field)).

Para a entrada do diretório Extensão de Fornecedor, o valor válido para esse campo é 1.

##### <a name="7813-typecategory-field"></a>Campo TypeCategory 7.8.1.3

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.1.3](#6413-typecategory-field)).

##### <a name="7814-inuse-field"></a>7.8.1.4 Campo de inutilização

O campo InUse deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.1.4](#6414-inuse-field)).

#### <a name="782-generalsecondaryflags-field"></a>7.8.2 Campo GeneralSecondaryFlags

O campo GeneralSecondaryFlags deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Genérico (consulte a Seção [6.4.2](#642-generalsecondaryflags-field)) e define o conteúdo do campo CustomDefined a ser reservado.

##### <a name="7821-allocationpossible-field"></a>7.8.2.1 Campo AllocationPossible

O campo AllocationPossible deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.2.1](#6421-allocationpossible-field)).

Para a entrada do diretório Extensão de Fornecedor, o valor válido para esse campo é 0.

##### <a name="7822-nofatchain-field"></a>7.8.2.2 Campo NoFatChain

O campo NoFatChain deve estar em conformidade com a definição fornecida no modelo DirectoryEntry Secundário Genérico (consulte a [Seção 6.4.2.2](#6422-nofatchain-field)).

#### <a name="783-vendorguid-field"></a>7.8.3 Campo VendorGuid

O campo VendorGuid deve conter um GUID que identifica exclusivamente a extensão de fornecedor determinada.

Todos os valores possíveis para esse campo são válidos, exceto o GUID nulo, que é {00000000-0000-0000-0000-000000000000} . No entanto, os fornecedores devem usar uma ferramenta de geração de GUID, como GuidGen.exe, para selecionar um GUID ao definir suas extensões.

O valor desse campo determina a estrutura específica do fornecedor do campo VendorDefined.

### <a name="79-vendor-allocation-directory-entry"></a>7.9 Entrada de diretório de alocação de fornecedor

A entrada do diretório Alocação de Fornecedor é uma entrada de diretório secundário benigna em Conjuntos de entradas de diretório de arquivos (consulte [Tabela 37](#table-37-vendor-allocation-directoryentry)). Um conjunto de entradas do diretório Arquivo pode conter qualquer número de entradas de diretório alocação de fornecedor, até o limite de entradas de diretório secundário, menos o número de outras entradas de diretório secundário. Além disso, as entradas de diretório alocação de fornecedor serão válidas somente se não precedem as entradas de diretório Extensão de Fluxo e Nome de Arquivo necessárias.

Entradas de diretório de alocação de fornecedor permitem que os fornecedores tenham entradas de diretório exclusivas específicas do fornecedor em conjuntos de entrada de diretório de arquivo individuais por meio do campo VendorGuid (consulte [Tabela 37](#table-37-vendor-allocation-directoryentry)). Entradas de diretório exclusivas permitem efetivamente que os fornecedores estendam o sistema de arquivos exFAT. Os fornecedores podem definir o conteúdo dos clusters associados, se existirem. As implementações de fornecedor podem manter o conteúdo dos clusters associados, se algum, e podem fornecer funcionalidade específica do fornecedor.

Implementações que não reconhecem o GUID de uma entrada de diretório alocação de fornecedor devem tratar a entrada de diretório da mesma forma que qualquer outra entrada de diretório secundário benigno não reconhecido (consulte a Seção [8.2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-37-vendor-allocation-directoryentry" />

**Tabela 37 Diretório de Alocação de FornecedorEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#791-entrytype-field">a Seção 7.9.1</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Esse campo é obrigatório e <a href="#792-generalsecondaryflags-field">a Seção 7.9.2</a> define seu conteúdo.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Esse campo é obrigatório e <a href="#793-vendorguid-field">a Seção 7.9.3</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>2</td>
<td>Esse campo é obrigatório e os fornecedores podem definir seu conteúdo.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Esse campo é obrigatório e a <a href="#794-firstcluster-field">seção 7.9.4</a> define seu conteúdo.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Esse campo é obrigatório e a <a href="#795-datalength-field">seção 7.9.5</a> define seu conteúdo.</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>Campo EntryType 7.9.1

O campo EntryType deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1](#641-entrytype-field)).

##### <a name="7911-typecode-field"></a>Campo 7.9.1.1 TypeCode

O campo TypeCode deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.1](#6411-typecode-field)).

Para a entrada do diretório de alocação do fornecedor, o valor válido para esse campo é 1.

##### <a name="7912-typeimportance-field"></a>Campo 7.9.1.2 TypeImportance

O campo TypeImportance deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.2](#6412-typeimportance-field)).

Para a entrada do diretório de alocação do fornecedor, o valor válido para esse campo é 1.

##### <a name="7913-typecategory-field"></a>Campo 7.9.1.3 TypeCategory

O campo TypeCategory deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.3](#6413-typecategory-field)).

##### <a name="7914-inuse-field"></a>Campo 7.9.1.4 InUse

O campo InUse deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.1.4](#6414-inuse-field)).

#### <a name="792-generalsecondaryflags-field"></a>Campo 7.9.2 GeneralSecondaryFlags

O campo GeneralSecondaryFlags deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.2](#642-generalsecondaryflags-field)) e define o conteúdo do campo CustomDefined a ser reservado.

##### <a name="7921-allocationpossible-field"></a>Campo 7.9.2.1 AllocationPossible

O campo AllocationPossible deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.2.1](#6421-allocationpossible-field)).

Para a entrada do diretório de alocação do fornecedor, o valor válido para esse campo é 1.

##### <a name="7922-nofatchain-field"></a>Campo 7.9.2.2 NoFatChain

O campo NoFatChain deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.2.2](#6422-nofatchain-field)).

#### <a name="793-vendorguid-field"></a>Campo 7.9.3 VendorGuid

O campo VendorGuid deve conter um GUID que identifica exclusivamente a alocação de fornecedor determinada.

Todos os valores possíveis para esse campo são válidos, exceto o GUID NULL, que é {00000000-0000-0000-0000-000000000000} . No entanto, os fornecedores devem usar uma ferramenta de geração de GUID, como GuidGen.exe, para selecionar um GUID ao definir suas extensões.

O valor desse campo determina a estrutura específica do fornecedor do conteúdo dos clusters associados, se existir.

#### <a name="794-firstcluster-field"></a>Campo 7.9.4 FirstCluster

O campo FirstCluster deve estar em conformidade com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.3](#643-firstcluster-field)).

#### <a name="795-datalength-field"></a>Campo de comprimento de 7.9.5

O campo DATALENGTH deve estar de acordo com a definição fornecida no modelo DirectoryEntry secundário genérico (consulte a [seção 6.4.4](#644-datalength-field)).

### <a name="710-texfat-padding-directory-entry"></a>7,10 entrada de diretório de preenchimento de TexFAT

Essa especificação, a especificação básica do sistema de arquivos do exFAT revisão 1, 0, não define a entrada do diretório de preenchimento TexFAT. No entanto, seu código de tipo é 1 e sua importância de tipo é 1. As implementações dessa especificação devem tratar as entradas do diretório de preenchimento TexFAT da mesma forma que qualquer outra entrada de diretório primário benigno não reconhecida, as implementações não moverão as entradas do diretório de preenchimento TexFAT.

## <a name="8-implementation-notes"></a>8 notas de implementação

### <a name="81-recommended-write-ordering"></a>8,1 ordem de gravação recomendada

As implementações devem garantir que o volume seja tão resiliente quanto possível para falhas de energia e outras falhas inevitáveis. Ao criar novas entradas de diretório ou modificar as alocações de cluster, as implementações geralmente devem seguir esta ordem de escrita:

1. Defina o valor do campo VolumeDirty como 1

2. Atualizar o FAT ativo, se necessário

3. Atualizar o bitmap de alocação ativa

4. Criar ou atualizar a entrada de diretório, se necessário

5. Limpe o valor do campo VolumeDirty para 0, se seu valor antes da primeira etapa for 0

Ao excluir entradas de diretório ou liberar alocações de cluster, as implementações devem seguir esta ordem de escrita:

1. Defina o valor do campo VolumeDirty como 1

2. Exclua ou atualize a entrada de diretório, se necessário

3. Atualizar o FAT ativo, se necessário

4. Atualizar o bitmap de alocação ativa

5. Limpe o valor do campo VolumeDirty para 0, se seu valor antes da primeira etapa for 0

### <a name="82-implications-of-unrecognized-directory-entries"></a>8,2 implicações de entradas de diretório não reconhecidas

As especificações de exFAT futuras do mesmo número de revisão principal, 1 e número de revisão secundária maior que 0, podem definir novas entradas de diretório primário benigno, secundário crítico e secundário benigno. Somente as especificações exFAT de um número maior de revisão principal podem definir novas entradas de diretório primário crítico. Implementações dessa especificação, a especificação do sistema de arquivos 1, 0 do exFAT, deve ser capaz de montar e acessar qualquer volume exFAT de número 1 de revisão principal e qualquer número de revisão menor. Isso apresenta cenários nos quais uma implementação pode encontrar entradas de diretório que não são reconhecidas. Os seguintes descrevem as implicações desses cenários:

1. A presença de entradas de diretório primário crítico não reconhecidas no diretório raiz renderiza o volume inválido. A presença de qualquer entrada de diretório primário crítico, exceto as entradas de diretório de arquivo, em qualquer diretório não raiz, renderiza o diretório de hospedagem inválido.

2. As implementações não devem modificar entradas de diretório primário benignos não reconhecidas ou suas alocações de cluster associadas. No entanto, ao excluir um diretório e somente ao excluir um diretório, as implementações devem excluir entradas de diretório primário benignos não reconhecidas e liberar todas as alocações de cluster associadas, se houver.

3. As implementações não devem modificar entradas de diretório secundária críticas não reconhecidas ou suas alocações de cluster associadas. A presença de uma ou mais entradas de diretório secundária crítico não reconhecidas em um conjunto de entradas de diretório renderiza o conjunto de entradas de diretório inteiro não reconhecido. Ao excluir um conjunto de entrada de diretório que contém uma ou mais entradas de diretório secundário críticas não reconhecidas, as implementações deverão liberar todas as alocações de cluster, se houver, associadas a entradas de diretório secundárias críticas não reconhecidas.
   Além disso, se o conjunto de entradas de diretório descrever um diretório, as implementações poderão:

   - Percorrer o diretório

   - Enumerar as entradas de diretório que ele contém

   - Excluir entradas de diretório contidas

   - Mover entradas de diretório contidas para um diretório diferente

   No entanto, as implementações não devem:

   - Modificar entradas de diretório contidas, exceto Delete, conforme observado

   - Criar novas entradas de diretório contidas

   - Abrir entradas de diretório contidas, exceto atravessar e enumerar, conforme observado

4. As implementações não devem modificar entradas de diretório secundário benignos não reconhecidas ou suas alocações de cluster associadas.
   As implementações devem ignorar entradas de diretório secundário benignos não reconhecidas. Ao excluir uma entrada de diretório definida, as implementações deverão liberar todas as alocações de cluster, se houver, associadas a entradas de diretório secundário benignos não reconhecidas.

## <a name="9-file-system-limits"></a>9 limites do sistema de arquivos

### <a name="91-sector-size-limits"></a>Limites de tamanho de setor de 9,1

O campo BytesPerSectorShift define os limites de tamanho de setor inferior e superior (que é avaliado como **limite inferior: 512 bytes; limite superior: 4.096 bytes**).

### <a name="92-cluster-size-limits"></a>9,2 limites de tamanho de cluster

O campo SectorsPerClusterShift define os limites de tamanho de cluster inferior e superior (**limite inferior: 1 setor; limite superior: 25--setores BytesPerSectorShift**, que são avaliados como 32MB).

### <a name="93-cluster-heap-size-limits"></a>9,3 limites de tamanho de heap de cluster

O heap de cluster deve conter, pelo menos, espaço suficiente para hospedar as seguintes estruturas básicas do sistema de arquivos: o diretório raiz, todos os bitmaps de alocação e a tabela de maiúsculas e minúsculas.

O limite de tamanho de heap de cluster inferior é uma função do limite de tamanho inferior de cada uma das estruturas básicas do sistema de arquivos que residem no heap de cluster. Até mesmo dado o menor cluster possível (512 bytes), cada uma das estruturas básicas do sistema de arquivos não precisa de mais de um cluster. Portanto, o **limite inferior é: 2 + clusters NumberOfFats**, que é avaliado como 3 ou 4 clusters, dependendo do valor do campo NumberOfFats.

O limite de tamanho de heap de cluster superior é uma função simples do número máximo possível de clusters, que o campo ClusterCount define (**limite superior: 2 <sup>32</sup>-11 clusters**). Independentemente do tamanho do cluster, tal heap de cluster tem espaço suficiente para, pelo menos, hospedar as estruturas básicas do sistema de arquivos.

### <a name="94-volume-size-limits"></a>9,4 limites de tamanho do volume

O campo VolumeLength define os limites de tamanho de volume inferior e superior (limite inferior: **2 <sup>20</sup>/2 setores <sup>BytesPerSectorShift</sup>**, que são avaliados como 1mb; **limite superior: 2 <sup>64</sup>-1 setores**, que, considerando o maior tamanho de setor possível, é avaliado como aproximadamente 64ZB). No entanto, essa especificação recomenda não mais do que 2 clusters<sup>24</sup>-2 no heap de cluster (consulte a [seção 3.1.9](#319-clustercount-field)). Portanto, o limite superior recomendado de um volume é: ClusterHeapOffset + (2<sup>24</sup>-2) \* 2<sup>SectorsPerClusterShift</sup>. Considerando o maior tamanho de cluster possível, 32 MB, e supondo que ClusterHeapOffset seja de 96 MB (espaço suficiente para as regiões Principal e Inicialização de Backup e apenas a Primeira FAT), o limite superior recomendado de um volume é avaliada como aproximadamente 512 TB.

### <a name="95-directory-size-limits"></a>9.5 Limites de tamanho do diretório

O campo DataLength da entrada do diretório extensão de fluxo define os limites de tamanho de diretório inferior e superior ( limite **inferior: 0 bytes; limite superior: 256 MB**). Isso significa que um diretório pode hospedar até 8.388.608 entradas de diretório (cada entrada de diretório consome 32 bytes). Considerando o menor conjunto de entrada do diretório arquivo possível, três entradas de diretório, um diretório pode hospedar até 2.796.202 arquivos.

## <a name="10-appendix"></a>Apêndice 10

### <a name="101-globally-unique-identifiers-guids"></a>10.1 GUIDs (Identificadores Globalmente Exclusivos)

Um GUID é a implementação da Microsoft de um identificador universal exclusivo. Um GUID é um valor de 128 bits que consiste em um grupo de oito dígitos hexadecimais, seguido por três grupos de quatro dígitos hexadecimais cada e seguido por um grupo de 12 dígitos hexadecimais, por exemplo {6B29FC40-CA47-1067-B31D-00DD010662DA}, (consulte [a Tabela 38](#table-38-guid-structure)).

<div id="table-38-guid-structure" />

**Estrutura GUID da Tabela 38**

<table>
<thead>
<tr class="header">
<th><strong>Nome do Campo</strong></th>
<th><p><strong>Deslocamento</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamanho</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentários</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Data1</td>
<td>0</td>
<td>4</td>
<td>Esse campo é obrigatório e contém os quatro bytes do primeiro grupo do GUID (6B29FC40h do exemplo).</td>
</tr>
<tr class="even">
<td>Data2</td>
<td>4</td>
<td>2</td>
<td>Esse campo é obrigatório e contém os dois bytes do segundo grupo do GUID (CA47h do exemplo).</td>
</tr>
<tr class="odd">
<td>Data3</td>
<td>6</td>
<td>2</td>
<td>Esse campo é obrigatório e contém os dois bytes do terceiro grupo do GUID (1067h do exemplo).</td>
</tr>
<tr class="even">
<td>Data4[0]</td>
<td>8</td>
<td>1</td>
<td>Esse campo é obrigatório e contém o byte mais significativo do quarto grupo do GUID (B3h do exemplo).</td>
</tr>
<tr class="odd">
<td>Data4[1]</td>
<td>9</td>
<td>1</td>
<td>Esse campo é obrigatório e contém o byte menos significativo do quarto grupo do GUID (1Dh do exemplo).</td>
</tr>
<tr class="even">
<td>Data4[2]</td>
<td>10</td>
<td>1</td>
<td>Esse campo é obrigatório e contém o primeiro byte do quinto grupo do GUID (00h do exemplo).</td>
</tr>
<tr class="odd">
<td>Data4[3]</td>
<td>11</td>
<td>1</td>
<td>Esse campo é obrigatório e contém o segundo byte do quinto grupo do GUID (DDh do exemplo).</td>
</tr>
<tr class="even">
<td>Data4[4]</td>
<td>12</td>
<td>1</td>
<td>Esse campo é obrigatório e contém o terceiro byte do quinto grupo do GUID (01h do exemplo).</td>
</tr>
<tr class="odd">
<td>Data4[5]</td>
<td>13</td>
<td>1</td>
<td>Esse campo é obrigatório e contém o quarto byte do quinto grupo do GUID (06h do exemplo).</td>
</tr>
<tr class="even">
<td>Data4[6]</td>
<td>14</td>
<td>1</td>
<td>Esse campo é obrigatório e contém o quinto byte do quinto grupo do GUID (62h do exemplo).</td>
</tr>
<tr class="odd">
<td>Data4[7]</td>
<td>15</td>
<td>1</td>
<td>Esse campo é obrigatório e contém o sexto byte do quinto grupo do GUID (DAh do exemplo).</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10.2 Tabelas de partição

Para garantir a interoperabilidade de volumes exFAT em um amplo conjunto de cenários de uso, as implementações devem usar o tipo de partição 07h para o armazenamento particionado MBR e o GUID de partição {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7} para armazenamento particionado por GPT.

## <a name="11-documentation-change-history"></a>11 Histórico de alterações de documentação

A Tabela 39 descreve o histórico de versões de, correções para, adições, remoções e esclarecimentos deste documento.

<div id="table-39-documentation-change-history" />

**Histórico de alterações da documentação da Tabela 39**

<table>
<thead>
<tr class="header">
<th><strong>Data</strong></th>
<th><strong>Descrição da alteração</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>08 de janeiro de 2008</td>
<td><p>Primeira versão da Especificação Básica, que inclui:</p>
<blockquote>
<p>Seção 1, Introdução</p>
<p>Seção 2,<br />
Estrutura de volume</p>
<p>Seção 3, Regiões de inicialização principal e de backup</p>
<p>Seção 4, Região da Tabela de Alocação de Arquivos</p>
<p>Seção 5, Região de Dados</p>
<p>Seção 6, Estrutura de Diretórios</p>
<p>Seção 7, Definições de entrada de diretório</p>
<p>Seção 8, Notas de Implementação</p>
<p>Seção 9, Limites do Sistema de Arquivos</p>
<p>Seção 10, Apêndice</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08 de junho de 2008</td>
<td><p>Segunda versão da Especificação Básica, que inclui as seguintes alterações:</p>
<blockquote>
<p>Adição da Seção 11,<br />
Histórico de alterações de documentação</p>
<p>Adição das entradas de diretório de alocação de fornecedor e extensão de fornecedor nas seções 7.8 e 7.9</p>
<p>Adição da tabela de caso up-case recomendada nas Seções 7.2.5 e 7.2.5.1</p>
<p>Adição dos campos UtcOffset na Seção 7.4 e adição do acrônimo UTC na Seção 1.3</p>
<p>Correção do tamanho do campo CustomDefined na Tabela 19</p>
<p>Correção do intervalo válido de valores NameLength na Seção 7.6.3</p>
<p>Correção e esclarecimento dos campos Timestamp e 10msIncrement na Seção 7.4</p>
<p>Esclarecimento da estrutura de parâmetros nulos na Seção 3.3</p>
<p>Esclarecimento do significado dos valores do campo NoFatChain na Seção 6.3.4.2</p>
<p>Esclarecimento do significado dos valores do campo DataLength na Seção 6.2.3</p>
<p>Esclarecimento do campo VolumeDirty na Seção 3.1.13.2 e a ordenação de gravação recomendada na Seção 8.1</p>
<p>Esclarecimento do campo MediaFailure na Seção 3.1.13.3</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01 de outubro de 2008</td>
<td><p>Terceira versão da Especificação Básica, que inclui as seguintes alterações:</p>
<blockquote>
<p>Adição de SHALL, SHOULD e MAY a explicações de campo</p>
<p>Adição de definição UTC na Tabela 2 Seção 1.3</p>
<p>Seções modificadas 1.5, para garantir o alinhamento com o documento de especificação do TexFAT.</p>
<p>Esclareceu a restrição de que somente a Microsoft pode definir o layout das entradas de diretório na seção 6,2</p>
<p>Foi adicionado esclarecimento de que o campo FirstCluster deverá ser zero se o DATALENGTH for zero e NoFatChain estiver definido para a seção 6.3.5 e a seção 6.4.3</p>
<p>Requisitos esclarecidos para entradas de diretório de arquivo válidas na seção 7,4</p>
<p>Requisito adicionado para nomes de arquivo e diretório exclusivos à seção 7,7</p>
<p>A observação de implementação foi adicionada para ASCII no final da seção 7.7.3</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01 de janeiro de 2009</td>
<td><p>A quarta versão da especificação básica, que inclui as seguintes alterações:</p>
<blockquote>
<p>Referências removidas a entradas de controle de acesso Windows CE</p>
<p>Foram adicionados esclarecimentos à seção 7.2.5.1 para exigir explicitamente uma tabela completa de casos</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02 de setembro de 2009</td>
<td><p>A quinta versão da especificação básica, que inclui as seguintes alterações:</p>
<blockquote>
<p>Alterações de formatação de documento para permitir uma melhor conversão em PDF</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24 de fevereiro de 2010</td>
<td><p>Sexta versão da especificação básica, que inclui as seguintes alterações:</p>
<blockquote>
<p>Declaração incorreta corrigida: "o campo FirstCluster deverá ser zero se o DATALENGTH for zero e NoFatChain for definido" na seção 6.3.5 e na seção 6.4.3 para "se o bit NoFatChain for 1 e FirstCluster deve apontar para um cluster válido no heap de cluster" para esclarecer que deve haver uma alocação válida se o bit NoFatChain for definido.</p>
<p>Adicionado "se o bit NoFatChain for 1, o DATALENGTH não deverá ser zero. Se o campo FirstCluster for zero, DATALENGTH também deverá ser zero "para a seção 6.3.6 e a seção 6.4.4 para esclarecer que deve haver uma alocação válida se o bit NoFatChain estiver definido.</p>
<p>Aviso de direitos autorais atualizado para 2010</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26 de agosto de 2019</td>
<td><p>Sétima versão da especificação básica, que inclui as seguintes alterações:</p>
<blockquote>
<p>Termos legais atualizados referentes à especificação, incluindo:</p>
<p>Remoção do aviso confidencial da Microsoft</p>
<p>Remoção da seção contrato de licença de documentação técnica da Microsoft Corporation</p>
<p>Aviso de direitos autorais atualizado para 2019</p>
</blockquote></td>
</tr>
</tbody>
</table>
