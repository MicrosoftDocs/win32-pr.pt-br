---
description: A propriedade ShortcutTarget do objeto Installer examina um atalho e retorna seu produto, nome do recurso e componente, se disponível.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Propriedade Installer.ShortcutTarget
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
ms.openlocfilehash: b54e334314c0bfd0fb721b175d0a14894d8a509ea02ff36e324903bb1fdbffaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893996"
---
# <a name="installershortcuttarget-property"></a>Propriedade Installer.ShortcutTarget

A **propriedade ShortcutTarget** do [**objeto Installer**](installer-object.md) examina um atalho e retorna seu produto, nome do recurso e componente, se disponível.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Valor da propriedade

Caminho completo e nome do arquivo.

## <a name="remarks"></a>Comentários

ShortcutTarget retorna um [**objeto Record**](record-object.md) que contém três campos:

-   O campo 1 é um GUID para o código do produto do atalho, se disponível. Esse campo pode ser nulo.
-   O campo 2 é a ID do recurso do atalho, se disponível. Esse campo pode ser nulo.
-   O campo 3 é um GUID para o código do componente, se disponível. Esse campo pode ser nulo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




