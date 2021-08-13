---
description: Retorna um objeto Recordlist que lista os produtos que usam um componente instalado especificado.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Propriedade Installer. ClientsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 54ecc8c0d76ae5105aec07a85adb18d93a8e7a9b75162f8124bb32fdd7f64597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632923"
---
# <a name="installerclientsex-property"></a>Propriedade Installer. ClientsEx

Essa propriedade retorna um objeto [**recordlist**](recordlist-object.md) que lista os produtos que usam um componente instalado especificado. Essa propriedade chama [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. essa propriedade está disponível a partir do Windows Installer 5,0.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ClientsEx
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

[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




