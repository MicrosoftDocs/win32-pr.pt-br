---
description: 'Saiba mais sobre: estrutura JET_RECSIZE dados'
title: estrutura JET_RECSIZE dados
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
ms.openlocfilehash: a7ea4520a75e83c77a6403a583e9131a15df337b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988219"
---
# <a name="jet_recsize-structure"></a>estrutura JET_RECSIZE dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_recsize-structure"></a>estrutura JET_RECSIZE dados

A **estrutura JET_RECSIZE** é usada pelo [JetGetRecordSize](./jetgetrecordsize-function.md) para retornar informações sobre os requisitos de uso de um registro no espaço de dados do usuário, o número de colunas definidas, o número de valores e o espaço de sobrecarga da estrutura de registro ESE.

**Windows Vista:** A **estrutura JET_RECSIZE** é introduzida no Windows Vista.

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

Dados do usuário associados ao registro, mas armazenados na árvore de valor longo.

**Observação**  Isso não conta valores longos intrínsecos.

**cbOverhead**

A sobrecarga da estrutura de registro ESE para esse registro. Isso inclui o tamanho da chave do registro.

**cbLongValueOverhead**

A sobrecarga dos dados de valor longo.

**Observação**  Isso não conta valores longos intrínsecos.

**cNonTaggedColumns**

Número total de colunas fixas e variáveis definidas neste registro.

**cTaggedColumns**

Número total de colunas marcadas definidas neste registro.

**cLongValues**

Número total de valores longos armazenados na árvore de valores longos para esse registro.

**Observação**  Isso não conta valores longos intrínsecos.

**cMultiValues**

O acúmulo do número total de valores além do primeiro para todas as colunas no registro.

### <a name="remarks"></a>Comentários

O número total de valores no registro seria **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetGetRecordSize](./jetgetrecordsize-function.md)
