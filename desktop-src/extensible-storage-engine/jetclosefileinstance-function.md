---
description: 'Saiba mais sobre: Função JetCloseFileInstance'
title: Função JetCloseFileInstance
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d837d1932559c39d6a3b249f934ef77cc56de11a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982970"
---
# <a name="jetclosefileinstance-function"></a>Função JetCloseFileInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetclosefileinstance-function"></a>Função JetCloseFileInstance

A **função JetCloseFileInstance** fecha um arquivo que foi aberto com [JetOpenFileInstance](./jetopenfileinstance-function.md) depois que os dados desse arquivo foram extraídos usando [JetReadFileInstance](./jetreadfileinstance-function.md).

**Windows XP: JetCloseFileInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância a ser usada para essa chamada.

Por Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global está implícito nesse caso.

Para Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só poderá ser chamada quando o mecanismo estiver no modo herdado (modo de compatibilidade do Windows 2000), em que há suporte para apenas uma instância. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

*hfFile*

O alça do arquivo a ser lido.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado. Isso pode acontecer para <strong>JetCloseFileInstance</strong> quando:</p><ul><li><p>O handle de instância especificado é inválido (Windows XP e versões posteriores)</p></li><li><p>O alça de arquivo especificado é inválido</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (Windows modo de compatibilidade 2000), em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, o alça de arquivo é fechado. Se um arquivo de banco de dados tiver sido fechado, o arquivo de patch de banco de dados associado (se algum) for destruído.

Em caso de falha, nenhuma alteração ocorre.

#### <a name="remarks"></a>Comentários

Atualmente, o mecanismo de banco de dados dá suporte apenas a um arquivo aberto por [meio de JetOpenFileInstance](./jetopenfileinstance-function.md) por vez. Se um alça de arquivo for aberto usando [JetOpenFileInstance,](./jetopenfileinstance-function.md) ele deverá ser fechado usando **JetCloseFileInstance** antes que outro arquivo possa ser aberto.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
