---
description: 'Saiba mais sobre: estrutura de JET_RECSIZE'
title: Estrutura de JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
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
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646738"
---
# <a name="jet_recsize-structure"></a>Estrutura de JET_RECSIZE


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>Estrutura de JET_RECSIZE

A estrutura de **JET_RECSIZE** é usada pelo [JetGetRecordSize](./jetgetrecordsize-function.md) para retornar informações sobre os requisitos de uso de um registro no espaço de dados do usuário, o número de colunas definidas, o número de valores e o espaço de sobrecarga da estrutura de registro do ESE.

**Windows Vista:** A estrutura de **JET_RECSIZE** é introduzida no Windows Vista.

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a>Membros

**cbData**

Conjunto de dados do usuário no registro.

**Observação**  O tamanho da chave não está incluído neste.

**cbLongValueData**

Dados de usuário associados ao registro, mas armazenados na árvore de valor longo.

**Observação**  Isso não conta os valores intrínsecos longos.

**cbOverhead**

A sobrecarga da estrutura do registro ESE para esse registro. Isso inclui o tamanho da chave do registro.

**cbLongValueOverhead**

A sobrecarga dos dados de valor longo.

**Observação**  Isso não conta os valores intrínsecos longos.

**cNonTaggedColumns**

Número total de colunas fixas e variáveis definidas neste registro.

**cTaggedColumns**

Número total de colunas marcadas definidas neste registro.

**cLongValues**

Número total de valores longos armazenados na árvore de valor longo deste registro.

**Observação**  Isso não conta os valores intrínsecos longos.

**cMultiValues**

A acumulação do número total de valores além do primeiro para todas as colunas no registro.

### <a name="remarks"></a>Comentários

O número total de valores no registro seria **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

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

[JetGetRecordSize](./jetgetrecordsize-function.md)
