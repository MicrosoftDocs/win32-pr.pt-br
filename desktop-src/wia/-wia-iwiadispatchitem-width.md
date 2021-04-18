---
description: A largura, em pixels, do item. Somente leitura.
ms.assetid: 4e636b76-af16-4fc1-8b88-2e0a2a24f841
title: Propriedade Item. Width
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Width
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: db55ceb84a61b65c0e173c210e21fb486d0e1ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807231"
---
# <a name="itemwidth-property"></a>Propriedade Item. Width

A largura, em pixels, do item. Somente leitura.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Item.Width
```



## <a name="property-value"></a>Valor da propriedade

Variável que recebe a largura.

## <a name="remarks"></a>Comentários

Se o item for uma câmera digital, a propriedade **Width** representará a largura das imagens que a câmera gera. Se o item for um scanner, essa propriedade representará a largura da base de verificação. Se o item for uma imagem, essa propriedade representará a largura real da imagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




