---
description: A tabela a seguir descreve os quatro tipos de componentes que podem ser envolvidos em uma operação de backup.
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: Trabalhando com a seleção para backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4bd20bd0c9139f8ed1c9f56cc8f499f1b6aaf14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461132"
---
# <a name="working-with-selectability-for-backup"></a>Trabalhando com a seleção para backup

A tabela a seguir descreve os quatro tipos de componentes que podem ser envolvidos em uma operação de backup.



| Tipo de componente                                                                                                                                                                                                               | Descrição                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componentes não selecionáveis para backup<br/>             | Não há ancestrais selecionáveis para backup em seus caminhos lógicos.<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componentes selecionáveis para backup<br/>                         | Não há ancestrais selecionáveis para backup em seus caminhos lógicos.<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Subcomponentes não selecionáveis para backup<br/> | Componentes não selecionáveis para backup com ancestrais selecionáveis para backup em seu caminho.<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Subcomponentes selecionáveis para backup<br/>             | Componentes selecionáveis para backup com ancestrais selecionáveis para backup em seu caminho.<br/>    |



 

Além disso, qualquer componente selecionável para backup — independentemente de ter o ancestral selecionável para backup ou não — define um [*conjunto de componentes*](vssgloss-c.md) se outros componentes o têm como um ancestral em seus caminhos lógicos.

As regras que regem a seleção de componentes para backup podem ser resumidas da seguinte maneira:

-   Quando qualquer componente sem um ancestral selecionável para backup em seu caminho lógico — se o componente é selecionável para backup ou não selecionável para backup — está incluído em um backup, ele deve ser [*incluído explicitamente*](vssgloss-e.md). Isso significa que os metadados para esses componentes são adicionados ao documento de componentes de backup.

    Os solicitantes adicionam explicitamente esses componentes usando o método [**IVssBackupComponents:: addcomponente**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) .

-   Os subcomponentes não selecionáveis para backup são sempre [*incluídos implicitamente*](vssgloss-i.md) no backup. Isso significa que os metadados para esses componentes não fazem parte do documento de componentes de backup.
-   Os subcomponentes selecionáveis para backup são incluídos implicitamente se esse ancestral estiver explicitamente incluído no backup. Nesse caso, os metadados para esses componentes não são adicionados ao documento de componentes de backup. Se um subcomponente de backup implicitamente selecionável definir um conjunto de componentes, os membros desse conjunto de componentes também serão selecionados implicitamente.
-   Subcomponentes selecioná-for-backup cujo ancestral selecionável para backup não está incluído explicitamente no backup ainda pode ser incluído explicitamente pelo solicitante usando o método [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) . Os metadados para o componente serão então adicionados ao documento de componentes de backup. Além disso, se um subcomponente selecionável para backup definir um conjunto de componentes, os membros desse conjunto de componentes serão incluídos implicitamente no backup.

O caso "myWriter" abordado em um [caminho lógico de componentes](logical-pathing-of-components.md) pode ser usado como um exemplo para ilustrar a seleção de backup.



| Nome do Componente | Caminho lógico            | Selecionável para backup |
|----------------|-------------------------|-----------------------|
| Executáveis  | ""                      | N                     |
| "ConfigFiles"  | Executáveis           | N                     |
| "LicenseInfo"  | ""                      | S                     |
| “Segurança”     | ""                      | S                     |
| UserInfo     | “Segurança”              | N                     |
| Certificado | “Segurança”              | N                     |
| "writerData"   | ""                      | S                     |
| Conjunto1         | "writerData"            | N                     |
| Janeiro          | "writerData \\ conjunto1"      | N                     |
| Dez          | "writerData \\ conjunto1"      | N                     |
| Conjunto2         | "writerData"            | N                     |
| Janeiro          | "writerData \\ conjunto2"      | N                     |
| Dez          | "writerData \\ conjunto2"      | N                     |
| Consultá        | "writerData \\ QueryLogs" | N                     |
| Usos        | "writerData"            | S                     |
| Janeiro          | "uso de writerData \\ "     | N                     |
| Dez          | "uso de writerData \\ "     | N                     |



 

Sempre que for feito o backup de "myWriter", a inclusão explícita do componente "executáveis" usando o método [**IVssBackupComponents:: addcomponente**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) incluirá implicitamente o componente "ConfigFiles".

O componente "LicenseInfo" é um componente selecionável para backup autônomo. Ele pode ser selecionado usando o método [**IVssBackupComponents:: addcomponente**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) ao critério do solicitante, mas sua seleção não selecionará nenhum outro componente.

O componente selecionável para backup "segurança" define um conjunto de componentes simples que contém dois subcomponentes não selecionáveis para backup, "UserInfo" e "Certificates". Se "Security" for explicitamente incluído para backup, "UserInfo" e "Certificates" sempre serão incluídos implicitamente também. Não há como incluir os subcomponentes "UserInfo" ou "Certificates" em uma operação de backup, a menos que "segurança" esteja incluído.

Se o componente "writerData" for selecionado, os componentes não selecionáveis para backup "Conjunto1", "Conjunto2" e "consulta", bem como o componente selecionável para backup "Usage", serão selecionados implicitamente. Cada um desses componentes tem subcomponentes que são selecionados implicitamente para backup. Nenhum de seus metadados será adicionado ao documento de componentes de backup.

Se o componente "writerData" não estiver selecionado, os componentes não selecionáveis para backup "Conjunto1", "Conjunto2" e "consulta" não serão incluídos para backup.

No entanto, os solicitantes podem optar por incluir explicitamente o selecionável para o componente de backup "uso". Os metadados desse componente serão adicionados ao documento de componentes de backup. Os subcomponentes "de uso" de "Jan" e "DEC" serão adicionados implicitamente ao backup, mas não terão suas informações adicionadas ao documento de componentes de backup.

A inclusão explícita de um componente para backup criará uma instância de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente no documento de componentes de backup.

Um solicitante recuperará informações sobre componentes explicitamente incluídos do documento de componentes de backup examinando os gravadores (usando [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)) incluídos em seu documento e recuperando os objetos [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) armazenados.

Como nenhuma das informações de conjunto de arquivos (especificação de arquivo, caminho e sinalizador de recursão) dos componentes presentes no documento de componentes de backup, nem quaisquer informações sobre componentes adicionados implicitamente estarão presentes, os solicitantes terão que consultar documentos de metadados do gravador para obter informações completas sobre todos os componentes incluídos no documento de componentes de backup.

 

 




