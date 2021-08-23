---
description: A propriedade FeatureCost do objeto Session retorna a quantidade total de espaço em disco (em unidades de 512 bytes) exigida pelo recurso especificado e seus recursos pai (até a raiz da tabela de recursos).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Propriedade Session. FeatureCost
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 617d1695b8b472952f22737ba3f677d9320f9b4214afc3dea5a9cc5010e2b1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629286"
---
# <a name="sessionfeaturecost-property"></a>Propriedade Session. FeatureCost

A propriedade **FeatureCost** do objeto [**Session**](session-object.md) retorna a quantidade total de espaço em disco (em unidades de 512 bytes) exigida pelo recurso especificado e seus recursos pai (até a raiz da tabela de recursos). Para cada recurso, o custo total é composto pelos custos de disco atribuídos a todos os componentes vinculados ao recurso.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




