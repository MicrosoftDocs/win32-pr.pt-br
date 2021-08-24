---
description: O tipo de dados LARGEINT define um \_ valor inteiro grande.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6eedf739d9d0b4285d0198ae905672dbbb7848a2b7d9ba106abb6a59fcdc4d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742646"
---
# <a name="largeint"></a>LARGEINT

O tipo de dados **LARGEINT** define um valor [**\_ inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) .


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Comentários

O membro **lpLargeIntTable** da estrutura [**set**](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais valores LARGEINT. Quando esse tipo de estrutura de **conjunto** é especificado, monitor de rede exibe um dos seguintes rótulos com cada valor de LARGEINT que ele encontra no pacote de protocolo.

-   Corresponde ao valor definido. O valor de LARGEINT é incluído no conjunto.
-   Valor de conjunto desconhecido. O valor de LARGEINT não está incluído no conjunto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

