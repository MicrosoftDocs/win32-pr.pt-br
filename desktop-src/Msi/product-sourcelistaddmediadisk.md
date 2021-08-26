---
description: Método Product.SourceListAddMediaDisk – o método SourceListAddMediaDisk adiciona um disco ao conjunto de discos registrados. Aceita Diskid, VolumeLabel e DiskPrompt como parâmetros. Esse método chama em MsiSourceListAddMediaDisk.
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Método Product.SourceListAddMediaDisk
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
ms.openlocfilehash: 9e3f6df653abeefd57f8311eed0d9e578f6a525c1a0dc915f4b629d367bb79fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042126"
---
# <a name="productsourcelistaddmediadisk-method"></a>Método Product.SourceListAddMediaDisk

O **método SourceListAddMediaDisk** adiciona um disco ao conjunto de discos registrados. Aceita *Diskid,* *VolumeLabel* e *DiskPrompt* como parâmetros. Esse método chama [**em MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

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

*Diskid* 
</dt> <dd>

Esse parâmetro fornece a ID do disco que está sendo adicionado ou atualizado.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Esse parâmetro fornece o rótulo do disco que está sendo adicionado ou atualizado. Uma atualização substitui o rótulo de volume existente no Registro. Para alterar apenas o prompt de disco, obter o rótulo de volume registrado existente e forneça-o junto com o novo prompt de disco. Uma cadeia de caracteres vazia para esse parâmetro registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o rótulo do volume.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Esse parâmetro fornece o prompt de disco do disco que está sendo adicionado ou atualizado. Uma atualização substitui o prompt de disco existente no Registro. Para alterar apenas o rótulo do volume, obter o prompt de disco existente do Registro e forneça-o com o novo rótulo de volume. Uma cadeia de caracteres vazia para esse parâmetro registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o prompt de disco.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct é definido como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Produto**](product-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




