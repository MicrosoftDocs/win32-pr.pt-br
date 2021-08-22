---
description: Retorna um objeto Recordlist que fornece o caminho completo de um componente instalado especificado.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Propriedade Installer. ComponentPathEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 720b10c75fcdf4a6b72f22a72d3b0860fc6089403385b0a951127f56286b6953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632610"
---
# <a name="installercomponentpathex-property"></a>Propriedade Installer. ComponentPathEx

Essa propriedade retorna um objeto [**recordlist**](recordlist-object.md) que fornece o caminho completo de um componente instalado especificado. Essa propriedade chama [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. essa propriedade está disponível a partir do Windows Installer 5,0.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




