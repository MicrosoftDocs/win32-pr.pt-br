---
description: A propriedade PatchFiles retorna um objeto StringList que contém uma lista de arquivos que podem ser atualizados pela lista de patches fornecida.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Propriedade Installer. PatchFiles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752451"
---
# <a name="installerpatchfiles-property"></a>Propriedade Installer. PatchFiles

A propriedade **PatchFiles** retorna um objeto [**StringList**](stringlist-object.md) que contém uma lista de arquivos que podem ser atualizados pela lista de patches fornecida. Essa propriedade chama [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista). Para obter mais informações sobre como usar a propriedade **PatchFiles** , consulte [listando os arquivos que podem ser atualizados](listing-the-files-that-can-be-updated.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 4,5 no Windows Server 2003 e no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto do instalador**](installer-object.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




