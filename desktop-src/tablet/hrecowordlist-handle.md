---
description: Um identificador HRECOWORDLIST é usado para gerenciar uma lista de palavras anexada a um contexto de reconhecedor. Você usa uma lista de palavras para melhorar os resultados de reconhecimento.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Identificador HRECOWORDLIST (recapitular. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501829"
---
# <a name="hrecowordlist-handle"></a>Identificador de HRECOWORDLIST

Um identificador **HRECOWORDLIST** é usado para gerenciar uma lista de palavras anexada a um contexto de reconhecedor. Você usa uma lista de palavras para melhorar os resultados de reconhecimento.


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a>Comentários

A função a seguir usa um **HRECOWORDLIST**.



| Função                                         | Descrição                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [**AddWordsToWordList**](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | Adiciona uma ou mais palavras à lista de palavras.<br/> |
| [**DestroyWordList**](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | Destrói a lista atual de palavras.<br/>          |
| [**MakeWordList**](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | Cria uma lista de palavras.<br/>                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Recapitular. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Função setwordlist**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




