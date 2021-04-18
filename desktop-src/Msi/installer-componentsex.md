---
description: Retorna um objeto Recordlist que lista os componentes instalados.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Propriedade Installer. ComponentsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749793"
---
# <a name="installercomponentsex-property"></a>Propriedade Installer. ComponentsEx

Essa propriedade retorna um objeto [**recordlist**](recordlist-object.md) que lista os componentes instalados. Essa propriedade chama [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Essa propriedade está disponível a partir do Windows Installer 5,0.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ComponentsEx
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

[**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




