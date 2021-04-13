---
description: 'Saiba mais sobre: estrutura de JET_SNPROG'
title: Estrutura de JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457261"
---
# <a name="jet_snprog-structure"></a>Estrutura de JET_SNPROG


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_snprog-structure"></a>Estrutura de JET_SNPROG

A estrutura de **JET_SNPROG** contém informações sobre o progresso de uma operação de execução longa. Quando a função de retorno de chamada é chamada para notificar o status da operação e a operação ainda está em andamento, o último parâmetro da função de retorno de chamada é um ponteiro para uma estrutura de **JET_SNPROG** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura de **JET_SNPROG** , em bytes. Esse valor confirma a presença dos campos a seguir.

**cunitDone**

O número de unidades de trabalho que já foram concluídas durante a função de execução longa.

**cunitTotal**

O número de unidades de trabalho que precisam ser concluídas. Esse valor deve ser sempre maior ou igual a **cunitDone**.

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

