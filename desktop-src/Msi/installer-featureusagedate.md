---
description: A propriedade FeatureUsageDate é uma propriedade somente leitura que retorna a data em que o recurso especificado foi usado pela última vez.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Propriedade Installer. FeatureUsageDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748590"
---
# <a name="installerfeatureusagedate-property"></a>Propriedade Installer. FeatureUsageDate

A propriedade **FeatureUsageDate** é uma propriedade somente leitura que retorna a data em que o recurso especificado foi usado pela última vez.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

O uso dos métodos [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) ou [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) ou seus equivalentes de API no recurso especificado define essa propriedade.

A data está no formato de data do MS-DOS, conforme mostrado na tabela a seguir.



| Bits | Sumário                                            |
|------|-----------------------------------------------------|
| 0-4  | Dia do mês (1-31)                             |
| 5-8  | Mês (1 = Janeiro, 2 = fevereiro e assim por diante)        |
| 9-15 | Deslocamento de ano de 1980 (adicione 1980 para obter o ano real) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




