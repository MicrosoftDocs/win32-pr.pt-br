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
ms.openlocfilehash: 16b4b4a259bf4e1c77fde592c5668f8584b28ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785068"
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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




