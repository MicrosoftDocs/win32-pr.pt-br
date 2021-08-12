---
description: A Propriedade Property do objeto UIPreview é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador ou, se for prefixada com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Propriedade UIPreview. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 51ef7b4589372006241beff1e9c35180b32c4d358e817b8d380353c324ffd9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623199"
---
# <a name="uipreviewproperty-property"></a>Propriedade UIPreview. Property

A propriedade **Property** do objeto [**UIPreview**](uipreview-object.md) é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador ou, se for prefixada com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual. Isso é exposto para permitir a exibição adequada de caixas de diálogo que dependem de valores de propriedade. Os valores de cadeia de caracteres ou inteiros podem ser fornecidos. Uma propriedade ou variável de ambiente inexistente é equivalente ao valor que está sendo nulo.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>Valor da propriedade

O nome de uma propriedade que diferencia maiúsculas de minúsculas ou um nome que não diferencia maiúsculas de minúsculas de uma variável de ambiente prefixado por um sinal de porcentagem (%).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview é definido como 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




