---
description: Retorna um objeto RecordList que lista os componentes instalados.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Propriedade Installer.ComponentsEx
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
ms.openlocfilehash: 1805780c7d21018ec51273b00df88493e25a38dd4525428ba605f8fa9934ceaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632314"
---
# <a name="installercomponentsex-property"></a>Propriedade Installer.ComponentsEx

Essa propriedade retorna um [**objeto RecordList**](recordlist-object.md) que lista os componentes instalados. Essa propriedade chama [**MsiEnumComponentsEx.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)

**[Windows Instalador 4.5 ou anterior:](not-supported-in-windows-installer-4-5.md)** Sem suporte. Essa propriedade está disponível a partir do Windows Installer 5.0.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




