---
description: 'Saiba mais sobre: função JetCompact'
title: Função JetCompact
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14e79ceda56658bf8b214fff923c2df17fe8f786
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480462"
---
# <a name="jetcompact-function"></a>Função JetCompact


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcompact-function"></a>Função JetCompact

A função **JetCompact** faz uma cópia de um banco de dados existente. A cópia é compactada para um estado ideal para uso. Os dados nos dados copiados serão empacotados de acordo com as medidas escolhidas para os índices na criação do índice. Dessa forma, os dados compactados podem ser armazenados da maneira mais densa possível. Como alternativa, os dados compactados podem reservar espaço para o aumento de registro subsequente ou inserções de índice.

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*szDatabaseSrc*

O banco de dados de origem que será compactado.

*szDatabaseDest*

O nome a ser usado para o banco de dados compactado.

*pfnStatus*

Uma função de retorno de chamada que pode ser chamada periodicamente por meio da operação Compact do banco de dados para relatar o progresso.

*pconvert*

Um ponteiro usado para designar uma DLL do ESE alternativa que pode ser usada para ler o banco de dados de origem e fornecer parâmetros opcionais para uma operação **JetCompact** que está convertendo um banco de dados de um anterior para um formato de versão posterior. este recurso foi descontinuado no Windows Server 2003.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitCompactRepair</p> | <p>Usado quando o banco de dados de origem é conhecido como corrompido. Ele permite que um conjunto completo de novos comportamentos se destinasse a recuperar o máximo de dados possível do banco de dado de origem. <strong>JetCompact</strong> com esse conjunto de opções pode retornar JET_errSuccess, mas não copiar todos os dados criados no banco de dado de origem. Os dados que estavam em partes danificadas do banco de dados de origem serão ignorados.</p> | 
| <p>JET_bitCompactStats</p> | <p>Faz com que o <strong>JetCompact</strong> despeje estatísticas no banco de dados de origem em um arquivo chamado DFRGINFO.TXT. As estatísticas incluem o nome de cada tabela no banco de dados de origem, o número de linhas em cada tabela, o tamanho total em bytes de todas as linhas em cada tabela, tamanho total em bytes de todas as colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> que foram grandes o suficiente para serem armazenados separados do registro, número de páginas de folha de índice clusterizado e número de páginas de folha de valor longo Além disso, estatísticas de resumo, incluindo o tamanho do banco de dados de origem, banco de dados de destino, tempo necessário para compactação de banco de dados, o espaço de banco de dados temporário também são todos despejados.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Um ponteiro <em>pconvert</em> não nulo foi fornecido, mas a versão do ESE que está sendo usada não oferece suporte ao recurso Convert. esse recurso foi removido na versão do Windows Server 2003 do ESE.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInTransaction</p> | <p>A sessão de chamada está dentro de uma transação. <strong>JetCompact</strong> deve ser chamado por uma sessão fora de qualquer transação.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, o banco de dados de origem é copiado no banco de dados de destino. O banco de dados de destino está em um estado ideal, por exemplo, todos os índices de tabela estão localizados em espaço em disco lógico adjacente. Cada página de índice é preenchida para o valor configurado quando os índices foram originalmente criados no banco de dados de origem. Todas as configurações de dados e metadados são copiadas com fidelidade total, a menos que a opção de reparo tenha sido especificada. Se a opção de reparo tiver sido especificada, alguns dados do banco de dado de origem podem não ter sido copiados.

Em caso de falha, o banco de dados de destino pode existir, mas não é uma cópia completa do banco de dados de origem.

#### <a name="remarks"></a>Comentários

A compactação de um banco de dados também é usada para atualizar um banco de dados de um formato de versão anterior para uma versão mais moderna. Um parâmetro opcional é *pconvert*, que contém uma estrutura que pode conter uma descrição para uma DLL de versão anterior a ser usada para ler o formato do banco de dados de origem. este recurso foi descontinuado no Windows Server 2003. após a Windows Server 2003, as novas versões do ESE sempre podem ler versões mais antigas do formato de banco de dados e, portanto, esse recurso não é necessário.

A densidade de dados desejada após uma operação de compactação é especificada quando tabelas e índices são criados. A densidade deve estar entre 20% e 100%. Se um banco de dados for basicamente lido e não atualizado, os aplicativos definirão a densidade como 100% para reduzir o número de operações de e/s durante o processamento da consulta. No entanto, se os dados forem atualizados com frequência com operações que aumentam o tamanho dos dados armazenados junto com o registro, ou se novos dados forem inseridos com frequência, o aplicativo escolherá uma densidade mais baixa para que as atualizações mais frequentemente encontrem os recursos necessários disponíveis. A operação de compactação do banco de dados faz com que o banco de dados seja idealmente disposto de acordo com o preenchimento escolhido pelo aplicativo.

A compactação de banco de dados é uma operação off-line. Ele não pode ser executado enquanto o banco de dados está em uso. Como resultado, normalmente é feito como parte de um processo de compilação do desenvolvimento de um aplicativo que fornece um conjunto de dados como parte de si mesmo.

A compactação de banco de dados offline toca em todos os bits de um banco e pode ser usada como um meio de verificar a consistência de um banco de dado. Se um banco de dados for suspeito, ele poderá ser compactado. Se nenhum erro for encontrado na compactação, será conhecido que o banco de dados esteja em um estado válido para o ESE.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCompactW</strong> (Unicode) e <strong>JetCompactA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetStopService](./jetstopservice-function.md)
