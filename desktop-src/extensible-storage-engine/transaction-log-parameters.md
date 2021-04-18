---
description: 'Saiba mais sobre: parâmetros do log de transações'
title: Parâmetros de Log de Transação
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781518"
---
# <a name="transaction-log-parameters"></a>Parâmetros de Log de Transação


_**Aplica-se a:** Windows | Windows Server_

**Neste artigo**  
Parâmetros de Log de Transação  
Requisitos  
Consulte Também  

## <a name="transaction-log-parameters"></a>Parâmetros de Log de Transação

Este tópico contém parâmetros que são usados para logs de transações.

*JET_paramBaseName*  
3  

Esse parâmetro define o prefixo de três letras usado para muitos dos arquivos usados pelo mecanismo de banco de dados. Por exemplo, o arquivo de ponto de verificação é chamado de EDB. CHK por padrão, porque o EDB é o nome de base padrão. O nome base pode ser usado para distinguir facilmente entre conjuntos de arquivos que pertencem a diferentes instâncias ou a aplicativos diferentes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>&quot;EDB&quot;</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>3 caracteres</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramCircularLog*  
17  

Esse parâmetro configura como os arquivos de log de transações são gerenciados pelo mecanismo de banco de dados.

Quando o log circular está desativado, todos os arquivos de log de transações gerados são mantidos no disco até que não sejam mais necessários porque um backup completo do banco de dados foi executado. Nesse modo, é possível restaurar de um backup mais antigo e reproduzir todos os arquivos de log de transações retidos, de modo que nenhum dado seja perdido como resultado do desastre que forçou a restauração. Backups completos regulares são necessários para impedir que o disco fique cheio de arquivos de log de transações.

Quando o log circular está ativado, somente os arquivos de log de transações mais jovens do que o ponto de verificação atual são mantidos no disco. O benefício desse modo é que os backups não são necessários para desativar arquivos de log de transação antigos. A desvantagem é que uma restauração sem perda de dados não é mais possível.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramCommitDefault*  
16  

Esse parâmetro controla a ação padrão tomada quando a transação mais externa é confirmada em uma sessão. Qualquer opção válida que possa ser passada para [JetCommitTransaction](./jetcommittransaction-function.md) também pode ser feita como o padrão para todas as sessões em uma instância e/ou para uma sessão específica. Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obter mais detalhes sobre essas opções.

Esse parâmetro tem um impacto na confiabilidade e no desempenho das transações. Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obter mais detalhes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>JET_GRBIT (inteiro)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Uma opção válida para JetCommitTransaction</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância ou sessão</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOldLogs*  
48  

Quando esse parâmetro for true e os arquivos de log de transações apontados pelo caminho do arquivo de log (**JET_paramLogFilePath**) forem de uma versão obsoleta, esses arquivos de log de transações serão excluídos automaticamente.

**Windows 2000:**  Deve-se ter cuidado com o uso desse parâmetro ao atualizar um banco de dados do Windows NT para o Windows 2000. Se o banco de dados não estiver em um estado consistente e os arquivos de log antigos forem excluídos, o conteúdo do banco de dados será perdido.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p><strong>Windows 2000:</strong>  For</p>
<p><strong>Windows XP:</strong>  True</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramIgnoreLogVersion*  
47  

Se esse parâmetro for true, o mecanismo de banco de dados não validará o número de versão do arquivo de log de transações durante [JetInit](./jetinit-function.md).

**Windows XP:**  A partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

Esse parâmetro fornece compatibilidade com versões anteriores do mecanismo de banco de dados para as convenções de nomenclatura do arquivo.

Atualmente, há suporte para as seguintes opções:

JET_bitESE98FileNames

Quando essa opção estiver presente, o mecanismo de banco de dados usará as seguintes convenções de nomenclatura para seus arquivos:

  - Os arquivos de log de transações usarão. LOG para sua extensão de arquivo

  - Os arquivos de ponto de verificação usarão. CHK para sua extensão de arquivo

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>JET_GRBIT (inteiro)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0, JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows Vista e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramLogBuffers*  
12  

