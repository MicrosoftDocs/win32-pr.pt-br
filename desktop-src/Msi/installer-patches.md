---
description: A propriedade patches somente leitura do objeto instalador retorna um objeto StringList que contém todos os patches aplicados ao produto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Propriedade Installer. patches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752037"
---
# <a name="installerpatches-property"></a>Propriedade Installer. patches

A propriedade **patches** somente leitura do objeto [**instalador**](installer-object.md) retorna um objeto [**StringList**](stringlist-object.md) que contém todos os patches aplicados ao produto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Valor da propriedade

Especifica o código do produto.

## <a name="remarks"></a>Comentários

Para enumerar os patches, um aplicativo é iterado por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each. Como os patches não são ordenados, qualquer patch novo tem um índice arbitrário. Isso significa que a função pode retornar patches em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




