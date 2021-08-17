---
description: A propriedade FeatureUsageCount é uma propriedade somente leitura que retorna o número de vezes que o recurso foi usado.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Propriedade Installer. FeatureUsageCount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f0f8444909d07655949cd35d060eb455e5a153fc2b897e757c2fdde2d1d731d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631195"
---
# <a name="installerfeatureusagecount-property"></a>Propriedade Installer. FeatureUsageCount

A propriedade **FeatureUsageCount** é uma propriedade somente leitura que retorna o número de vezes que o recurso foi usado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

O uso dos métodos [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) ou [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) ou seus equivalentes de API no recurso especificado incrementa essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




