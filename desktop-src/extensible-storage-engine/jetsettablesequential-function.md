---
description: 'Saiba mais sobre: Função JetSetTableSequential'
title: Função JetSetTableSequential
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a8b49b112c9566b15226e8ffd52f4240cff2fb8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471712"
---
# <a name="jetsettablesequential-function"></a>Função JetSetTableSequential


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsettablesequential-function"></a>Função JetSetTableSequential

A **função JetSetTableSequential** notifica o mecanismo de banco de dados de que o aplicativo está digitalizando todo o índice atual que contém um determinado cursor. Consequentemente, os métodos usados para acessar os dados de índice serão ajustados para tornar esse cenário o mais rápido possível.

**Windows XP:****JetSetTableSequential** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*grbit*

Um grupo de bits que especificam zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitPrereadForward</p> | <p>Essa opção é usada para indexar na direção da frente.</p><p><strong>Windows 7:</strong><strong>JET_bitPrereadForward</strong> é introduzido no Windows 7.  </p> | 
| <p>JET_bitPrereadBackward</p> | <p>Essa opção é usada para indexar na direção para trás.</p><p><strong>Windows 7:</strong><strong>JET_bitPrereadBackward</strong> é introduzido no Windows 7.  </p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram quiesced como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p> | 



Se essa função for bem-sucedida, o índice atual do cursor será otimizado para uma verificação sequencial de todo o índice. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, nenhuma alteração na configuração do cursor ocorrerá. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Se o aplicativo precisar verificar com eficiência um subconjunto conhecido de um índice, uma otimização semelhante também será executada sempre que um intervalo de índices for estabelecido usando [JetSetIndexRange](./jetsetindexrange-function.md). Essa otimização só está disponível no Windows XP e versões posteriores.

Se o aplicativo precisar verificar com eficiência um subconjunto desconhecido de um índice, nenhuma ação deverá ser tomada. O mecanismo pode detectar automaticamente o comportamento de verificação e buscará dados com antecedência. No entanto, esse comportamento não é tão agressivo.

Essa otimização torna a verificação do índice primário eficiente e torna a verificação apenas os dados de entrada de índice em um índice secundário eficiente. Ele não tornará a verificação de um índice secundário ao recuperar dados de registro eficiente. Isso acontece porque o mecanismo não executa uma leitura antecipada nos dados de registro.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
