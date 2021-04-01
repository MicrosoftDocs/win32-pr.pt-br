---
description: 'Saiba mais sobre: estrutura de JET_RSTINFO'
title: Estrutura de JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090129"
---
# <a name="jet_rstinfo-structure"></a>Estrutura de JET_RSTINFO


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_rstinfo-structure"></a>Estrutura de JET_RSTINFO

A estrutura de **JET_RSTINFO** contém informações de controle para o processo de recuperação, como informações de realocação de banco de dados e a capacidade de controlar a interrupção da recuperação.

**Windows Vista:** A estrutura de **JET_RSTINFO** é introduzida no Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura.

**rgrstmap**

A estrutura que descreve o caminho novo e antigo de um banco de dados restaurado.

**crstmap**

Contagem de entradas de matriz no rgrstmap.

**lgposStop**

A posição do log para parar a recuperação em. Nenhum desfazer será feito.

**logtimeStop**

Reservado para uso futuro.

**pfnStatus**

Uma função de status para relatar o status da recuperação.

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
<td><p>Implementado como <strong>JET_RSTINFO_W</strong> (Unicode) e <strong>JET_RSTINFO_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetInit3](./jetinit3-function.md)
