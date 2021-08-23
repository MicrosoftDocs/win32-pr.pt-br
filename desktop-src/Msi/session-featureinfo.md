---
description: O método FeatureInfo do objeto Session retorna um objeto FeatureInfo que contém informações descritivas para o recurso especificado.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Método Session. FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4d6e44a16305d4a46525cfed631068ff0137c642b09b8dc6a9eca169a104548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625194"
---
# <a name="sessionfeatureinfo-method"></a>Método Session. FeatureInfo

O método **FeatureInfo** do objeto [**Session**](session-object.md) retorna um objeto **FeatureInfo** que contém informações descritivas para o recurso especificado.

## <a name="syntax"></a>Sintaxe


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recurso* 
</dt> <dd>

Identifica o recurso de interesse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




