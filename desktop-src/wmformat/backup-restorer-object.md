---
title: Objeto do restaurador de backup
description: Objeto do restaurador de backup
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows SDK do formato de mídia, objetos do restaurador de backup
- ASF (Advanced Systems Format), objetos do restaurador de backup
- ASF (formato de sistemas avançados), objetos do restaurador de backup
- objetos, objetos do restaurador de backup
- restaurador de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7bf14f8afda284d8d0ae3d4f36d37fff0baa63f4f42802a98830038ec2d850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028124"
---
# <a name="backup-restorer-object"></a>Objeto do restaurador de backup

O restaurador de backup fornece interfaces para lidar com o backup de licenças, normalmente em mídia removível e, em seguida, a restauração dessas licenças em um novo computador.

O objeto do restaurador de backup é criado pela função [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) , que define um ponteiro para uma interface [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) . As outras interfaces do objeto do restaurador de backup podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte do objeto restaurador de backup.



| Interface                                              | Descrição                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Define e recupera as propriedades exigidas pelas interfaces [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) e [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) . |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Faz backup de licenças, normalmente para que elas possam ser restauradas em outro computador.                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Restaura licenças.                                                                                                                                        |



 

A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para usar o objeto de restaurador de backup.



| Interface                                      | Descrição                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recebe mensagens de status de processos que são executados em um thread separado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fazendo backup e restaurando licenças**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Objeto**](objects.md)
</dt> </dl>

 

 




