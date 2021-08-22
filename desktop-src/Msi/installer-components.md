---
description: A propriedade componentes somente leitura retorna um objeto StringList que enumera o conjunto de componentes instalados para todos os produtos.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Propriedade Installer. Components
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b8538e594ed02a1bc355ed4cf57db1befb1443e58d7afe2038b16e08eb9e4659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632404"
---
# <a name="installercomponents-property"></a>Propriedade Installer. Components

A propriedade **componentes** somente leitura retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de componentes instalados para todos os produtos.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Para enumerar os componentes, um aplicativo pode iterar por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each. Como os componentes não são ordenados, todos os componentes novos têm um índice arbitrário. Isso significa que a função pode retornar componentes em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




