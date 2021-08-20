---
description: Método Patch.SourceListAddMediaDisk – o método SourceListAddMediaDisk adiciona um disco ao conjunto de discos registrados. Aceita Diskid, VolumeLabel e DiskPrompt como parâmetros. Esse método chama em MsiSourceListAddMediaDisk.
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Método Patch.SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3df81274581c64a37fbf505bbfd68d0907f5ca626e58bdfccbac61156fd29a9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942607"
---
# <a name="patchsourcelistaddmediadisk-method"></a>Método Patch.SourceListAddMediaDisk

O **método SourceListAddMediaDisk** adiciona um disco ao conjunto de discos registrados. Aceita *Diskid,* *VolumeLabel* e *DiskPrompt* como parâmetros. Esse método chama [**em MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

## <a name="syntax"></a>Sintaxe


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Diskid* 
</dt> <dd>

Esse parâmetro fornece a ID do disco que está sendo adicionado ou atualizado.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Esse parâmetro fornece o rótulo do disco que está sendo adicionado ou atualizado. Uma atualização substitui o rótulo de volume existente no Registro. Para alterar apenas o prompt de disco, obter o rótulo de volume registrado existente e forneça-o junto com o novo prompt de disco. Uma cadeia de caracteres NULL ou vazia registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o rótulo do volume.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Esse parâmetro fornece o prompt de disco do disco que está sendo adicionado ou atualizado. Uma atualização substitui o prompt de disco existente no Registro. Para alterar apenas o rótulo do volume, obter o prompt de disco existente do Registro e forneça-o com o novo rótulo de volume. Uma cadeia de caracteres NULL ou vazia registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o prompt de disco.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch é definido como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




