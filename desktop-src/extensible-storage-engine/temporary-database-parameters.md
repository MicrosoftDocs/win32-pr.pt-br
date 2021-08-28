---
description: 'Saiba mais sobre: parâmetros de banco de dados temporários'
title: Parâmetros de banco de dados temporários
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: 427ed51c2757075ccb28fd70e5554c49dc8db4e8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986819"
---
# <a name="temporary-database-parameters"></a>Parâmetros de banco de dados temporários


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="temporary-database-parameters"></a>Parâmetros de banco de dados temporários

Este tópico contém parâmetros que são usados para o banco de dados temporário.

*JET_paramEnableTempTableVersioning*  
46  

Esse parâmetro controla o uso de transações em tabelas temporárias. Quando esse parâmetro for false, as tabelas temporárias serão mais rápidas, mas não será possível reverter as atualizações feitas em uma transação.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>True</p> | 
| <p>Tipo:</p> | <p>Booliano</p> | 
| <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Sim</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramPageTempDBMin*  
19  

Esse parâmetro controla o tamanho inicial do banco de dados temporário. O tamanho está em páginas de banco de dados. Um tamanho de zero indica que o tamanho padrão de um banco de dados comum deve ser usado.

Geralmente, é desejável que aplicativos pequenos configurem o banco de dados temporário para que seja o menor possível. Definir esse parâmetro como 14 atingirá o menor banco de dados temporário possível. Observe que também é possível eliminar totalmente o banco de dados temporário definindo **JET_paramMaxTemporaryTables** como zero.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>0</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Sim</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramTempPath*  
1  

Esse parâmetro indica o caminho relativo ou absoluto do sistema de arquivos da pasta ou do arquivo que conterá o banco de dados temporário para a instância. Se o caminho for para uma pasta que conterá o banco de dados temporário, ele deverá ser encerrado com um caractere de barra invertida. O banco de dados temporário é usado para manter dado volátil que é gerado no processo de tratamento de chamadas de informações da API do ESE, criação de índices ou armazenamento do conteúdo de uma tabela temporária.

**Observação**  Se um caminho relativo for especificado, ele será relativo ao diretório de trabalho atual do processo que hospeda o aplicativo que está usando o mecanismo de banco de dados.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>"tmp. edb"</p> | 
| <p>Tipo:</p> | <p>Caminho (cadeia de caracteres)</p> | 
| <p>Intervalo válido:</p> | <p>0 a 247 caracteres</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Sim</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[Arquivos extensíveis Armazenamento mecanismo](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
