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
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759369"
---
# <a name="uipreviewproperty-property"></a>Propriedade UIPreview. Property

A propriedade **Property** do objeto [**UIPreview**](uipreview-object.md) é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador ou, se for prefixada com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual. Isso é exposto para permitir a exibição adequada de caixas de diálogo que dependem de valores de propriedade. Os valores de cadeia de caracteres ou inteiros podem ser fornecidos. Uma propriedade ou variável de ambiente inexistente é equivalente ao valor que está sendo nulo.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>Valor da propriedade

O nome de uma propriedade que diferencia maiúsculas de minúsculas ou um nome que não diferencia maiúsculas de minúsculas de uma variável de ambiente prefixado por um sinal de porcentagem (%).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview é definido como 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




