---
description: 'Saiba mais sobre: função JetIdle'
title: Função JetIdle
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: babe3077c01b6b2a9c1f2f55b48921582d6343bd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984539"
---
# <a name="jetidle-function"></a>Função JetIdle


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetidle-function"></a>Função JetIdle

A função **JetIdle** está expirada e deve ser usada somente para fins de teste. **JetIdle** pode ser usado para executar tarefas de limpeza ociosas ou verificar o status do repositório de versão no ESE.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão que será usada para esta chamada.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes bits:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIdleCompact</p> | <p>Dispara a limpeza do repositório de versão.</p> | 
| <p>JET_bitIdleFlushBuffers</p> | <p>Reservado para uso futuro. Se esse sinalizador for especificado, a API retornará JET_errInvalidgrbit.</p> | 
| <p>JET_bitIdleStatus</p> | <p>Retorna JET_wrnIdleFull se o repositório de versão for maior que metade cheio.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro <em>grbit</em> fornecido à API não era válido.</p> | 



Se essa função for realizada com sucesso, a operação apropriada será disparada ou um código de erro indicando o quão completo o repositório de versão está dependendo do *grbit* fornecido.

Se essa função falhar, a operação solicitada não será concluída com êxito.

#### <a name="remarks"></a>Comentários

O repositório de versão mantém o mecanismo de isolamento de instantâneo do ESE. Se o repositório de versão for mais do que metade cheio, o programa poderá fechar transações de longa execução. Se uma transação de longa execução esgotar o armazenamento de versão, o ESE interromperá a permissão de operações de gravação no banco de dados.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
