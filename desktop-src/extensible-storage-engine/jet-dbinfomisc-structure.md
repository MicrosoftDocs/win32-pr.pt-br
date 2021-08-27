---
description: 'Saiba mais sobre: estrutura de JET_DBINFOMISC'
title: Estrutura JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7d7861e558bbf6a1938d252a52e7bb781068a331
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476862"
---
# <a name="jet_dbinfomisc-structure"></a>Estrutura JET_DBINFOMISC


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_dbinfomisc-structure"></a>Estrutura JET_DBINFOMISC

A estrutura de **JET_DBINFOMISC** contém informações diversas sobre um banco de dados. Essas são as informações contidas no cabeçalho do banco de dados.

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
    } JET_DBINFOMISC;
```

### <a name="members"></a>Membros

**ulVersion**

A versão nativa do mecanismo de banco de dados que criou o banco de dados. Consulte [JetGetVersion](./jetgetversion-function.md) para recuperar a versão nativa para o mecanismo de banco de dados atual.

**ulUpdate**

Rastreia atualizações de formato de banco de dados incremental que são compatíveis com versões anteriores.


| <p>ulVersion, ulUpdate =</p> | <p>Significado</p> | 
|------------------------------|----------------|
| <p>0x620, 0</p> | <p>Formato beta do sistema operacional original (4/22/97).</p> | 
| <p>0x620, 1</p> | <p>Adicione colunas no catálogo para indexação condicional e antigo (5/29/97).</p> | 
| <p>0x620, 2</p> | <p>Adicione o sinalizador fLocalizedText no IDB (6/5/97).</p> | 
| <p>0x620, 3</p> | <p>Adicione SPLIT_BUFFER às páginas raiz da árvore de espaço (10/30/97).</p> | 
| <p>0x620, 2</p> | <p>Reverta a revisão para que ESE97 permaneça compatível com o encaminhamento (1/28/98).</p> | 
| <p>0x620, 3</p> | <p>Adicione novas colunas marcadas ao catálogo ("CallbackData" e "CallbackDependencies").</p> | 
| <p>0x620, 4</p> | <p>Suporte a SLV: signSLV, fSLVExists no cabeçalho do BD (5/5/98).</p> | 
| <p>0x620, 5</p> | <p>Nova árvore de espaço do SLV (5/29/98).</p> | 
| <p>0x620, 6</p> | <p>Mapa de espaço do SLV (10/12/98).</p> | 
| <p>0x620, 7</p> | <p>IDXSEG de 4 bytes (12/10/98).</p> | 
| <p>0x620, 8</p> | <p>Novo formato de coluna de modelo (1/25/99).</p> | 
| <p>0x620, 9</p> | <p>Colunas de modelo classificadas (6/24/99).</p> | 
| <p>0x623, 0</p> | <p>Novo Gerenciador de espaço (5/15/99).</p> | 



**signDb**

Assinatura do banco de dados (incluindo a hora de criação). Essa estrutura é de 28 bytes.

**dbstate**

Esse é o estado do banco de dados.

As opções a seguir estão disponíveis para este membro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_dbstateJustCreated<br />1</p> | <p>O banco de dados acabou de ser criado.</p> | 
| <p>JET_dbstateDirtyShutdown<br />2</p> | <p>O banco de dados requer a execução de recuperação rígida ou flexível para tornar-se utilizável ou móvel. Um não deve tentar mover bancos de dados nesse estado.</p> | 
| <p>JET_dbstateCleanShutdown<br />3</p> | <p>O banco de dados está em um estado limpo. O banco de dados pode ser anexado sem nenhum arquivo de log.</p> | 
| <p>JET_dbstateBeingConverted<br />4</p> | <p>O banco de dados está sendo atualizado.</p> | 
| <p>JET_dbstateForceDetach<br />5</p> | <p>Interno.</p> | 



**lgposConsistent**

NULL se o banco de dados estiver em um estado sujo. Esta é a posição de log que foi usada quando o banco de dados foi trazido pela última vez para um estado de desligamento normal.

**logtimeConsistent**

NULL se o banco de dados estiver em um estado sujo. Essa é a hora em que o banco de dados foi trazido pela última vez para um estado de desligamento normal.

**logtimeAttach**

A hora em que o banco de dados foi anexado pela última vez com [JetAttachDatabase](./jetattachdatabase-function.md).

**lgposAttach**

A posição do log que foi usada na última vez em que o banco de dados foi anexado com [JetAttachDatabase](./jetattachdatabase-function.md).

**logtimeDetach**

A hora em que o banco de dados foi desanexado pela última vez com [JetDetachDatabase](./jetdetachdatabase-function.md).

**lgposDetach**

A posição do log que foi usada na última vez em que o banco de dados foi desanexado com [JetDetachDatabase](./jetdetachdatabase-function.md).

**signLog**

Dá suporte à infraestrutura ESE e não pode ser usada em seu código.

**bkinfoFullPrev**

Dá suporte à infraestrutura ESE e não pode ser usada em seu código.

**bkinfoIncPrev**

Dá suporte à infraestrutura ESE e não pode ser usada em seu código.

**bkinfoFullCur**

Dá suporte à infraestrutura ESE e não pode ser usada em seu código.

**fShadowingDisabled**

Dá suporte à infraestrutura ESE e não pode ser usada em seu código.

**fUpgradeDb**

Dá suporte à infraestrutura ESE e não pode ser usada em seu código.

**dwMajorVersion**

representa os números de versão de Windows NT quando os índices de bancos de dados foram atualizados. Usado para atualizar índices.

**dwMinorVersion**

representa os números de versão de Windows NT quando os índices de bancos de dados foram atualizados. Usado para atualizar índices.

**dwBuildNumber**

representa os números de versão de Windows NT quando os índices de bancos de dados foram atualizados. Usado para atualizar índices.

**lSPNumber**

representa os números de versão de Windows NT quando os índices de bancos de dados foram atualizados. Usado para atualizar índices.

**cbPageSize**

Tamanho da página do banco de dados. 0 significa que o tamanho da página é de 4 KB.

Esse valor será recuperado somente se JET_DbInfoMisc foi passado para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
