---
title: Fazendo backup e restaurando licenças
description: Fazendo backup e restaurando licenças
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows SDK do formato de mídia, fazendo backup de licenças
- Windows SDK de formato de mídia, restaurando licenças
- Windows SDK de formato de mídia, backup e restauração de licenças
- ASF (Advanced Systems Format), fazendo backup de licenças
- ASF (formato de sistemas avançados), fazendo backup de licenças
- ASF (Advanced Systems Format), restaurando licenças
- ASF (formato de sistemas avançados), restaurando licenças
- ASF (Advanced Systems Format), backup de licença e restauração
- ASF (formato de sistemas avançados), backup e restauração de licenças
- DRM (gerenciamento de direitos digitais), fazendo backup de licenças
- DRM (gerenciamento de direitos digitais), fazendo backup de licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), backup e restauração de licenças
- DRM (gerenciamento de direitos digitais), backup e restauração de licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378a41d975e8f19d38c637d585759d0038f5b86550769ae49d6a6490844f223e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028134"
---
# <a name="backing-up-and-restoring-licenses"></a>Fazendo backup e restaurando licenças

Os processos de backup e restauração são assíncronos. Elas são disparadas quando o usuário seleciona um comando de menu ou uma opção no aplicativo para fazer backup ou restaurar licenças. Você deve permitir que o usuário especifique os locais em que as licenças devem ser armazenadas em backup e restauradas.

Para fazer backup de licenças:

1.  Use a função [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) para criar o objeto de restaurador de backup.
2.  Chame o método [**IWMBackupRestoreProps:: SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) para definir o caminho de backup (o local onde você irá gravar os arquivos, como: \\ ou D: \\ licenças).
3.  Chame o método [**IWMLicenseBackup:: BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) para fazer backup das licenças no caminho especificado.

Os eventos a seguir são enviados para o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :

-   **WMT \_ BACKUPRESTORE \_ begin** indica que o processo de backup foi iniciado.
-   **WMT \_ BACKUPRESTORE \_ end** indica que o processo de backup foi concluído.
-   **WMT \_ \_Licença restrita** indica que uma ou mais licenças não podem ser submetidas a backup porque o direito não foi permitido pelo proprietário do conteúdo.

A ID da chave também é incluída nesta mensagem. Se você tiver implementado um banco de dados para arquivos protegidos que incluam a ID de chave e os metadados, você poderá exibir uma mensagem para o usuário com o título específico (como um título de música) para o qual não é possível fazer backup da licença. Caso contrário, a mensagem deve ser genérica e informar ao usuário que não é possível fazer backup de algumas licenças.

Para restaurar licenças:

1.  Use a função **WMCreateBackupRestorer** para criar o objeto de restaurador de backup.
2.  Chame o método **IWMBackupRestoreProps:: SetProp** para definir o caminho de restauração para o local onde são feitos o backup das licenças.
3.  Chame o método [**IWMLicenseRestore:: RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) para restaurar licenças desse local.

Os eventos a seguir são enviados para o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :

-   **WMT \_ BACKUPRESTORE \_ conexão** indica que o aplicativo está se conectando ao serviço de gerenciamento de licenças.
-   **WMT \_ A \_ DESconexão do BACKUPRESTORE** indica que o aplicativo está desconectando do serviço de gerenciamento de licenças.
-   **WMT \_ BACKUPRESTORE \_ begin** indica que o processo de restauração foi iniciado.
-   **WMT \_ BACKUPRESTORE \_ end** indica que o processo de restauração foi concluído.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Interface IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**Interface IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**Interface IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




