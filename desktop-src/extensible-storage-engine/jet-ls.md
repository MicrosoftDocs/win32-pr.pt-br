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
ms.openlocfilehash: 82a0df37215122e943955f32aeed4d39dd70b268
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983149"
---
# <a name="jet_ls"></a>JET_LS


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_ls"></a>JET_LS

O tipo de dados **JET_LS** contém um identificador de contexto para armazenamento local (ls). Esse identificador pode ser associado a um cursor ou uma tabela e pode se referir a recursos alocados dinamicamente.

**Windows xp: JET_LS** é introduzido no Windows XP.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Tipos de dados

JET_LS

Um valor de JET_LSNil indica um identificador de contexto inválido.

### <a name="remarks"></a>Comentários

Um identificador de contexto é inicialmente associado ao tipo de dados **JET_LS** , usando [JetSetLS](./jetsetls-function.md). O identificador de contexto pode ser recuperado do tipo de dados **JET_LS** , usando [JetGetLS](./jetgetls-function.md).

O identificador de contexto pode ser explicitamente desassociado do tipo de dados **JET_LS** usando [JetGetLS](./jetgetls-function.md) com JET_bitLSReset. Como alternativa, o identificador de contexto pode ser implicitamente desassociado do tipo de dados **JET_LS** quando o objeto subjacente é liberado pelo mecanismo de banco de dados como resultado de uma ação direta ou indireta pelo aplicativo. No caso implícito, um retorno de chamada de tempo de execução é emitido para o aplicativo para que ele possa limpar o identificador de contexto. Para obter mais informações sobre como desassociar implicitamente do tipo de dados **JET_LS** , consulte [JetSetLS](./jetsetls-function.md).

Os sinalizadores a seguir são associados ao tipo de dados JET_LS.


| <p>Termo</p> | <p>Descrição</p> | 
|-------------|--------------------|
| <p>JET_bitLSReset</p> | <p>O identificador de contexto é desassociado do objeto.</p> | 
| <p>JET_bitLSCursor</p> | <p>Definir ou recuperar o armazenamento local associado a um cursor de tabela.</p> | 
| <p>JET_bitLSTable</p> | <p>Definir ou recuperar o armazenamento local associado a uma tabela.</p> | 
| <p>JET_LSNil</p> | <p>O identificador de contexto é inválido.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
