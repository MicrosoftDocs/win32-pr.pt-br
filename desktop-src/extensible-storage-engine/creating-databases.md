---
description: 'Saiba mais sobre: Criando bancos de dados'
title: Criando bancos de dados
TOCTitle: Creating Databases
ms:assetid: d221144d-f777-4f8a-80ca-2ebdb77108dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294100(v=EXCHG.10)
ms:contentKeyID: 32765715
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eac708b64837fc79fa8a5060df7deb93ec552e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791437"
---
# <a name="creating-databases"></a>Criando bancos de dados


_**Aplica-se a:** Windows | Windows Server_

## <a name="creating-databases"></a>Criando bancos de dados

O banco de dados do ESE consiste em uma ou mais tabelas que organizam os dados por colunas e linhas. O banco de dados ESE é identificado por nome e ID do banco de dados. Um banco de dados ESE é semelhante a um único arquivo para o sistema operacional Microsoft Windows; no entanto, internamente, o banco de dados é armazenado como uma coleção de páginas. Essas páginas contêm metadados que descrevem os dados no banco de dados, os mesmos e um ou mais índices que armazenam diferentes ordens dos dados. O banco de dados pode conter até 2 ^ 31 páginas ou 16 terabytes de dados para um banco de dado com 8 KB de páginas.

O aplicativo cria uma instância do mecanismo de banco de dados e, em seguida, cria um banco de dados e anexa-o à instância. Até 6 bancos de dados podem ser anexados simultaneamente a uma instância com [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetAttachDatabase](./jetattachdatabase-function.md). Uma ou mais sessões devem ser iniciadas no banco de dados, pois todas as operações do ESE subsequentes são executadas no contexto de uma sessão. Uma sessão separada deve ser aberta para cada thread usando o ESE.

Este procedimento inicializará o ESE e criará um banco de dados.

### <a name="to-initialize-ese-and-create-a-database"></a>Para inicializar o ESE e criar um banco de dados

1.  [JetCreateInstance](./jetcreateinstance-function.md): cria uma instância do mecanismo de banco de dados.
    
    **Windows XP e posterior:** Essa função está disponível no Windows XP e versões posteriores. No Windows 2000, há suporte apenas para uma instância e essa instância é criada implicitamente

2.  [JetSetSystemParameter](./jetsetsystemparameter-function.md): os parâmetros do sistema que afetam o layout físico, como o JET_paramLogFilePath e JET_paramSystemPath devem ser definidos antes de inicializar a instância com [JetInit](./jetinit-function.md). Os parâmetros definidos neste estágio são definidos para todos os bancos de dados criados na instância. [JetSetSystemParameter](./jetsetsystemparameter-function.md) é a única função que pode usar a instância antes de ser inicializada com [JetInit](./jetinit-function.md).

3.  [JetInit](./jetinit-function.md): Inicializa a instância. A instância deve ser inicializada com [JetInit](./jetinit-function.md) antes que possa ser usada com outras funções.

4.  [JetBeginSession](./jetbeginsession-function.md): cria a sessão para todas as transações subsequentes. Todas as transações de banco de dados ocorrem no contexto da sessão ([JET_SESID](./jet-sesid.md)).

5.  [JetCreateDatabase](./jetcreatedatabase-function.md): cria o banco de dados e retorna um identificador para a ID do banco de dados ([JET_DBID](./jet-dbid.md)).
    
    Se o banco de dados já existir, a etapa 5 acima será substituída pelas duas etapas a seguir:
    
    1.  [JetAttachDatabase](./jetattachdatabase-function.md): anexa o banco de dados pelo nome à sessão
    
    2.  [JetOpenDatabase](./jetopendatabase-function.md): retorna a ID do banco de dados que é usada em operações de banco de dados subsequentes.

Um banco de dados pode ser desanexado de uma instância do ESE usando [JetDetachDatabase](./jetdetachdatabase-function.md) e posterior anexado a outra instância com [JetAttachDatabase](./jetattachdatabase-function.md). Quando o banco de dados é desanexado, ele pode ser copiado como um único arquivo usando utilitários padrão do Windows. No entanto, quando o banco de dados é anexado a uma instância ESE, ele não pode ser copiado porque o ESE abre exclusivamente os arquivos de banco de dados. Além disso, se a instância falhar, o arquivo de banco de dados não poderá ser copiado sozinho porque precisa que os arquivos de log de transações associados a ele se recuperem dessa falha.
