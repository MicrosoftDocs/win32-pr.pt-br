---
description: Os gravadores são aplicativos ou serviços que armazenam informações persistentes em arquivos em disco e que fornecem os nomes e locais desses arquivos para os solicitantes usando a interface de cópia de sombra.
ms.assetid: 24fc2d7c-f8d6-49ca-9bb5-0179bef68e78
title: Gravadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ca409e8dc6153a6b3e2b747dc23cc391055471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763142"
---
# <a name="writers"></a>Gravadores

Os [*gravadores*](vssgloss-w.md) são aplicativos ou serviços que armazenam informações persistentes em arquivos em disco e que fornecem os nomes e locais desses arquivos para os solicitantes usando a interface de cópia de sombra.

Durante as operações de backup, os gravadores asseguram que seus dados estejam inativos e estáveis – adequados para cópia de sombra e backup. Os gravadores colaboram com restaurações desbloqueando arquivos quando possível e indicando locais alternativos quando necessário.

Se nenhum gravador estiver presente durante uma operação de backup do VSS, uma cópia de sombra ainda poderá ser criada. Nesse caso, todos os dados no volume copiado por sombra estarão no [*estado consistente com falhas*](vssgloss-c.md).

## <a name="writer-state"></a>Estado do gravador

Os gravadores mantêm seu estado em um objeto de metadados baseado em XML, o [*documento de metadados do gravador*](vssgloss-w.md).

Esses metadados de gravador são a única estrutura de dados que contém o [*conjunto de arquivos*](vssgloss-f.md)— caminho, especificação de arquivo e sinalizador de recursão — dos dados a serem armazenados em backup e restaurados.

O documento de metadados do gravador organiza os conjuntos de arquivos do gravador em grupos ou [*componentes*](vssgloss-c.md). A relação de um desses componentes durante as operações de backup e restauração para os outros componentes gerenciados pelo gravador é descrita no documento de metadados do gravador pela seleção do componente [*para backup*](vssgloss-s.md), sua [*seleção para restauração*](vssgloss-s.md)e seus [*caminhos lógicos*](vssgloss-l.md). (Para obter mais informações, consulte [Configurando a organização do componente](definition-of-components-by-writers.md) e [trabalhando com a seleção e os caminhos lógicos](working-with-selectability-and-logical-paths.md).)

Informações adicionais que regem a restauração de arquivos e outros problemas também estão contidas neste documento.

O solicitante precisa dos metadados do gravador, em conjunto com seu próprio documento de componentes de backup, para processar um backup ou uma restauração.

Ao contrário do documento de componentes de backup, o documento de metadados do gravador deve ser considerado como uma estrutura somente leitura. Depois que um gravador o cria, o documento não é alterado.

## <a name="writer-event-handling"></a>Manipulação de eventos do gravador

As operações do VSS de um gravador são iniciadas por meio do recebimento de eventos COM.

Quando nenhum evento estiver presente, um gravador não executará operações do VSS (como um backup ou uma restauração VSS). Em vez disso, ele executa seu trabalho normal, como responder a consultas de banco de dados, gerenciar os dados do usuário ou fornecer outros serviços.

Para garantir que o tratamento de erros para várias sessões de backup e restauração paralelas seja executado corretamente e para garantir que uma sessão de backup ou restauração não corrompa outra, você deve fazer o seguinte:

-   Se o manipulador de eventos de um gravador (como [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)) chamar o método [**CVssWriterEx2:: GetSessionID**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid), [**CVssWriter:: SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure)ou [**CVssWriterEx2:: SetWriterFailureEx**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) , o manipulador de eventos deverá chamar o método no mesmo thread que chamou o manipulador de eventos.
-   A implementação do gravador de um manipulador de eventos, como o [**OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) , pode descarregar o trabalho em threads de trabalho, se desejado, desde que cada thread de trabalho realize o relatório de todos os relatórios de erros necessários de volta para o thread do manipulador de eventos original.

## <a name="handling-identify-events"></a>Tratamento de eventos de identificação

Com exceção do evento identify, o tipo e a ordem dos eventos que um gravador recebe dependem exclusivamente do tipo de operações do VSS que estão atualmente em andamento.

O evento de identificação requer que os gravadores forneçam as informações do sistema sobre sua configuração e os arquivos que eles gerenciam por meio de seu [*documento de metadados do gravador*](vssgloss-w.md). Um evento de identificação é gerado no suporte de quase qualquer operação do VSS, incluindo consultas do sistema, bem como operações de cópia de sombra e backup e restauração. Portanto, qualquer implementação do gravador do manipulador de eventos de identificação [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) deve ser capaz de lidar com um evento de identificação a qualquer momento, incluindo no meio do processamento de outra operação VSS, como um backup ou uma restauração. Um evento de identificação nunca deve ser considerado como parte do ciclo de vida de uma operação VSS, embora sua geração seja esperada e necessária antes do início dessa operação.

É particularmente importante que as informações de estado sobre uma operação do VSS não sejam modificadas em [**CVssWriter:: Onidentification**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), pois o recebimento de um evento fora de ordem redefiniria essas informações.

## <a name="backup-and-restore-events"></a>Eventos de backup e restauração

Dependendo se estiver participando de um backup ou uma restauração, um gravador receberá entre dois e sete eventos, além de um evento de identificação inicial.

Lidar com esses eventos constitui (do ponto de vista de um gravador) o ciclo de vida de uma operação de backup ou restauração.

Em uma operação de backup típica (consulte [visão geral do processamento de um backup no VSS](overview-of-processing-a-backup-under-vss.md)), um gravador trataria os seguintes eventos (além de um evento de identificação inicial):

-   PrepareForBackup
-   PrepareForSnapshot
-   Congelamento
-   Descongelar
-   Pós-instantâneo
-   BackupComplete
-   BackupShutdown

Em uma operação de restauração típica (consulte [visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md)), um gravador trataria os seguintes eventos:

-   Prerestore
-   Restauração

 

 



