---
title: Backup
description: Permitir que aplicativos de backup se comuniquem com outros aplicativos e serviços sobre operações de backup e restauração. Execute o backup em fita, inicialize a fita e recupere informações da unidade de fita. Manter arquivos duplicados com o SIS (armazenamento de instância única).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- Backup de backup
- backup Backup , home
- backup de operações de restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efe2668df47c271aba5befc3ba380c313b7bc15c11162a29b8364be6eb3fead
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588886"
---
# <a name="backup"></a>Backup

As chaves do Registro para backup e restauração permitem que os aplicativos de backup se comuniquem com outros aplicativos e serviços sobre operações de backup e restauração. Para obter mais informações, consulte Chaves e valores do Registro [para backup e restauração.](registry-keys-for-backup-and-restore.md)

A API de backup em fita permite que os aplicativos de backup leiam e gravem em uma fita, inicializam uma fita e recuperam informações de fita ou unidade de fita. Para obter mais informações, consulte [Backup em fita](tape-backup.md).

O SIS (armazenamento de instância única) é uma arquitetura projetada para manter arquivos duplicados com um mínimo de sobrecarga. O aplicativo de backup usa a API de backup do SIS para acessar a arquitetura do SIS. Para obter mais informações, consulte [Armazenamento de instância única e Backup do SIS.](single-instance-store-and-sis-backup.md)

O backup e a restauração de arquivos criptografados são habilitados pela API de criptografia bruta, que lê e grava arquivos criptografados enquanto mantém os dados em formato criptografado. A API permite que os dados criptografados nesses arquivos sejam armazenados em backup e restaurados, ao mesmo tempo que a meta de manter a segurança dos dados de backup e ser usada por um aplicativo que não tem permissão para usar as chaves de criptografia no arquivo. Para obter mais informações, [consulte Backup e restauração de arquivos criptografados.](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)

A ferramenta Saslayed pode permitir que os aplicativos de recuperação de estado do sistema movam, excluam e deem o nome curto dos arquivos do sistema. Para obter mais informações, [ consulteSrdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de backup](backup-reference.md)
</dt> </dl>

 

 