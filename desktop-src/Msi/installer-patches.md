---
description: A propriedade Patches somente leitura do objeto Installer retorna um objeto StringList que contém todos os patches aplicados ao produto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Propriedade Installer.Patches
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
ms.openlocfilehash: 33576b92924493a99c058196639faa34f5b42e388b9e30b6e300c17444ddeeff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430776"
---
# <a name="installerpatches-property"></a>Propriedade Installer.Patches

A propriedade **Patches** somente leitura do objeto [**Installer**](installer-object.md) retorna um objeto [**StringList**](stringlist-object.md) que contém todos os patches aplicados ao produto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Valor da propriedade

Especifica o código do produto.

## <a name="remarks"></a>Comentários

Para enumerar os patches, um aplicativo itera pelo objeto [**StringList**](stringlist-object.md) usando um constructo For Each. Como os patches não são ordenados, qualquer novo patch tem um índice arbitrário. Isso significa que a função pode retornar patches em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




