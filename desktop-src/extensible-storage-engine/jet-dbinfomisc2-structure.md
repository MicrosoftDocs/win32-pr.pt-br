---
description: 'Saiba mais sobre: estrutura JET_DBINFOMISC2 dados'
title: Estrutura JET_DBINFOMISC2
TOCTitle: JET_DBINFOMISC2 Structure
ms:assetid: c62e87ca-c02c-4d6f-a1e6-f80d022c6aad
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294085(v=EXCHG.10)
ms:contentKeyID: 32765700
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2b42433df5a2712061c1c88ce2d0ad8afbabc3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480492"
---
# <a name="jet_dbinfomisc2-structure"></a>Estrutura JET_DBINFOMISC2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_dbinfomisc2-structure"></a>Estrutura JET_DBINFOMISC2

A **estrutura JET_DBINFOMISC2** contém informações diversas sobre um banco de dados. Essas são as informações contidas no header do banco de dados.

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
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
    } JET_DBINFOMISC2;
```

### <a name="members"></a>Membros

**ulVersion**

A versão nativa do mecanismo de banco de dados que criou o banco de dados. Consulte [JetGetVersion para](./jetgetversion-function.md) recuperar a versão nativa do mecanismo de banco de dados atual.

**ulUpdate**

Rastreia atualizações incrementais de formato de banco de dados compatíveis com versões anteriores.


| <p>ulVersion, ulUpdate =</p> | <p>Significado</p> | 
|------------------------------|----------------|
| <p>0x620,0</p> | <p>Formato Beta do sistema operacional original (22/4/97).</p> | 
| <p>0x620,1</p> | <p>Adicione colunas no catálogo para indexação condicional e OLD (29/5/97).</p> | 
| <p>0x620,2</p> | <p>Adicione o sinalizador fLocalizedText no IDB (6/5/97).</p> | 
| <p>0x620,3</p> | <p>Adicione SPLIT_BUFFER páginas raiz da árvore de espaço (30/10/97).</p> | 
| <p>0x620,2</p> | <p>Reverter a revisão para que o ESE97 permaneça compatível com o encaminhamento (28/1/98).</p> | 
| <p>0x620,3</p> | <p>Adicione novas colunas marcadas ao catálogo ("CallbackData" e "CallbackDependencies").</p> | 
| <p>0x620,4</p> | <p>Suporte a SLV: signSLV, fSLVExists no header do banco de dados (5/5/98).</p> | 
| <p>0x620,5</p> | <p>Nova árvore de espaço SLV (29/5/98).</p> | 
| <p>0x620,6</p> | <p>Mapa de espaço SLV (12/10/98).</p> | 
| <p>0x620,7</p> | <p>IDXSEG de 4 byte (12/10/98).</p> | 
| <p>0x620,8</p> | <p>Novo formato de coluna de modelo (25/1/99).</p> | 
| <p>0x620,9</p> | <p>Colunas de modelo classificação (24/06/99).</p> | 
| <p>0x620, A</p> | <p>Base de código mesclada (26/3/2003).</p> | 
| <p>0x620,B</p> | <p>Novo formato de verificação (08/01/2004).</p> | 
| <p>0x620,C</p> | <p>Aumento do comprimento máximo da chave para 1000/2000 bytes para páginas de 4/8kb (15/1/2004).</p> | 
| <p>0x620, D</p> | <p>Dicas de espaço do catálogo, space_header.v2 (15/07/2007).</p> | 
| <p>0x620,E</p> | <p>Adicione novo formato de nó/extensão ao gerenciador de espaços, use-o para pools reservados de espaço (8/9/2007).</p> | 
| <p>0x620,F</p> | <p>Compactação para valores longos intrínsecos (30/10/2007).</p> | 
| <p>0x620,10</p> | <p>Compactação para valores longos separados (05/12/2007).</p> | 
| <p>0x620,11</p> | <p>Novo tamanho da parte LV para páginas grandes (29/12/2007).</p> | 



**signDb**

Assinatura do banco de dados (incluindo a hora de criação). Essa estrutura é de 28 bytes.

**dbstate**

Esse é o estado do banco de dados.

As opções a seguir estão disponíveis para esse membro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_dbstateJustCreated<br />1</p> | <p>O banco de dados acabou de ser criado.</p> | 
| <p>JET_dbstateDirtyShutdown<br />2</p> | <p>O banco de dados requer que a recuperação lenta ou lenta seja executado para se tornar acessível ou movêvel. Não se deve tentar mover bancos de dados nesse estado.</p> | 
| <p>JET_dbstateCleanShutdown<br />3</p> | <p>O banco de dados está em um estado limpo. O banco de dados pode ser anexado sem nenhum arquivo de log.</p> | 
| <p>JET_dbstateBeingConverted<br />4</p> | <p>O banco de dados está sendo atualizado.</p> | 
| <p>JET_dbstateForceDetach<br />5</p> | <p>Interno.</p> | 



**lgposConsistent**

Nulo se o banco de dados estiver em um estado sujo. Essa é a posição de log que foi usada quando o banco de dados foi colocado pela última vez em um estado de desligamento limpo.

**logtimeConsistent**

Nulo se o banco de dados estiver em um estado sujo. Esta é a hora em que o banco de dados foi levado pela última vez para um estado de desligamento limpo.

**logtimeAttach**

A hora em que o banco de dados foi anexado pela última vez com [JetAttachDatabase.](./jetattachdatabase-function.md)

**lgposAttach**

A posição de log que foi usada na última vez em que o banco de dados foi anexado com [JetAttachDatabase.](./jetattachdatabase-function.md)

**logtimeDetach**

A hora em que o banco de dados foi desaixado pela [última vez com JetDetachDatabase.](./jetdetachdatabase-function.md)

**lgposDetach**

A posição de log que foi usada na última vez em que o banco de dados foi detached com [JetDetachDatabase](./jetdetachdatabase-function.md).

**signLog**

Dá suporte à infraestrutura de ESE e não pode ser usado em seu código.

**bkinfoFullPrev**

Dá suporte à infraestrutura de ESE e não pode ser usado em seu código.

**bkinfoIncPrev**

Dá suporte à infraestrutura de ESE e não pode ser usado em seu código.

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

**genMinRequired**

Representa a geração de log mínima necessária para repetir os logs. Normalmente, isso é usado como a geração de ponto de verificação.

**genMaxRequired**

Representa a geração de log máxima necessária para repetir os logs.

**logtimeGenMaxCreate**

Representa a data e a hora de criação do arquivo de log genMax.

**ulRepairCount**

O número de vezes que um reparo foi chamado neste banco de dados.

**logtimeRepair**

Representa a data e a hora em que o último reparo foi executado.

**ulRepairCountOld**

O número de vezes que o reparo foi executado neste banco de dados antes da última desfragmentação.

**ulECCFixSuccess**

O número de vezes que um erro de um bit foi corrigido e resultou em uma boa página.

**logtimeECCFixSuccess**

Representa a data e a hora em que o último erro de um bit foi corrigido e resultou em uma boa página.

**ulECCFixSuccessOld**

Representa o número de vezes que um erro de um bit foi corrigido e resultou em uma boa página antes do último reparo.

**ulECCFixFail**

O número de vezes que um erro de um bit foi corrigido e resultou em uma página inadequada.

**logtimeECCFixFail**

Representa a data e a hora em que o último erro de um bit foi corrigido e resultou em uma página inadequada.

**ulECCFixFailOld**

O número de vezes que um erro de um bit foi corrigido e resultou em uma página inapropriada antes do último reparo.

**ulBadChecksum**

O número de vezes que um erro ECC não corrigível/checksum foi encontrado.

**logtimeBadChecksum**

Representa a data e a hora em que o último erro não corrigível de ECC/checksum foi encontrado.

**ulBadChecksumOld**

O número de vezes que um erro ECC não corrigível/checksum foi encontrado antes do último reparo.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
