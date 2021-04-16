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
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747547"
---
# <a name="installercomponentpathex-property"></a>Propriedade Installer. ComponentPathEx

Essa propriedade retorna um objeto [**recordlist**](recordlist-object.md) que fornece o caminho completo de um componente instalado especificado. Essa propriedade chama [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Essa propriedade está disponível a partir do Windows Installer 5,0.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




