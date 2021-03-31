---
description: 'Saiba mais sobre: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
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
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836912"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_coltyp"></a>JET_COLTYP

O **JET_COLTYP** grupo de constantes descreve todos os tipos de coluna possíveis que podem ser encontrados em uma tabela.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_coltypNil<br />
0</p></td>
<td><p>Um tipo de coluna inválido.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBit<br />
1</p></td>
<td><p>Um tipo de coluna que permite três valores: <strong>true</strong>, <strong>false</strong>ou <strong>NULL</strong>. Esse tipo de coluna tem um byte de comprimento e é um tamanho fixo. <strong>Falso</strong> classifica antes de <strong>verdadeiro</strong>. Observe que o tamanho desse tipo não corresponde ao tamanho do tipo booliano Variant.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedByte<br />
2</p></td>
<td><p>Um inteiro não assinado de 1 byte que pode assumir valores entre 0 (zero) e 255.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypShort<br />
3</p></td>
<td><p>Um inteiro com sinal de 2 bytes que pode assumir os valores entre-32768 e 32767. Valores negativos são classificados antes de valores positivos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLong<br />
4</p></td>
<td><p>Um inteiro com sinal de 4 bytes que pode assumir os valores entre-2147483648 e 2147483647. Valores negativos são classificados antes de valores positivos.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypCurrency<br />
5</p></td>
<td><p>Um inteiro com sinal de 8 bytes que pode assumir os valores entre-9.223.372.036.854.775.808 e 9223372036854775807. Valores negativos são classificados antes de valores positivos. Esse tipo de coluna é idêntico ao tipo de moeda variante. Esse tipo de coluna também pode ser usado como um inteiro com sinal de 8 bytes nativo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypIEEESingle<br />
6</p></td>
<td><p>Um número de ponto flutuante de precisão única (4 bytes).</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypIEEEDouble<br />
7</p></td>
<td><p>Um número de ponto flutuante de precisão dupla (8 bytes).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypDateTime<br />
8</p></td>
<td><p>Um número de ponto flutuante de precisão dupla (8 bytes) que representa uma data em dias fracionários desde o ano 1900. Esse tipo de coluna é idêntico ao tipo de data de variante.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBinary<br />
9</p></td>
<td><p>Uma coluna binária bruta de comprimento fixo ou variável que pode ter até 255 bytes de comprimento.</p>
<p>Esse tipo de coluna pode ser usado para implementar um GUID, se configurado como um comprimento fixo, coluna binária de 16 bytes. A única limitação é que a ordenação relativa de valores em um índice em uma coluna desse tipo não corresponderá à ordenação relativa da renderização de cadeia de caracteres de registro padrão de um GUID (ou seja, &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypText<br />
10</p></td>
<td><p>Uma coluna de texto de comprimento fixo ou variável que pode ter até 255 caracteres ASCII de comprimento ou 127 caracteres Unicode de comprimento.</p>
<p>Todas as cadeias são armazenadas como um número contado de caracteres. As cadeias de caracteres não precisam ser terminadas em nulo. Além disso, não é necessário que a contagem inclua um terminador nulo. Por fim, caracteres nulos inseridos podem ser armazenados.</p>
<p>Cadeias de caracteres ASCII são sempre tratadas como não diferencia maiúsculas de minúsculas para fins de classificação e pesquisa. Além disso, somente os caracteres que antecedem o primeiro caractere nulo (se houver) são considerados para classificação e pesquisa.</p>
<p>As cadeias de caracteres Unicode usam a API do Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> para criar chaves de classificação que são usadas posteriormente para classificar e Pesquisar esses dados. Por padrão, as cadeias de caracteres Unicode são consideradas no idioma inglês dos EUA e são classificadas e pesquisadas usando os seguintes sinalizadores de normalização: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. No Windows 2000, é possível personalizar esses sinalizadores por índice para incluir também NORM_IGNORENONSPACE. No Windows XP e versões posteriores, é possível solicitar qualquer combinação dos seguintes sinalizadores de normalização por índice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH e SORT_STRINGSORT.</p>
<p>Em todas as versões, é possível personalizar a localidade por índice. Qualquer localidade pode ser usada, desde que o pacote de idiomas apropriado tenha sido instalado no computador. Por fim, todos os caracteres nulos encontrados em uma cadeia de caracteres Unicode são completamente ignorados.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongBinary<br />
11</p></td>
<td><p>Uma coluna binária bruta de comprimento fixo ou variável que pode ter até 2147483647 bytes de comprimento. Esse tipo é considerado um valor longo. Um valor longo é especial porque pode ser grande e pode ser acessado como um fluxo. De outra forma, esse tipo é idêntico ao JET_coltypBinary.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLongText<br />
12</p></td>
<td><p>Uma coluna de texto fixa ou de comprimento variável que pode ter até 2147483647 caracteres ASCII de comprimento ou 1073741823 caracteres Unicode de comprimento. Esse tipo é considerado um valor longo. Um valor longo é especial porque pode ser grande e pode ser acessado como um fluxo. De outra forma, esse tipo é idêntico ao JET_coltypText.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypSLV<br />
13</p></td>
<td><p>Este tipo de coluna é obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedLong<br />
14</p></td>
<td><p>Um inteiro sem sinal de 4 bytes que pode assumir valores entre 0 (zero) e 4294967295.</p>
<p><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, no Windows Server 2008 e em versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongLong<br />
15</p></td>
<td><p>Um inteiro com sinal de 8 bytes que pode assumir os valores entre-9.223.372.036.854.775.808 e 9223372036854775807. Valores negativos são classificados antes de valores positivos.</p>
<p><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, no Windows Server 2008 e em versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypGUID<br />
16</p></td>
<td><p>Uma coluna binária de comprimento fixo de 16 bytes que representa nativamente o tipo de dados GUID. Os valores de coluna de GUID são classificados da mesma maneira que esses valores seriam classificados como cadeias de caracteres na forma padrão (ou seja, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</p>
<p><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, no Windows Server 2008 e em versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypUnsignedShort<br />
17</p></td>
<td><p>Um inteiro sem sinal de 2 bytes que pode assumir valores entre 0 e 65535.</p>
<p><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, no Windows Server 2008 e em versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypMax<br />
18</p></td>
<td><p>Uma constante que descreve o máximo (ou seja, um que não é o maior número de colunas válido) com suporte no mecanismo.</p>
<p>Esse valor deve ser usado com cuidado porque ele será alterado à medida que novos tipos de coluna forem suportados. Por exemplo, ele tem um valor literal diferente no Windows 2000 do que no Windows XP e versões posteriores.</p></td>
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

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
