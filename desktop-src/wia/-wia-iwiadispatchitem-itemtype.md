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
ms.openlocfilehash: 3cbf60c935a88a62786c7c516ec0e768d65019c02d4419c44d928cee704a67b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450776"
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
| file   | O item é um arquivo de imagem ou áudio.             |
| áudio  | O item é um clipe de áudio.                      |
| image  | O item é uma imagem.                           |



 

## <a name="remarks"></a>Comentários

Um item pode ter mais de um tipo. Por exemplo, cada imagem é dos tipos "imagem" e "arquivo". **ItemType** retorna uma cadeia de caracteres que inclui todos os tipos válidos para o item, separados por ponto e vírgula. Por exemplo, "Image; File". Não há nenhum espaço nessa cadeia de caracteres e não há um ponto-e-vírgula no final.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




