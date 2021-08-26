---
description: 'Saiba mais sobre: função JetSetCursorFilter'
title: Função JetSetCursorFilter
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5958d288e8b101795d1c8e4b4db789ade4b98418
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477512"
---
# <a name="jetsetcursorfilter-function"></a>Função JetSetCursorFilter


_**Aplica-se a:** Windows | Windows Servidor_

A função **JetSetCursorFilter** define uma matriz de filtros simples para a função [JetMove](./jetmove-function.md) .

a função **JetSetCursorFilter** foi introduzida no sistema operacional Windows 8.

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

O cursor a ser posicionado.

*rgFilters*

Os filtros de registro simples.

*cFilters*

O número de filtros.

*grbit*

Um grupo de bits que especifica zero ou mais das opções de movimentação listadas na tabela a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>Nenhum</p> | <p>Opção padrão.</p> | 



### <a name="return-value"></a>Valor retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. para obter mais informações sobre os possíveis erros do ESE (extensible Armazenamento engine), consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 



#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2012.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Confira também

[JetMove](./jetmove-function.md)  
[JET_ERR](./jet-err.md)
