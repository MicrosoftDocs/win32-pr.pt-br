---
description: 'Saiba mais sobre: estrutura de JET_ERRINFOBASIC_W'
title: Estrutura de JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103930774"
---
# <a name="jet_errinfobasic_w-structure"></a>Estrutura de JET_ERRINFOBASIC_W


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_errinfobasic_w-structure"></a>Estrutura de JET_ERRINFOBASIC_W

A estrutura de **JET_ERRINFOBASIC_W** define os dados que são retornados do método [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) quando o JET_ErrorInfoSpecificErr InfoLevel é passado.

Observação: esta documentação se baseia em uma versão preliminar do mecanismo de armazenamento extensível. Essas informações estão sujeitas a alterações.

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura, em bytes. Ele deve ser definido como sizeof (JET_ERRINFOBASIC).

**errValue**

O valor de erro que foi avaliado, conforme passado para o argumento *pvResult* para [JetGetErrorInfo ()](./jetgeterrorinfow-function.md).

**errcatMostSpecific**

A constante [JET_ERRCAT](./jet-errcat.md) de nível mais baixo associada ao erro; ou seja, a categoria de nível folha na hierarquia de categoria documentada em [JET_ERRCAT](./jet-errcat.md).

**rgCategoricalHierarchy \[ 8\]**

A hierarquia de categorias de erro que está associada ao erro. A posição 0 é o nível mais alto na hierarquia de [JET_ERRCAT](./jet-errcat.md)e o restante são subcategorias até que a categoria mais específica seja definida, após a qual todas as categorias são JET_errcatUnknown.

**lSourceLine**

Reservado.

**rgszSourceFile \[ 64\]**

Reservado.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>
