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
ms.openlocfilehash: cb2779c75d525e45e9140d8f70665a09fe202b21
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988109"
---
# <a name="jet_unicodeindex-structure"></a>Estrutura de JET_UNICODEINDEX


_**Aplica-se a:** Windows | Windows Servidor_

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

**Windows 2000**: os dois únicos valores válidos para **dwFlags** são:

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)

<!-- end list -->

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)

**dwMapFlags** tem as seguintes restrições.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>LCMAP_SORTKEY</p> | <p>Mandatory.</p> | 
| <p>LCMAP_BYTEREV</p> | <p>Opcional.</p> | 
| <p>NORM_IGNORECASE</p> | <p>Opcional.</p> | 
| <p>NORM_IGNORENONSPACE</p> | <p>Opcional.</p> | 
| <p>NORM_IGNORESYMBOLS</p> | <p>Opcional.</p> | 
| <p>NORM_IGNOREKANATYPE</p> | <p>Opcional.</p> | 
| <p>NORM_IGNOREWIDTH</p> | <p>Opcional.</p> | 
| <p>SORT_STRINGSORT</p> | <p>Opcional.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
