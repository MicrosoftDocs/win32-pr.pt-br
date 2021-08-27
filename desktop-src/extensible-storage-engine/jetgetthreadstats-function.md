---
description: 'Saiba mais sobre: função JetGetThreadStats'
title: Função JetGetThreadStats
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b47cd9de933efdc5a73aba32a212432a9e37a12
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984669"
---
# <a name="jetgetthreadstats-function"></a>Função JetGetThreadStats


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetthreadstats-function"></a>Função JetGetThreadStats

A função **JetGetThreadStats** recupera informações de desempenho do mecanismo de banco de dados para o thread atual. Várias chamadas podem ser usadas para coletar estatísticas que refletem a atividade do mecanismo de banco de dados nesse thread entre essas chamadas.

**Windows vista:** o **JetGetThreadStats** é introduzido no Windows Vista.  

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parâmetros

*pvResult*

O buffer de saída que recebe os dados de estatísticas de thread. O buffer contém uma estrutura de [JET_THREADSTATS](./jet-threadstats-structure.md) após uma chamada bem-sucedida.

*cbMax*

O tamanho máximo em bytes do buffer de saída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>A operação falhou porque o buffer de saída fornecido era muito pequeno para conter os dados solicitados. A função <strong>JetGetThreadStats</strong> retornará esse erro quando o buffer de saída for muito pequeno para conter a menor versão da estrutura de <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> suportada pelo mecanismo de banco de dados.</p> | 



Em caso de sucesso, o buffer de saída conterá uma estrutura de [JET_THREADSTATS](./jet-threadstats-structure.md) que contém estatísticas do mecanismo de banco de dados para o thread atual.

Em caso de falha, o estado do buffer de saída é indefinido.

#### <a name="remarks"></a>Comentários

As informações fornecidas por duas chamadas consecutivas dessa API devem ser usadas para computar a despesa de qualquer outra operação do mecanismo de banco de dados no thread atual. Em geral, isso é feito fazendo uma leitura anterior e posterior das estatísticas e subtraindo a contagem After da contagem before para obter a contagem líquida de operações executadas.

Por exemplo, um aplicativo poderia chamar **JetGetThreadStats** uma vez para obter uma leitura inicial das estatísticas para o thread atual. Em seguida, ele pode chamar a função [JetMove](./jetmove-function.md) com o parâmetro de *galinha* definido como JET_MoveNext para mover para a próxima entrada de índice em um índice. Em seguida, ele pode chamar **JetGetThreadStats** novamente para obter outra leitura das estatísticas do thread. Em seguida, ele pode subtrair o contador cPageReferenced da segunda leitura do primeiro. O resultado seria o número de páginas de banco de dados referenciadas pelo mecanismo de banco de dados para executar a operação [JetMove](./jetmove-function.md) .

As estatísticas de cada thread são acumuladas durante o tempo de vida desse thread. As estatísticas serão redefinidas se a DLL do mecanismo de banco de dados for descarregada do processo de host.

A estrutura de [JET_THREADSTATS](./jet-threadstats-structure.md) provavelmente será expandida no futuro para conter mais estatísticas. Novas estatísticas serão adicionadas ao final da estrutura e poderão ser recuperadas com um tamanho de buffer de saída maior. A presença de estatísticas adicionais pode ser inferida por um valor cbStruct maior.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)
