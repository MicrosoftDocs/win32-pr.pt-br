---
description: 'Saiba mais sobre: Função JetGetInstanceInfo'
title: Função JetGetInstanceInfo
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dfc8bec0e6cee6e127dc99135d82db3ee3001ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478342"
---
# <a name="jetgetinstanceinfo-function"></a>Função JetGetInstanceInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetinstanceinfo-function"></a>Função JetGetInstanceInfo

A **função JetGetInstanceInfo** recupera informações sobre as instâncias em execução.

**Windows XP: JetGetInstanceInfo** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Parâmetros

*pcInstanceInfo*

Um ponteiro para um buffer que receberá o número de elementos armazenados em *paInstanceInfo*.

*paInstanceInfo*

Um ponteiro para um buffer que receberá o endereço do primeiro elemento de uma matriz de estruturas.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Esse erro será retornado por <strong>JetGetInstanceInfo</strong> quando:</p><ul><li><p><em>pcInstanceInfo ou</em> <em>paInstanceInfo</em> são NULL.</p></li></ul> | 
| <p>JET_errOutOfMemory</p> | <p>Não há memória suficiente para processar a solicitação.</p> | 



#### <a name="remarks"></a>Comentários

O mecanismo de banco de dados alocará uma matriz de [JET_INSTANCE_INFO](./jet-instance-info-structure.md) estruturas. O chamador é responsável por liberar essa memória com [JetFreeBuffer.](./jetfreebuffer-function.md)

Se não houver instâncias ativas, **JetGetInstanceInfo** retornará JET_errSuccess e *pcInstanceInfo* receberá um valor de 0.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetInstanceInfoW</strong> (Unicode) e <strong>JetGetInstanceInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
