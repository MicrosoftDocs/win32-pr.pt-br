---
description: 'Saiba mais sobre: estrutura de JET_UNICODEINDEX'
title: Estrutura de JET_UNICODEINDEX
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104371030"
---
# <a name="jet_unicodeindex-structure"></a>Estrutura de JET_UNICODEINDEX


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_unicodeindex-structure"></a>Estrutura de JET_UNICODEINDEX

A estrutura de **JET_UNICODEINDEX** personaliza como os dados Unicode são normalizados quando um índice é criado em uma coluna Unicode.

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>Membros

**lcid**

A ID de localidade a ser usada ao normalizar os dados. Qualquer localidade pode ser usada, desde que o pacote de idiomas apropriado tenha sido instalado no computador. A única exceção é que a localidade neutra do idioma (LCID de zero) é inválida.

**dwMapFlags**

Esses sinalizadores são passados para [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) quando os dados Unicode são normalizados para uma chave, o que permite que os sinalizadores definidos pelo usuário substituam o padrão.

**Windows 2000**: os únicos dois valores válidos para **dwFlags** são:

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)

<!-- end list -->

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)

**dwMapFlags** tem as seguintes restrições.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>LCMAP_SORTKEY</p></td>
<td><p>Mandatory.</p></td>
</tr>
<tr class="even">
<td><p>LCMAP_BYTEREV</p></td>
<td><p>Opcional.</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNORECASE</p></td>
<td><p>Opcional.</p></td>
</tr>
<tr class="even">
<td><p>NORM_IGNORENONSPACE</p></td>
<td><p>Opcional.</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNORESYMBOLS</p></td>
<td><p>Opcional.</p></td>
</tr>
<tr class="even">
<td><p>NORM_IGNOREKANATYPE</p></td>
<td><p>Opcional.</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNOREWIDTH</p></td>
<td><p>Opcional.</p></td>
</tr>
<tr class="even">
<td><p>SORT_STRINGSORT</p></td>
<td><p>Opcional.</p></td>
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

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