Esse parâmetro irá configurar a quantidade de memória usada para armazenar em cache os registros de log antes que eles sejam gravados no arquivo de log de transações. A unidade para esse parâmetro é o tamanho do setor do volume que contém os arquivos de log de transações. O tamanho do setor quase sempre é de 512 bytes, portanto, é seguro assumir esse tamanho para a unidade.

Esse parâmetro tem um impacto no desempenho. Quando o mecanismo de banco de dados está sob carga de atualização pesada, esse buffer pode se tornar completo com muita rapidez. Um tamanho de cache maior para o arquivo de log de transações é essencial para um bom desempenho de atualização sob uma condição de alta carga. O padrão é conhecido como muito pequeno para esse caso.

**Windows XP e windows 2000:**  No Windows XP e versões anteriores, não é recomendável definir esse parâmetro como um número de buffers maior (em bytes) que metade do tamanho de um arquivo de log de transações.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  80</p>
<p><strong>Windows Vista:</strong>  126</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  80 – 2147483647</p>
<p><strong>Windows Vista:</strong>  1 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramLogCheckpointPeriod*  
14  

Esse parâmetro configura o mecanismo de banco de dados para pegar um ponto de verificação quando o número especificado de setores do arquivo de log tiver sido gerado.

**Windows XP:**  A partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFileCreateAsynch*  
69  

Quando esse parâmetro for definido como true, o mecanismo de banco de dados criará o próximo arquivo de log de transações, pois o arquivo de log de transações atual será consumido. A intenção é minimizar o tempo gasto alternando de um arquivo de log de transações para o próximo em uma carga de atualização pesada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>True</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFilePath*  
2 

Esse parâmetro indica o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá os logs de transação para a instância. O caminho deve ser terminado com um caractere de barra invertida, que indica que o caminho de destino é uma pasta. Os arquivos de log de transações contêm as informações necessárias para colocar os arquivos de banco de dados em um estado consistente após uma falha. Normalmente, eles são chamados de EDB \* . Façam. O conteúdo dos arquivos de log de transações é tão importante (se não mais) do que os próprios arquivos de banco de dados. Todo esforço deve ser feito para protegê-los.

Também haverá arquivos de log de reserva adicionais chamados RES1. LOG e RES2. LOG armazenado junto com os arquivos de log comuns. O conteúdo desses arquivos não é importante, pois sua única finalidade é reservar espaço em disco para permitir que o mecanismo seja desligado normalmente em um cenário de disco baixo. Eles também serão um arquivo de log temporário normalmente chamado de EDBTMP. Faça logon nessa mesma pasta. O conteúdo desse arquivo também não é importante. Este arquivo é um novo arquivo de log que está sendo preparado para uso.

As propriedades do volume do host dos arquivos de log de transações e seu posicionamento em relação aos outros arquivos usados pelo mecanismo de banco de dados podem afetar drasticamente o desempenho.

**Observação**  Se um caminho relativo for especificado, ele será relativo ao diretório de trabalho atual do processo que hospeda o aplicativo que está usando o mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>&quot;.\& vincular</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Caminho da pasta (cadeia de caracteres)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 246 caracteres</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFileSize*  
11  

Esse parâmetro irá configurar o tamanho dos arquivos de log de transações. Cada arquivo de log de transações é um tamanho fixo. O tamanho é igual à configuração desse parâmetro de sistema em unidades de 1024 bytes.

Esse parâmetro tem um impacto na confiabilidade. Se a configuração for muito pequena, o número máximo de arquivos de log (1048575) será alcançado muito mais rapidamente. Quando isso acontece, a instância deve ser desligada corretamente, os arquivos de log existentes devem ser excluídos e a instância deve ser reiniciada. Essa ação não apenas reduzirá a disponibilidade do aplicativo, mas também invalidará quaisquer backups anteriores do banco de dados do aplicativo.

