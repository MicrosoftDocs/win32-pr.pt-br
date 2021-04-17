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
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747946"
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

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




