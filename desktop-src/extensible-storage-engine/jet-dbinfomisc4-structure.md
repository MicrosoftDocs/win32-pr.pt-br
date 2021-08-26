---
description: 'Saiba mais sobre: estrutura de JET_DBINFOMISC4'
title: Estrutura JET_DBINFOMISC4
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
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
ms.openlocfilehash: d52697bfc67b6eafa69c3d284be087527ca73275a03f5d9b98e6b88cb2de6bd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017190"
---
# <a name="jet_dbinfomisc4-structure"></a>Estrutura JET_DBINFOMISC4


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_dbinfomisc4-structure"></a>Estrutura JET_DBINFOMISC4

A estrutura de **JET_DBINFOMISC4** contém informações diversas sobre um banco de dados. Essas são as informações contidas no cabeçalho do banco de dados.

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
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
```

### <a name="members"></a>Membros

**ulVersion**

A versão nativa do mecanismo de banco de dados que criou o banco de dados. Consulte [JetGetVersion](./jetgetversion-function.md) para recuperar a versão nativa para o mecanismo de banco de dados atual.

**ulUpdate**

Rastreia atualizações de formato de banco de dados incremental que são compatíveis com versões anteriores.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ulVersion, ulUpdate =</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x620, 0</p></td>
<td><p>Formato beta do sistema operacional original (4/22/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 1</p></td>
<td><p>Adicione colunas no catálogo para indexação condicional e antigo (5/29/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Adicione o sinalizador fLocalizedText no IDB (6/5/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Adicione SPLIT_BUFFER às páginas raiz da árvore de espaço (10/30/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Reverta a revisão para que ESE97 permaneça compatível com o encaminhamento (1/28/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Adicione novas colunas marcadas ao catálogo ( &quot; CallbackData &quot; e &quot; CallbackDependencies &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 4</p></td>
<td><p>Suporte a SLV: signSLV, fSLVExists no cabeçalho do BD (5/5/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 5</p></td>
<td><p>Nova árvore de espaço do SLV (5/29/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 6</p></td>
<td><p>Mapa de espaço do SLV (10/12/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 7</p></td>
<td><p>IDXSEG de 4 bytes (12/10/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 8</p></td>
<td><p>Novo formato de coluna de modelo (1/25/99).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 9</p></td>
<td><p>Colunas de modelo classificadas (6/24/99).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, um</p></td>
<td><p>Base de código mesclado (3/26/2003).</p></td>
</tr>
<tr class="even">
<td><p>0x620, B</p></td>
<td><p>Novo formato de soma de verificação (1/08/2004).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, C</p></td>
<td><p>Maior comprimento de chave máximo de 1000/2000 bytes para páginas de 4/8 KB (1/15/2004).</p></td>
</tr>
<tr class="even">
<td><p>0x620, D</p></td>
<td><p>Dicas de espaço de catálogo, space_header. v2 (7/15/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, E</p></td>
<td><p>Adicionar novo formato de nó/extensão ao Gerenciador de espaço, use-o para pools reservados de espaço (8/9/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, F</p></td>
<td><p>Compactação para valores longos intrínsecos (10/30/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 10</p></td>
<td><p>Compactação para valores longos separados (12/05/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 11</p></td>
<td><p>Novo tamanho de bloco LV para páginas grandes (12/29/2007).</p></td>
</tr>
</tbody>
</table>


**signDb**

Assinatura do banco de dados (incluindo a hora de criação). Essa estrutura é de 28 bytes.

**dbstate**

Esse é o estado do banco de dados.

As opções a seguir estão disponíveis para este membro.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_dbstateJustCreated<br />
1</p></td>
<td><p>O banco de dados acabou de ser criado.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateDirtyShutdown<br />
2</p></td>
<td><p>O banco de dados requer a execução de recuperação rígida ou flexível para tornar-se utilizável ou móvel. Um não deve tentar mover bancos de dados nesse estado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>O banco de dados está em um estado limpo. O banco de dados pode ser anexado sem nenhum arquivo de log.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateBeingConverted<br />
4</p></td>
<td><p>O banco de dados está sendo atualizado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateForceDetach<br />
5</p></td>
<td><p>Interno.</p></td>
</tr>
</tbody>
</table>


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

Dá suporte à infraestrutura de ESE e não pode ser usado em seu código.

**fShadowingDisabled**

Dá suporte à infraestrutura de ESE e não pode ser usado em seu código.

**fUpgradeDb**

Dá suporte à infraestrutura de ESE e não pode ser usado em seu código.

**dwMajorVersion**

Representa os Windows NT de versão quando os índices de bancos de dados foram atualizados. Usado para atualizar índices.

**dwMinorVersion**

Representa os Windows NT de versão quando os índices de bancos de dados foram atualizados. Usado para atualizar índices.

**dwBuildNumber**

Representa os Windows NT de versão quando os índices de bancos de dados foram atualizados. Usado para atualizar índices.

**lSPNumber**

Representa os Windows NT de versão quando os índices de bancos de dados foram atualizados. Usado para atualizar índices.

**cbPageSize**

Tamanho da página do banco de dados. 0 significa que o tamanho da página é de 4 KB.

Esse valor será recuperado somente se JET_DbInfoMisc foi passado para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).

**genMinRequired**

Representa a geração mínima de log necessária para repetir os logs. Normalmente, isso é usado como a geração de ponto de verificação.

**genMaxRequired**

Representa a geração máxima de log necessária para repetir os logs.

**logtimeGenMaxCreate**

Representa a data e a hora de criação do arquivo de log genMax.

**ulRepairCount**

O número de vezes que um reparo foi chamado neste banco de dados.

**logtimeRepair**

Representa a data e a hora em que o último reparo foi executado.

**ulRepairCountOld**

O número de vezes que o reparo foi executado nesse banco de dados antes da última desfragmentação.

**ulECCFixSuccess**

O número de vezes que um erro de um bit foi corrigido e resultou em uma boa página.

**logtimeECCFixSuccess**

Representa a data e a hora em que o último erro de um bit foi corrigido e resultou em uma boa página.

**ulECCFixSuccessOld**

Representa o número de vezes que um erro de um bit foi corrigido e resultou em uma boa página antes do último reparo.

**ulECCFixFail**

O número de vezes que um erro de um bit foi corrigido e resultou em uma página ruim.

**logtimeECCFixFail**

Representa a data e a hora em que o último erro de um bit foi corrigido e resultou em uma página ruim.

**ulECCFixFailOld**

O número de vezes que um erro de um bit foi corrigido e resultou em uma página ruim antes do último reparo.

**ulBadChecksum**

O número de vezes que um erro de ECC/checksum não corretamente foi encontrado.

**logtimeBadChecksum**

Representa a data e a hora em que o último erro de ECC/checksum não corrigida foi encontrado.

**ulBadChecksumOld**

O número de vezes que um erro de ECC/checksum não corretamente foi encontrado antes do último reparo.

**genCommitted**

O número máximo de gerações de log comprometidas com o banco de dados. Normalmente, a geração de log atual.

**bkinfoCopyPrev**

O último backup de Cópia bem-sucedido.

**bkinfoDiffPrev**

O último backup diferencial bem-sucedido. Esse valor é redefinido quando bkinfoFullPrev é definido.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
