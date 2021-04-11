---
description: 'Saiba mais sobre: estrutura de JET_SETSYSPARAM'
title: Estrutura de JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296247"
---
# <a name="jet_setsysparam-structure"></a>Estrutura de JET_SETSYSPARAM


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_setsysparam-structure"></a>Estrutura de JET_SETSYSPARAM

Uma matriz de estruturas de **JET_SETSYSPARAM** indicam um conjunto específico de parâmetros de sistema global que são definidos como um argumento ao usar a função [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .

**Windows XP:** Essa estrutura é introduzida no Windows XP.

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a>Membros

**paramid**

A ID do parâmetro do sistema que será definido.

Consulte [parâmetros do sistema do mecanismo de armazenamento extensível](./extensible-storage-engine-system-parameters.md) para obter uma lista completa de parâmetros do sistema e suas propriedades.

**lParam**

O valor opcional a ser definido para o parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo inteiro.

**sz**

O valor opcional a ser definido para o parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo de cadeia de caracteres.

**erra**

O erro resultante da chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md) com os parâmetros especificados anteriormente.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JET_ SETSYSPARAM_W</strong> (Unicode) e <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[Parâmetros do sistema do mecanismo de armazenamento extensível](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
