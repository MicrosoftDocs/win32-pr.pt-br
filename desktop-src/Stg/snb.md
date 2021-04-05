---
title: SNB (Objidl. h)
description: Um bloco de nome de cadeia de caracteres (SNB) é um ponteiro para uma matriz de ponteiros para cadeias de caracteres, que termina em um ponteiro nulo.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918221"
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
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Objidl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Objidl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





