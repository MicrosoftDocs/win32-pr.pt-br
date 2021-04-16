---
description: A propriedade FeatureCurrentState do objeto Session é uma propriedade somente leitura que retorna o estado atual instalado do recurso designado. Para valores de estado, consulte a propriedade FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Propriedade Session. FeatureCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787067"
---
# <a name="sessionfeaturecurrentstate-property"></a>Propriedade Session. FeatureCurrentState

A propriedade **FeatureCurrentState** do objeto [**Session**](session-object.md) é uma propriedade somente leitura que retorna o estado atual instalado do recurso designado. Para valores de estado, consulte a propriedade [**FeatureRequestState**](session-featurerequeststate.md) .

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Valor da propriedade

Nome de cadeia de caracteres necessário do recurso solicitado e uma chave primária na [tabela de recursos](feature-table.md).

## <a name="remarks"></a>Comentários

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Session**](session-object.md)
</dt> <dt>

[**Propriedade FeatureRequestState**](session-featurerequeststate.md)
</dt> </dl>

 

 




