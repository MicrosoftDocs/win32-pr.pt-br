---
description: 'Saiba mais sobre: Função JetGotoSecondaryIndexBookmark'
title: Função JetGotoSecondaryIndexBookmark
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca8b05c0eeac88521d03b95a94f7d2363d5746e9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468943"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>Função JetGotoSecondaryIndexBookmark


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgotosecondaryindexbookmark-function"></a>Função JetGotoSecondaryIndexBookmark

A **função JetGotoSecondaryIndexBookmark** posiciona um cursor para uma entrada de índice associada ao indicador de índice secundário especificado. O indicador de índice secundário deve ser usado com o mesmo índice na mesma tabela da qual foi originalmente recuperado. O indicador de índice secundário para uma entrada de índice pode ser recuperado usando **JetGotoSecondaryIndexBookmark**.

**Windows XP:****JetGotoSecondaryIndexBookmark** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*pvSecondaryKey*

O buffer que contém a chave secundária a ser usada para posicionar o cursor.

*cbSecondaryKey*

O tamanho da chave secundária no buffer.

*pvPrimaryBookmark*

O buffer que contém o indicador de chave primária a ser usado para posicionar o cursor.

*cbPrimaryBookmark*

O tamanho do indicador de chave primária no buffer.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBookmarkPermitVirtualCurrency</p> | <p>Caso a entrada de índice não possa mais ser encontrada, o cursor será posicionado à esquerda onde essa entrada de índice foi encontrada anteriormente. A operação ainda falhará com JET_errRecordDeleted; no entanto, será possível mover para a entrada de índice seguinte ou anterior em relação à entrada de índice que agora está ausente.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque é porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>O indicador de índice secundário fornecido era inválido. Esse erro pode ter ocorrido porque a chave secundária é zero ou o ponteiro do buffer de chave secundária é <strong>NULL.</strong> Esse erro ocorre porque</p><ul><li><p>O índice secundário atual não tem uma restrição de exclusividade e o tamanho do indicador fornecido é zero.</p></li><li><p>O ponteiro do buffer de indicador é <strong>NULL.</strong></p></li></ul> | 
| <p>JET_errNoCurrentIndex</p> | <p>O cursor não está atualmente em um índice secundário. Não é significativo ir para um indicador de índice secundário quando o cursor não está usando um índice secundário no momento. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> deve ser usado quando o cursor não está em um índice secundário.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Não foi possível encontrar a entrada de índice associada ao indicador de índice secundário.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p> | 



Se essa função for bem-sucedida, o cursor será posicionado em uma entrada de índice associada ao indicador de índice secundário especificado. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor usar, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, a posição do cursor permanecerá inalterada, a menos que JET_errRecordDeleted seja retornado e JET_bitBookmarkPermitVirtualCurrency for especificado. Nesse caso, o cursor será posicionado onde a entrada de índice associada ao indicador de índice secundário especificado teria sido. O cursor pode ser movido em relação a essa posição, mas ainda não está em uma entrada de índice válida.

Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor usar, essa chave de pesquisa será excluída. Em qualquer caso, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
