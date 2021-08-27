---
description: 'Saiba mais sobre: função JetPrereadIndexRanges'
title: Função JetPrereadIndexRanges
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ff2d9e7c538e8aa8cc862fe9a72c0308e497fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986659"
---
# <a name="jetprereadindexranges-function"></a>Função JetPrereadIndexRanges


_**Aplica-se a:** Windows | Windows Servidor_

A função **JetPrereadIndexRanges** lê índices para melhorar o desempenho.

a função **JetPrereadIndexRanges** foi introduzida no sistema operacional Windows 8.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela na qual os itens são relidos.

*rgIndexRanges*

Os intervalos de chave a serem lidos.

*cIndexRanges*

O número de intervalos de chave a serem lidos, determinados pelo número de elementos em *rgIndexRanges*.

*pcRangesPreread*

O número de intervalos de chave que foram realmente lidos.

*rgcolumnidPreread*

Lista de IDs de coluna para colunas de valor longo a serem lidas. Por padrão, somente o registro na página é de leitura. Se colunas de valor longo fora da página precisarem ser lidas, suas IDs de coluna precisarão ser passadas por esse parâmetro.

*ccolumnidPreread*

O número de IDs de coluna para colunas de valor longo a serem lidas, determinado pelo número de elementos em *rgcolumnidPreread*.

*grbit*

Um grupo de bits que especifica zero ou mais valores de direção de preread listados na tabela a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>Encaminhar</p> | <p>Leitura antecipada.</p> | 
| <p>Compatibilidade</p> | <p>Leia o retrocesso.</p> | 
| <p>FirstPageOnly</p> | <p>Somente Leia a primeira página de qualquer coluna longa.</p> | 
| <p>NormalizedKey</p> | <p>Chave/indicador normalizado fornecido em vez do valor da coluna.</p> | 



### <a name="return-value"></a>Valor retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. para obter mais informações sobre os possíveis erros do ESE (extensible Armazenamento engine), consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 



#### <a name="remarks"></a>Comentários

Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, você deverá iniciar as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2012.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte também

[JET_ERR](./jet-err.md)
