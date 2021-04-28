---
description: Método patch. SourceListAddMediaDisk – o método SourceListAddMediaDisk adiciona um disco ao conjunto de discos registrados. Aceita DiskId, VolumeLabel e DiskPrompt como parâmetros. Esse método chama em MsiSourceListAddMediaDisk.
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Método patch. SourceListAddMediaDisk
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
ms.openlocfilehash: 052831befb95976358b53d989db36d5b2fa43efe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084363"
---
# <a name="patchsourcelistaddmediadisk-method"></a>Método patch. SourceListAddMediaDisk

O método **SourceListAddMediaDisk** adiciona um disco ao conjunto de discos registrados. Aceita *DiskId*, *VolumeLabel* e *DiskPrompt* como parâmetros. Esse método chama em [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

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

*DiskId* 
</dt> <dd>

Esse parâmetro fornece a ID do disco que está sendo adicionado ou atualizado.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Esse parâmetro fornece o rótulo do disco que está sendo adicionado ou atualizado. Uma atualização substitui o rótulo de volume existente no registro. Para alterar apenas a solicitação de disco, obtenha o rótulo de volume registrado existente e forneça-o junto com o novo prompt de disco. Uma cadeia de caracteres nula ou vazia registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o rótulo do volume.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Esse parâmetro fornece o prompt de disco do disco que está sendo adicionado ou atualizado. Uma atualização substitui o prompt de disco existente no registro. Para alterar apenas o rótulo do volume, obtenha o prompt de disco existente do registro e forneça o novo rótulo de volume. Uma cadeia de caracteres nula ou vazia registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o prompt de disco.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Distribuído**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




