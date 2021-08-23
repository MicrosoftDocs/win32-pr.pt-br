---
title: SNB (Objidl. h)
description: Um bloco de nome de cadeia de caracteres (SNB) é um ponteiro para uma matriz de ponteiros para cadeias de caracteres, que termina em um ponteiro nulo.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49a7868912b9d7d1e3d9f3b1f82805e6e285d815eacbc559c887febd23e9e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682776"
---
# <a name="snb"></a>SNB

Um bloco de nome de cadeia de caracteres (**SNB**) é um ponteiro para uma matriz de ponteiros para cadeias de caracteres, que termina em um ponteiro **nulo** . Os blocos de nomes de cadeia de caracteres são usados pela interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e por chamadas de função que abrem objetos de armazenamento. As cadeias de caracteres apontam para objetos de armazenamento contidos ou fluxos que devem ser excluídos nas chamadas abertas.


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**SNB**
</dt> <dd>

\[\_marshaling de conexão (wireSNB)\]

</dd> </dl>

## <a name="remarks"></a>Comentários

O **SNB** deve ser criado alocando um bloco contíguo de memória no qual os ponteiros para cadeias de caracteres são seguidos por um ponteiro **NULL** , que é seguido pelas cadeias de caracteres reais.

O marshaling de um **SNB** é baseado na suposição de que o **SNB** que foi passado foi criado dessa maneira. Embora possa ser armazenado de outras maneiras, o **SNB** criado dessa maneira tem a vantagem de exigir apenas uma operação de alocação e uma liberação de memória para todas as cadeias de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Objidl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Objidl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





