---
description: A propriedade sources enumera todas as fontes para a instância de patch. Essa propriedade chama MsiSourceListEnumSources e retorna uma matriz de cadeias de caracteres e aceita o tipo de origem como argumento.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Propriedade patch. Sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2a2f190c7d8ae42e43ac934a043dfb1a98a5e15e142415736406ffbd7f3cbc4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042396"
---
# <a name="patchsources-property"></a>Propriedade patch. Sources

A propriedade **sources** enumera todas as fontes para a instância de patch. Essa propriedade chama [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) e retorna uma matriz de cadeias de caracteres e aceita o tipo de origem como argumento.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a>Valor da propriedade

O tipo de origem a ser enumerado. O valor pode ser *msiInstallSourceTypeNetwork* (1) ou *msiInstallSourceTypeURL* (2).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Distribuído**](patch-object.md)
</dt> <dt>

[**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




