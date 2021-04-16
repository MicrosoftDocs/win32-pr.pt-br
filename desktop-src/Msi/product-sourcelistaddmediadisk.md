---
description: O método SourceListAddMediaDisk adiciona um disco ao conjunto de discos registrados. Aceita DiskId, VolumeLabel e DiskPrompt como parâmetros. Esse método chama em MsiSourceListAddMediaDisk.
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Método Product. SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2f81b21570d708f361e45be7f6f42a93fd0d335
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747325"
---
# <a name="productsourcelistaddmediadisk-method"></a>Método Product. SourceListAddMediaDisk

O método **SourceListAddMediaDisk** adiciona um disco ao conjunto de discos registrados. Aceita *DiskId*, *VolumeLabel* e *DiskPrompt* como parâmetros. Esse método chama em [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

## <a name="syntax"></a>Sintaxe


```JScript
Product.SourceListAddMediaDisk(
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

Esse parâmetro fornece o rótulo do disco que está sendo adicionado ou atualizado. Uma atualização substitui o rótulo de volume existente no registro. Para alterar apenas a solicitação de disco, obtenha o rótulo de volume registrado existente e forneça-o junto com o novo prompt de disco. Uma cadeia de caracteres vazia para esse parâmetro registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o rótulo do volume.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Esse parâmetro fornece o prompt de disco do disco que está sendo adicionado ou atualizado. Uma atualização substitui o prompt de disco existente no registro. Para alterar apenas o rótulo do volume, obtenha o prompt de disco existente do registro e forneça o novo rótulo de volume. Uma cadeia de caracteres vazia para esse parâmetro registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o prompt de disco.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Remessa**](product-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




