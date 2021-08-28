---
description: 'Saiba mais sobre: Função JetEnableMultiInstance'
title: Função JetEnableMultiInstance
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dba0b8094187f3a59f05f4b1a1fae1b95dbab66e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989029"
---
# <a name="jetenablemultiinstance-function"></a>Função JetEnableMultiInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetenablemultiinstance-function"></a>Função JetEnableMultiInstance

A **função JetEnableMultiInstance** configura o mecanismo de banco de dados para uso com várias instâncias no mesmo processo. Uma matriz opcional de parâmetros de sistema global está disponível para o primeiro chamador, permitindo a alteração no modo de várias instâncias.

**Windows XP: JetEnableMultiInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Parâmetros

*psetsysparam*

Uma matriz de parâmetros globais do sistema a definir se e somente se o mecanismo entrar no modo de várias instâncias como resultado dessa chamada. Se *csetsysparam* for zero, *psetsysparam* será ignorado.

*csetsysparam*

A contagem de elementos para a matriz de parâmetros globais definir se e somente se o mecanismo entrar no modo de várias instâncias como resultado dessa chamada. Se *csetsysparam* for zero, *psetsysparam* será ignorado.

*pcsetsucceed*

Um ponteiro para a contagem de parâmetros globais do sistema que foram configurados com êxito como resultado dessa chamada.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Os parâmetros de índice de tupla especificados não eram permitidos. Esse erro pode ser retornado por <strong>JetEnableMultiInstance</strong> somente ao definir JET_paramIndexTuplesLengthMin <a href="gg294119(v=exchg.10).md">,</a> <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> como um valor ilegal.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidPath</p> | <p>O caminho do sistema de arquivos especificado era inválido. Esse erro pode ser retornado por <strong>JetEnableMultiInstance</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos. Por exemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> pode retornar esse erro.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>A operação falhou porque é ilegal quando o mecanismo de banco de dados está operando no modo de instância única (Windows modo de compatibilidade 2000).</p> | 
| <p>JET_errSystemParamsAlreadySet</p> | <p><strong>JetEnableMultiInstance</strong> falhou porque o mecanismo já está no modo de várias instâncias.</p><p><strong>Observação  </strong> Isso ocorrerá mesmo se nenhum parâmetro do sistema for especificado.</p> | 



Se essa função for bem-sucedida, o mecanismo de banco de dados será configurado para ser executado no modo de várias instâncias. O mecanismo também foi configurado com êxito com a lista opcional de parâmetros do sistema global.

Se essa função falhar, o mecanismo de banco de dados permanecerá no modo atual. Se *pcsetsucceed for* diferente de zero, esse número de parâmetros do sistema permanecerá definido.

#### <a name="remarks"></a>Comentários

Essa função só deverá ser usada se o aplicativo deve configurar um determinado conjunto de parâmetros do sistema atomicamente ao configurar o mecanismo de banco de dados para uso em um cenário de vários usuários no mesmo processo. Se outro método de sincronização estiver disponível, é preferível chamar [JetCreateInstance](./jetcreateinstance-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) separadamente.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetEnableMultiInstanceW</strong> (Unicode) e <strong>JetEnableMultiInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
