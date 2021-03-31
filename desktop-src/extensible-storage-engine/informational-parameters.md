---
description: 'Saiba mais sobre: parâmetros informativos'
title: Parâmetros informativos
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647604"
---
# <a name="informational-parameters"></a>Parâmetros informativos


_**Aplica-se a:** Windows | Windows Server_

## <a name="informational-parameters"></a>Parâmetros informativos

Este tópico contém parâmetros que são usados para expor informações sobre o mecanismo de banco de dados.

*JET_paramKeyMost*  
134  

Esse parâmetro somente leitura indica o comprimento máximo de chave de índice permitido que pode ser selecionado para o tamanho da página do banco de dados atual (conforme configurado por JET_paramDatabasePageSize).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>JET_cbKeyMost4KBytePage</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>255 – 65535</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Começando com o Windows Server 2008 e o Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxColtyp*  
131  

Esse parâmetro somente leitura retorna o [JET_COLTYP](./jet-coltyp.md) máximo (JET_coltypMax) para essa versão do mecanismo de banco de dados. Esse valor pode ser usado para testar o suporte de um [JET_COLTYP](./jet-coltyp.md)específico. Se um determinado [JET_COLTYP](./jet-coltyp.md) for menor que o valor desse parâmetro, ele será suportado pelo mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>JET_coltypUnsignedShort + 1</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 255</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Começando com o Windows Server 2008 e o Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramLVChunkSizeMost*  
163  

Parâmetro somente leitura que retorna o tamanho da parte de valor longo com base no tamanho da página configurada. Se um valor longo for para ser lido ou gravado com várias chamadas de coluna Jet {Set, Retrieve}, o uso de um buffer cujo tamanho é um múltiplo do tamanho da parte é mais eficiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>2 KB página = 1966 bytes<br />
página de 4 KB = 4014 bytes<br />
8 KB página = 8110 bytes<br />
16 KB página = 4050 bytes<br />
32 KB página = 8150 bytes</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-10000</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p></p></td>
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
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
