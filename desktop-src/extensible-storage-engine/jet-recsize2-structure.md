---
description: 'Saiba mais sobre: estrutura de JET_RECSIZE2'
title: Estrutura de JET_RECSIZE2
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
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791504"
---
# <a name="jet_recsize2-structure"></a>Estrutura de JET_RECSIZE2


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_recsize2-structure"></a>Estrutura de JET_RECSIZE2

A estrutura de **JET_RECSIZE2** é usada pelo [JetGetRecordSize2](./jetgetrecordsize2-function.md) para retornar informações sobre os requisitos de uso de um registro no espaço de dados do usuário, o número de colunas definidas, o número de valores e o espaço de sobrecarga da estrutura de registro do ESE.

**Windows 7:** A estrutura de **JET_RECSIZE2** é introduzida no sistema operacional Windows 7.

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

**cCompressedColumns**

O número total de colunas compactadas.

**cbDataCompressed**

O tamanho compactado dos dados do usuário neste registro. Isso é o mesmo que cbData se nenhum valor longo intrínseco for compactado.

**cbLongValueDataCompressed**

O tamanho compactado dos dados do usuário na árvore de valor longo. Isso é o mesmo que os dados de cbLongValue se nenhum valor longo separado for compactado.

### <a name="remarks"></a>Comentários

O número total de valores no registro seria **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

Os dados lógicos no registro são (cbData + cbLongValueData) e o tamanho físico dos dados é (cbDataCompressed + cbLongValueDataCompressed). Isso pode ser usado para calcular a taxa de compactação de dados armazenados.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o sistema operacional Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o sistema operacional Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetGetRecordSize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
