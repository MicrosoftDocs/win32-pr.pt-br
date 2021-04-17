---
description: O método SourceListClearMediaDisk do objeto patch remove um disco especificado do conjunto de discos registrados para um patch. Aceita DiskId como um parâmetro. Esse método chama MsiSourceListClearMediaDisk.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Método patch. SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748762"
---
# <a name="patchsourcelistclearmediadisk-method"></a>Método patch. SourceListClearMediaDisk

O método **SourceListClearMediaDisk** do objeto [**patch**](patch-object.md) remove um disco especificado do conjunto de discos registrados para um patch. Aceita *DiskId* como um parâmetro. Esse método chama [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).

## <a name="syntax"></a>Sintaxe


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DiskId* 
</dt> <dd>

Esse parâmetro fornece a ID do disco a ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




