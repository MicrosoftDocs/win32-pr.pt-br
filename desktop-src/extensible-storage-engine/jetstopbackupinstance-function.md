---
description: 'Saiba mais sobre: função JetStopBackupInstance'
title: Função JetStopBackupInstance
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4dae676cfbbb0f2509a7d86fbb6507b8e2110f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987239"
---
# <a name="jetstopbackupinstance-function"></a>Função JetStopBackupInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetstopbackupinstance-function"></a>Função JetStopBackupInstance

A função **JetStopBackupInstance** impede que o streaming da atividade relacionada ao backup continue em uma instância em execução específica, encerrando assim o backup de streaming de forma previsível.

**Windows xp:** o **JetStopBackupInstance** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

Identifica a instância em execução a ser usada para a chamada à API.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O parâmetro de instância especificado tem um valor inválido (não uma instância que está sendo executada no momento).</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 



Se essa função for realizada com êxito, a instância especificada começará a falhar quaisquer novas APIs de backup de streaming.

Se essa função falhar, nenhuma etapa a ser preparada para o término do backup na instância será executada e nenhuma alteração no estado da instância ocorrerá.

#### <a name="remarks"></a>Comentários

O backup é geralmente disparado por um evento fora do mecanismo de processo e usando essa API, o aplicativo ESENT em si fará outras chamadas para que as APIs de backup de streaming falhem. A maioria das APIs de backup de streaming começará a falhar com JET_errBackupAbortByServer. Assim, qualquer progresso de backup de streaming (como [JetReadFileInstance](./jetreadfileinstance-function.md)) retornará um erro. Operações de backup que fazem parte do encerramento de backup (como [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ainda serão permitidas.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
