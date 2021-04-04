---
title: Backup
description: Permitir que aplicativos de backup se comuniquem com outros aplicativos e serviços sobre operações de backup e restauração. Execute o backup em fita, inicialize a fita e recupere as informações da unidade de fita. Manter arquivos duplicados com o SIS (armazenamento de instância única).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- Backup de backup
- Backup de backup, página inicial
- Backup de operações de restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084721"
---
# <a name="backup"></a>Backup

As chaves do registro para backup e restauração permitem que aplicativos de backup se comuniquem com outros aplicativos e serviços sobre operações de backup e restauração. Para obter mais informações, consulte [chaves e valores do registro para backup e restauração](registry-keys-for-backup-and-restore.md).

A API de backup em fita permite que os aplicativos de backup leiam e gravem em uma fita, inicializem uma fita e recuperem informações de fita ou unidade de fita. Para obter mais informações, consulte [backup em fita](tape-backup.md).

O SIS (armazenamento de instância única) é uma arquitetura projetada para manter arquivos duplicados com um mínimo de sobrecarga. Aplicativo de backup use a API de backup do SIS para acessar a arquitetura do SIS. Para obter mais informações, consulte [armazenamento de instância única e backup do SIS](single-instance-store-and-sis-backup.md).

O backup e a restauração de arquivos criptografados são habilitados pela API de criptografia bruta, que lê e grava arquivos criptografados enquanto mantém os dados em formato criptografado. A API permite que os dados criptografados nesses arquivos sejam armazenados em backup e restaurados, ao mesmo tempo em que atendem às metas de manutenção da segurança dos dados de backup e que podem ser usados por um aplicativo que não tem permissão para usar as chaves de criptografia no arquivo. Para obter mais informações, consulte [backup e restauração de arquivos criptografados](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).

A ferramenta Srdelayed pode permitir que aplicativos de recuperação de estado do sistema movam, excluam e definam o nome curto dos arquivos do sistema. Para obter mais informações, consulte [Srdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de backup](backup-reference.md)
</dt> </dl>

 

 