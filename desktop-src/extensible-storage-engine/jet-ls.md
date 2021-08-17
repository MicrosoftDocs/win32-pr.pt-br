---
description: 'Saiba mais sobre: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 38ddb306ee6fdcbd1eb792b2c29ca367adc0f4b88cc25dfcbdde22c2638258d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765032"
---
# <a name="jet_ls"></a>JET_LS


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_ls"></a>JET_LS

O **JET_LS** de dados contém um identificador de contexto para o armazenamento local (LS). Esse handle pode ser associado a um cursor ou a uma tabela e pode se referir a recursos alocados dinamicamente.

**Windows XP: JET_LS** é introduzido no Windows XP.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Tipos de dados

JET_LS

Um valor de JET_LSNil indica um alça de contexto inválido.

### <a name="remarks"></a>Comentários

Um identificador de contexto é inicialmente associado ao tipo **JET_LS** de dados, usando [JetSetLS](./jetsetls-function.md). O identificador de contexto pode ser recuperado do tipo **JET_LS** de dados, usando [JetGetLS](./jetgetls-function.md).

O identificador de contexto pode ser desassociado explicitamente do **tipo de dados JET_LS** usando [JetGetLS](./jetgetls-function.md) com JET_bitLSReset. Como alternativa, o identificador de contexto pode ser desassociado implicitamente do tipo de dados **JET_LS** quando o objeto subjacente é liberado pelo mecanismo de banco de dados como resultado da ação direta ou indireta do aplicativo. No caso implícito, um retorno de chamada de runtime é emitido para o aplicativo para que ele possa limpar o handle de contexto. Para obter mais informações sobre a desassociação implícita do **tipo JET_LS** dados, consulte [JetSetLS](./jetsetls-function.md).

Os sinalizadores a seguir são associados ao tipo JET_LS dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Termo</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>O identificador de contexto é desassociado do objeto .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSCursor</p></td>
<td><p>Definir ou recuperar o armazenamento local associado a um cursor de tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Definir ou recuperar o armazenamento local associado a uma tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_LSNil</p></td>
<td><p>O alça de contexto é inválido.</p></td>
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
<td><p>Requer Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
