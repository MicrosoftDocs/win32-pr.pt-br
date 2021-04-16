---
description: Há determinadas circunstâncias em que os arquivos cujo backup será feito não são o local padrão para esses arquivos.
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: Trabalhando com caminhos alternativos durante o backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98e93af4d12b804032a64841542e731ff77e048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794548"
---
# <a name="working-with-alternate-paths-during-backup"></a>Trabalhando com caminhos alternativos durante o backup

Há determinadas circunstâncias em que os arquivos cujo backup será feito não são o local padrão para esses arquivos.

Por exemplo, alguns gravadores não podem garantir a liberação de seus dados dentro da janela de tempo entre [*congelar*](vssgloss-f.md) e [*descongelar*](vssgloss-t.md) eventos. Esses gravadores podem optar por gerar arquivos duplicados contendo uma última configuração válida em um diretório de origem não padrão ou um [*caminho alternativo*](vssgloss-a.md).

O termo caminho alternativo, conforme usado com o VSS, não deve ser confundido com o termo [*mapeamento de local alternativo*](vssgloss-a.md). Os caminhos alternativos são usados somente durante as operações de backup e se referem a uma fonte alternativa da qual fazer backup. Mapeamentos de local alternativos são usados somente durante operações de restauração e se referem a um destino alternativo para operações de restauração.

**Para usar um caminho alternativo durante o backup**

1.  Durante a fase de descoberta de uma operação de backup (consulte [visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md)), um solicitante examinará os dados do componente de cada gravador usando [**IVssExamineWriterMetadata:: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) e obter instâncias da interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .
2.  Em seguida, um solicitante Obtém o [*conjunto de arquivos*](vssgloss-f.md) gerenciado por cada componente, representado por instâncias da interface [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) , chamando o método [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) .
3.  Além de um caminho ([**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), uma especificação de arquivo ([**IVssWMFiledesc:: filespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)) e um sinalizador de recursão ([**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)), um objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) pode conter um local alternativo (usado como um caminho alternativo para operações de backup e um mapeamento de local alternativo para operações de restauração) usando o método [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) .
4.  Se o valor retornado por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) for não nulo, os aplicativos de backup usarão esse valor em vez do valor obtido de [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) para selecionar e localizar os arquivos para fazer backup.
5.  Apesar de usar um caminho alternativo, os solicitantes ainda devem respeitar a especificação do arquivo e as configurações recursivas retornadas por [**IVssWMFiledesc:: filespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) e [**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive).

Observe que na restauração, qualquer caminho alternativo, ou seja, um local alternativo retornado por uma instância de [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) Obtida de uma instância de [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)que, por sua vez, foi obtido de uma instância do [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtidos recuperando um documento de metadados do gravador armazenado — não é usado durante a restauração.

O caminho padrão (retornado pelo método [**GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) da mesma instância de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) é usado para definir um local de restauração ou um mapeamento de local alternativo — encontrado usando o método [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) — indica onde um arquivo deve ser restaurado (consulte [trabalhando com locais alternativos durante a restauração](working-with-alternate-locations-during-restore.md)).

 

 



