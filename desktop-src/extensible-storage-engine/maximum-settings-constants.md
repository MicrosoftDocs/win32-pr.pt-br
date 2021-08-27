---
description: 'Saiba mais sobre: Constantes de Configurações máximas'
title: Constantes Configurações máximo
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: fa6ff7044dcd43e4b51c801784d29955f3d34a15
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982219"
---
# <a name="maximum-settings-constants"></a>Constantes Configurações máximo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="maximum-settings-constants"></a>Constantes Configurações máximo

Essas constantes fornecem as configurações máximas permitidas em itens em um banco de dados ESE.


| <p>Constante/valor</p> | <p>Descrição</p> | 
|-----------------------|--------------------|
| <p>JET_BASE_NAME_LENGTH<br />3</p> | <p>Define o comprimento do prefixo usado para nomear arquivos usados pelo mecanismo de banco de dados. Esse comprimento é aplicável ao nome definido para o parâmetro <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> sistema.</p> | 
| <p>JET_MAX_COMPUTERNAME_LENGTH<br />15</p> | <p>Define o comprimento máximo para <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p> | 
| <p>JET_cbBookmarkMost<br />256</p> | <p>O tamanho máximo padrão de um indicador. Isso é válido quando o tamanho da chave é deixado em seu valor padrão.</p> | 
| <p>JET_cbBookmarkMostMost<br />2000</p> | <p>O tamanho máximo de um indicador quando esent está configurado para ter as maiores chaves possíveis.</p><p><strong>Windows 7:</strong> JET_cbBookmarkMostMost é introduzido no Windows 7.</p> | 
| <p>JET_cbNameMost<br />64</p> | <p>O comprimento máximo de um objeto, coluna, índice ou nome da propriedade.</p><p><strong>Observação</strong>  Se Unicode, o valor será 128.</p> | 
| <p>JET_cbFullNameMost<br />255</p> | <p>O comprimento máximo de um "name.name.name..." Construir.</p><p><strong>Observação</strong>  Se Unicode, o valor será 510.</p> | 
| <p>JET_cbColumnLVPageOverhead<br />82</p> | <p>Esse número pode ser usado para calcular a quantidade máxima de um BLOB que pode ser armazenada pelo mecanismo de banco de dados em uma única página de banco de dados. A fórmula é max size = JET_paramDatabasePageSize-JET_cbColumnLVPageOverhead.</p><p>Esse valor agora está obsoleto. O tamanho da parte de valor longo deve ser recuperado com o parâmetro JET_paramLVChunkSizeMost valor.</p> | 
| <p>JET_cbColumnMost<br />255</p> | <p>O tamanho máximo de dados de coluna de valor não longo.</p> | 
| <p>JET_cbLVDefaultValueMost<br />255</p> | <p>O tamanho máximo de um valor longo (LongBinary ou LongText) valor padrão da coluna.</p> | 
| <p>JET_cbKeyMost<br />255</p> | <p>O tamanho máximo padrão de uma chave de classificação ou índice.</p> | 
| <p>JET_cbKeyMostMost<br />2000</p> | <p>O tamanho máximo configurável de uma chave de classificação ou índice para qualquer tamanho de página. (Consulte JET_INDEXCREATE2.cbKeyMost)</p><p><strong>Windows 7:</strong> JET_cbKeyMostMost é introduzido no sistema operacional Windows 7.</p> | 
| <p>JET_cbKeyMost2KBytePage<br />500</p> | <p>O tamanho máximo configurável máximo permitida para uma chave de índice em um banco de dados usando páginas de 2048 byte. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage é introduzido no sistema operacional Windows Vista.</p> | 
| <p>JET_cbKeyMost4KBytePage<br />1000</p> | <p>O tamanho máximo configurável máximo permitida para uma chave de índice em um banco de dados usando páginas de 4096 byte. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage é introduzido no Windows Vista.</p> | 
| <p>JET_cbKeyMost8KBytePage<br />2000</p> | <p>O tamanho máximo configurável máximo permitida para uma chave de índice em um banco de dados usando páginas de 8192 byte. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</p><p><strong>Windows Vista:</strong> JET_cbKeyMost8KBytePage é introduzido no Windows Vista</p> | 
| <p>JET_cbKeyMostMin<br />255</p> | <p>O tamanho máximo mínimo permitida para uma chave de índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</p><p><strong>Windows Vista:</strong> JET_cbKeyMostMin é introduzido no Windows Vista.</p> | 
| <p>JET_cbLimitKeyMost<br />256</p> | <p>O tamanho máximo da chave quando a chave é formada usando um <em>grbit</em>de limite, como JET_bitStrLimit, que é usado na <a href="gg269329(v=exchg.10).md">função JetMakeKey.</a></p> | 
| <p>JET_cbPrimaryKeyMost<br />255</p> | <p>O tamanho máximo do índice primário. Agora, isso está obsoleto.</p> | 
| <p>JET_cbSecondaryKeyMost<br />255</p> | <p>O tamanho máximo do índice secundário. Agora, isso está obsoleto.</p> | 
| <p>JET_ccolKeyMost<br />12</p> | <p>O número máximo de componentes em uma chave de classificação ou índice.</p><p><strong>Windows Vista:</strong> No Windows Vista e versões posteriores Windows o valor é 16.</p> | 
| <p>JET_ccolMost<br />0x0000fee0</p> | <p>O número máximo de colunas permitidas em uma tabela.</p><p><strong>Windows XP:</strong> O valor 0x0000fee0 é usado no Windows XP e versões posteriores e posteriores do Windows</p><p><strong>Windows 2000:</strong> O valor 0x00007ffe é usado no Windows 2000.</p> | 
| <p>JET_ccolFixedMost<br />0x0000007f</p> | <p>O número máximo de colunas fixas permitidas em uma tabela, atualmente 127.</p> | 
| <p>JET_ccolVarMost<br />0x00000080</p> | <p>O número máximo de colunas de comprimento variável que podem ser contidas em uma tabela, atualmente 128.</p> | 
| <p>JET_ccolTaggedMost<br />( JET_ccolMost - 0x000000ff )</p> | <p>O número máximo de colunas marcadas que podem ser contidas em uma tabela, atualmente 64993.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 


