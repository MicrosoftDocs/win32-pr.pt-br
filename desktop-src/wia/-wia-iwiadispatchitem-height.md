---
description: A altura, em pixels, do item. Somente leitura.
ms.assetid: 0df73d33-c1ae-43e1-b906-00540e04dfd9
title: Propriedade Item. Height
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Height
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b9828fddf5630bfa1513fdb7913087054ad2c2c533468d69ca9b1b63e79b0341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208342"
---
# <a name="itemheight-property"></a>Propriedade Item. Height

A altura, em pixels, do item. Somente leitura.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Item.Height
```



## <a name="property-value"></a>Valor da propriedade

Variável que recebe a altura.

## <a name="remarks"></a>Comentários

Se o item for uma câmera digital, a propriedade **Height** representará a altura das imagens que essa câmera gera. Se o item for um scanner, essa propriedade representará a altura da base de verificação. Se o item for uma imagem, essa propriedade representará a altura real da imagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




