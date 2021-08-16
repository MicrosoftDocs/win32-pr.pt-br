---
description: A propriedade Features é uma propriedade somente leitura que retorna um objeto StringList que enumera o conjunto de recursos publicados para o produto especificado.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Propriedade Installer. Features
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e31dfe2c487a151280a10c4fa7222c005f94c0eeb4ac4f3f5145d67ab600fe9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631468"
---
# <a name="installerfeatures-property"></a>Propriedade Installer. Features

A propriedade **Features** é uma propriedade somente leitura que retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de recursos publicados para o produto especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Valor da propriedade

Especifica o código do produto do produto.

## <a name="remarks"></a>Comentários

Para enumerar os recursos, um aplicativo é iterado por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each. Como os recursos não são ordenados, qualquer recurso novo tem um índice arbitrário, o que significa que a função pode retornar recursos em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Funções de status do sistema](installer-function-reference.md)
</dt> </dl>

 

 




