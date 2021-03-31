---
title: Funções de backup
description: As funções a seguir são usadas com o backup em fita.
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312c7477c28f83b7c1c64073234799219346f89a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641504"
---
# <a name="backup-functions"></a>Funções de backup

As funções a seguir são usadas com o [backup em fita](tape-backup.md).



| Função                                           | Descrição                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | Lê os dados associados a um arquivo ou diretório especificado em um buffer.                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | Busca adiante em um fluxo de dados.                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | Grava um fluxo de dados de um buffer para um arquivo ou diretório especificado.                                |
| [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | Reformata uma fita.                                                                                      |
| [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | Apaga toda ou parte de uma fita.                                                                          |
| [**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | Recupera informações que descrevem a fita ou a unidade de fita.                                       |
| [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | Recupera o endereço atual da fita.                                                             |
| [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | Determina se o dispositivo de fita está pronto para processar comandos de fita.                                  |
| [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | Prepara a fita para ser acessada ou removida.                                                           |
| [**Setfitaparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | Especifica o tamanho do bloco de uma fita ou configura o dispositivo de fita.                                      |
| [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | Define a posição da fita no dispositivo especificado.                                                        |
| [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | Grava um número especificado de marcas de gravação, marcações, marcas de gravação curtas ou longas marcas de caixa de filepara um dispositivo de fita. |



 

As funções a seguir são fornecidas para trabalhar com o [armazenamento de instância única e o backup do SIS](single-instance-store-and-sis-backup.md).



| Função                                                          | Descrição                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**SisCreateBackupStructure**](siscreatebackupstructure.md)      | Cria a estrutura de backup do SIS especificada com base nas informações fornecidas.                      |
| [**SisCreateRestoreStructure**](siscreaterestorestructure.md)    | Cria a estrutura de restauração do SIS especificada com base nas informações fornecidas.                     |
| [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)    | Retorna informações que descrevem os arquivos de armazenamento comuns aos quais o link do SIS especificado aponta.            |
| [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)          | Libera memória alocada pelas funções de API do SIS.                                                       |
| [**SisFreeBackupStructure**](sisfreebackupstructure.md)          | Libera a estrutura de backup do SIS especificada.                                                          |
| [**SisFreeRestoreStructure**](sisfreerestorestructure.md)        | Libera a estrutura de restauração do SIS especificada.                                                         |
| [**SisRestoredCommon StoreFile**](sisrestoredcommonstorefile.md) | Relata para a arquitetura do SIS que um arquivo de armazenamento comum foi gravado.                         |
| [**SisRestoredLink**](sisrestoredlink.md)                        | Retorna os nomes do arquivo de repositório comum ou dos arquivos apontados pelo link SIS restaurado especificado. |



 

As funções a seguir são fornecidas para trabalhar com [backup e restauração de arquivos criptografados](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).



| Função                                                | Descrição                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CloseEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | Feche um arquivo criptografado aberto com [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa). |
| [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | Abra um arquivo criptografado com acesso aos dados em formato criptografado.                            |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | Ler um arquivo criptografado deixando seus dados no formato criptografado.                               |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | Grave um arquivo criptografado deixando seus dados no formato criptografado.                              |



 

 

 