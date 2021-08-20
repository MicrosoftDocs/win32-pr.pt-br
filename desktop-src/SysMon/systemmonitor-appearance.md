---
title: Propriedade SystemMonitor. Appearance
description: Recupera ou define a aparência do controle para incluir ou omitir os efeitos de exibição tridimensionais.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Propriedade Appearance SysMon
- Propriedade Appearance SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c606ed69bca635fe0f261f64ed4439305dcdfb542edd4c0095e62eaa97266147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956199"
---
# <a name="systemmonitorappearance-property"></a>Propriedade SystemMonitor. Appearance

Recupera ou define a aparência do controle para incluir ou omitir os efeitos de exibição tridimensionais.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property Appearance As Long
```



## <a name="property-value"></a>Valor da propriedade

O valor de aparência que determina se o controle é pintado com efeitos tridimensionais.

Você pode definir essa propriedade como um dos valores a seguir.



| Valor                                                                        | Significado                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Pinta o controle sem efeitos visuais.<br/>                                    |
| <dl> <dt>1</dt> </dl> | Pinta o controle com efeitos tridimensionais. Esse é o valor padrão.<br/> |



 

## <a name="exceptions"></a>Exceções



| Tipo de exceção               | Condição                                    |
|------------------------------|----------------------------------------------|
| **System.ArgumentException** | O valor de aparência especificado não é válido. |



 

## <a name="remarks"></a>Comentários

Essa é uma propriedade de ambiente. O valor dessa propriedade é determinado pelo contêiner. Definir o valor dessa propriedade pode afetar a ilusão do controle e do contêiner sendo um único aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





