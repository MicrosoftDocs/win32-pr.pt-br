---
description: Representa uma lista de palavras que podem ser usadas para melhorar o resultado do reconhecimento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Classe InkWordList (Msinkaut. h)
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
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813628"
---
# <a name="inkwordlist-class"></a>Classe InkWordList

Representa uma lista de palavras que podem ser usadas para melhorar o resultado do reconhecimento.

**InkWordList** tem estes tipos de membros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)

### <a name="interfaces"></a>Interfaces

A classe **InkWordList** define essas interfaces.



| Interface        | Descrição                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | Esse objeto implementa a interface com do **IInkWordList** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **InkWordList** tem esses métodos.



| Método                                       | Descrição                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Adiciona uma única palavra ao **InkWordList**.<br/>                   |
| [**Mescle**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Mescla outro **InkWordList** com este **InkWordList**.<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Remove uma única palavra de um **InkWordList**.<br/>                |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedade de listas de palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Constantes do factor](factoid-constants.md)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

