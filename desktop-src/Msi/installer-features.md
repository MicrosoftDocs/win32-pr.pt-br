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
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751649"
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
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Funções de status do sistema](installer-function-reference.md)
</dt> </dl>

 

 




