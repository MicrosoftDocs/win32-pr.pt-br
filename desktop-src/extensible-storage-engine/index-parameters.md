---
description: 'Saiba mais sobre: parâmetros de índice'
title: Parâmetros de Índice
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011780"
---
# <a name="index-parameters"></a>Parâmetros de Índice


_**Aplica-se a:** Windows | Windows Server_

## <a name="index-parameters"></a>Parâmetros de Índice

Este tópico contém parâmetros que são usados para o índice.

*JET_paramIndexTupleIncrement*  
132  

Esse parâmetro especifica o padrão para o incremento de deslocamento usado para percorrer o valor da coluna de origem ao gerar cada tupla. Para obter mais informações, consulte a estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 - 32767</p></td>
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


*JET_paramIndexTupleStart*  
133  

Esse parâmetro especifica o padrão para o deslocamento no valor da coluna de origem no qual a geração de tupla será iniciada. Para obter mais informações, consulte a estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

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
<td><p>0 - 32767</p></td>
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


*JET_paramIndexTuplesLengthMax*  
111  

Esse parâmetro especifica o padrão para o comprimento máximo de tupla em um índice de tupla. Para obter mais informações, consulte a estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  Antes do Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão. Para o Windows Vista, não há mais suporte para isso.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>  0, 2-255</p>
<p><strong>Windows Vista:</strong>  2-255</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMin*  
110  

Esse parâmetro especifica o padrão para o comprimento mínimo de tupla em um índice de tupla. Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obter mais informações.

**Windows Vista:**  Antes do Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão. Para o Windows Vista, não há mais suporte para isso.

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
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>  0, 2-255</p>
<p><strong>Windows Vista:</strong>  2-255</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesToIndexMax*  
112  

Esse parâmetro especifica o padrão para o comprimento máximo de uma cadeia de caracteres de origem a ser dividida em tuplas para um índice de tupla. Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obter mais informações.

**Windows Vista:**  Antes do Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão. Para o Windows Vista, não há mais suporte para isso.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>32767</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 – 32767</p>
<p><strong>Windows Vista:</strong>  1 a 32767</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramUnicodeIndexDefault*  
72  

Esse parâmetro controla os parâmetros Unicode padrão usados por qualquer índice em uma coluna de chave Unicode. O tipo desse parâmetro é [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e, na verdade, é passado usando um ponteiro de buffer armazenado no parâmetro Integer de [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md). O tamanho do buffer deve ser igual ao tamanho de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e deve ser passado para [JetGetSystemParameter](./jetgetsystemparameter-function.md) usando o parâmetro de tamanho do buffer de cadeia de caracteres. Isso é claramente inconsistente, mas esse é o comportamento desse parâmetro.

O valor padrão desse parâmetro contém um LCID para a localidade inglês dos EUA e os seguintes sinalizadores [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa): LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**Windows 2000:**  A SORTid no LCID é ignorada. Uma SORTid de SORT_DEFAULT sempre é usada.

**Windows 2000:**  Os sinalizadores [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) devem conter os seguintes sinalizadores: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. Além disso, os sinalizadores [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)podem conter os seguintes sinalizadores: NORM_IGNORENONSPACE.

**Observação**  Se o seu aplicativo quiser armazenar dados Unicode, é altamente recomendável que você não confie nos parâmetros Unicode padrão para seus índices. O uso do inglês americano é equivalente o uso da localidade invariável e os sinalizadores de [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)padrão são conhecidos por sério interferem em alguns idiomas. Você sempre deve especificar suas próprias configurações para os parâmetros Unicode para JetCreateIndex2 usando [JET_INDEXCREATE](./jet-indexcreate-structure.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Especial</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>JET_UNICODEINDEX * (JET_UNICODEINDEX)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Especial</p></td>
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


### <a name="requirements"></a>Requisitos

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


### <a name="see-also"></a>Consulte Também

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
