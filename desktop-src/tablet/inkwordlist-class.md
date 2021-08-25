---
description: Representa uma lista de palavras que podem ser usadas para melhorar o resultado do reconhecimento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Classe InkWordList (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: fe46cf8f1befaf2717cfcf0a8e131113ed4552843bd3b6572364c27f3418ab34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938666"
---
# <a name="inkwordlist-class"></a>Classe InkWordList

Representa uma lista de palavras que podem ser usadas para melhorar o resultado do reconhecimento.

**InkWordList** tem estes tipos de membros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)

### <a name="interfaces"></a>Interfaces

A **classe InkWordList** define essas interfaces.



| Interface        | Descrição                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | Esse objeto implementa a interface **COM IInkWordList.**<br/> |



 

### <a name="methods"></a>Métodos

A **classe InkWordList** tem esses métodos.



| Método                                       | Descrição                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Adiciona uma única palavra ao **InkWordList.**<br/>                   |
| [**Mesclagem**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Mescla outro **InkWordList** a neste **InkWordList.**<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Remove uma única palavra de um **InkWordList.**<br/>                |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedade WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Constantes factoid](factoid-constants.md)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

