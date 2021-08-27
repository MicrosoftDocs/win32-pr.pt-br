---
description: 'Saiba mais sobre: estrutura JET_RECSIZE2 dados'
title: estrutura JET_RECSIZE2 de JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: c187d57149b7f0589d56439bfacbf7129ab4fe4a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987829"
---
# <a name="jet_recsize2-structure"></a>estrutura JET_RECSIZE2 de JET_RECSIZE2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_recsize2-structure"></a>estrutura JET_RECSIZE2 de JET_RECSIZE2

A **estrutura JET_RECSIZE2** é usada por [JetGetRecordSize2](./jetgetrecordsize2-function.md) para retornar informações sobre os requisitos de uso de um registro no espaço de dados do usuário, o número de colunas definidas, o número de valores e o espaço de sobrecarga da estrutura de registro ESE.

**Windows 7:** A **JET_RECSIZE2** é introduzida no sistema operacional Windows 7.

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
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

**cCompressedColumns**

O número total de colunas compactadas.

**cbDataCompressed**

O tamanho compactado dos dados do usuário nesse registro. Isso será o mesmo que cbData se nenhum valor longo intrínseco for compactado.

**cbLongValueDataCompressed**

O tamanho compactado dos dados do usuário na árvore de valor longo. Isso será o mesmo que os dados cbLongValue se nenhum valor longo separado for compactado.

### <a name="remarks"></a>Comentários

O número total de valores no registro seria **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

Os dados lógicos no registro são (cbData+cbLongValueData) e o tamanho físico dos dados é (cbDataCompressed+cbLongValueDataCompressed). Isso pode ser usado para calcular a taxa de compactação dos dados armazenados.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows sistema operacional Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows sistema operacional server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetGetRecordSize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