Esse parâmetro tem um impacto no desempenho. Se a configuração for muito grande, o [JetInit](./jetinit-function.md) será lento, pois o mecanismo de banco de dados deve ler o arquivo de log mais recente (no mínimo) quando ele for inicializado. Se a configuração for muito grande, ela também levará mais tempo para alternar entre os arquivos de log. Se a configuração for muito pequena, mais arquivos de log precisarão ser criados para um determinado número de atualizações que adicionarão mais sobrecarga.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>5120</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  128 – 32768</p>
<p><strong>Windows Vista:</strong>  64 – 32768</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramLogWaitingUserMax*  
15  

Esse parâmetro tenta otimizar a liberação do buffer de log causado por uma confirmação durável aguardando que um número especificado de sessões aguarde uma confirmação durável antes de forçar uma liberação a ocorrer na esperança de que outra transação compartilhará a liberação.

**Windows XP:**  A partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramRecovery*  
34  

Esse parâmetro é a opção mestra que controla a recuperação de falha de uma instância. Se esse parâmetro for definido como "on", a recuperação de estilo ARIES será usada para colocar todos os bancos de dados na instância em um estado consistente no caso de uma falha de processo ou máquina. Se esse parâmetro for definido como "off", todos os bancos de dados na instância serão gerenciados sem o benefício da recuperação de falhas. Isso significa que, se a instância não for desligada corretamente usando [JetTerm](./jetterm-function.md) antes da saída do processo ou do desligamento do computador, o conteúdo de todos os bancos de dados nessa instância será corrompido.

A desabilitação da recuperação é útil em circunstâncias especiais, em que é conhecido que o conteúdo de um banco de dados não seja útil no caso de uma falha. A recuperação deve ser habilitada para todos os outros casos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>&quot;Em&quot;</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 259 caracteres</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramSystemPath*  
0  

Esse parâmetro indica o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá o arquivo de ponto de verificação para a instância. O caminho deve ser terminado com um caractere de barra invertida, que indica que o caminho de destino é uma pasta. O arquivo de ponto de verificação é um arquivo simples mantido por instância que lembra o arquivo de log de transações mais antigo que deve ser reproduzido para colocar todos os bancos de dados nessa instância em um estado consistente após uma falha. O arquivo de ponto de verificação normalmente é chamado de EDB. CHK.

**Observação**  Se um caminho relativo for especificado, ele será relativo ao diretório de trabalho atual do processo que hospeda o aplicativo que está usando o mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>&quot;.\& vincular</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Caminho da pasta (cadeia de caracteres)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 246 caracteres</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramWaitLogFlush*  
13 

Esse parâmetro tenta otimizar a liberação do buffer de log causado por uma confirmação durável aguardando um período de tempo especificado antes de forçar uma liberação a ocorrer na esperança de que outra transação compartilhará a liberação.

**Windows XP:**  A partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância ou sessão</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

Esse parâmetro é usado para especificar os recursos de compatibilidade de nomenclatura de arquivo a serem mantidos com o esquema de nomenclatura do arquivo do Windows Server 2003 e anterior. Para obter mais informações sobre os diferentes arquivos e sua nomenclatura, consulte [arquivos do mecanismo de armazenamento extensível](./extensible-storage-engine-files.md).

O JET_bitESE98FileNames garante que a extensão de arquivo usada nos arquivos de log de transações e o arquivo de ponto de verificação sejam os mesmos usados no Windows Server 2003. Observação: se estiver atualizando do Windows Server 2003, esse bit ainda não precisará ser especificado, pois o mecanismo atualizará automaticamente as extensões de arquivo se JET_paramCircularLog for definido como **true** ou manter a extensão de log mais antiga se JET_paramCircularLog for **false**.

**Observação**  Para definir um bit, o valor deve primeiro ser recuperado e, em seguida, "ou" no bit de compatibilidade desejado.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>JET_GRBIT (inteiro)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Começando com o Windows Server 2008 e o Windows Vista</p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte Também

[Arquivos do mecanismo de armazenamento extensível](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)
