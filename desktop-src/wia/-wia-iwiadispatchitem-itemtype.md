---
description: O tipo deste item. Somente leitura.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Propriedade Item. ItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790395"
---
# <a name="itemitemtype-property"></a>Propriedade Item. ItemType

O tipo deste item. Somente leitura.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a>Valor da propriedade

Os seguintes valores são possíveis:



| Valor  | Descrição                                     |
|--------|-------------------------------------------------|
| dispositivo | O item é um dispositivo de hardware WIA.              |
| folder | O item é uma pasta que contém outros itens. |
| arquivo   | O item é um arquivo de imagem ou áudio.             |
| áudio  | O item é um clipe de áudio.                      |
| image  | O item é uma imagem.                           |



 

## <a name="remarks"></a>Comentários

Um item pode ter mais de um tipo. Por exemplo, cada imagem é dos tipos "imagem" e "arquivo". **ItemType** retorna uma cadeia de caracteres que inclui todos os tipos válidos para o item, separados por ponto e vírgula. Por exemplo, "Image; File". Não há nenhum espaço nessa cadeia de caracteres e não há um ponto-e-vírgula no final.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




