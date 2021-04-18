---
description: A propriedade ShortcutTarget do objeto do instalador examina um atalho e retorna seu produto, o nome do recurso e o componente, se disponível.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Propriedade Installer. ShortcutTarget
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752249"
---
# <a name="installershortcuttarget-property"></a>Propriedade Installer. ShortcutTarget

A propriedade **ShortcutTarget** do objeto do [**instalador**](installer-object.md) examina um atalho e retorna seu produto, o nome do recurso e o componente, se disponível.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Valor da propriedade

Caminho completo e nome do arquivo.

## <a name="remarks"></a>Comentários

ShortcutTarget retorna um [**objeto de registro**](record-object.md) que contém três campos:

-   O campo 1 é um GUID para o código do produto do atalho, se disponível. Este campo pode ser nulo.
-   O campo 2 é a ID do recurso do atalho, se disponível. Este campo pode ser nulo.
-   O campo 3 é um GUID para o código do componente, se disponível. Este campo pode ser nulo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




