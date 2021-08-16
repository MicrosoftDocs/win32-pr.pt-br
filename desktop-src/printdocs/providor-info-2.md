---
description: A estrutura PROVIDOR \_ INFO \_ 2 anexa um provedor de impressão à lista de pedido do provedor de impressão.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: PROVIDOR_INFO_2 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 969af36fe0a64bb586fbf62912ca27c6ebba9ba0a627701e4bc57f6202bfe1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091676"
---
# <a name="providor_info_2-structure"></a>Estrutura PROVIDOR \_ INFO \_ 2

A **estrutura PROVIDOR \_ INFO \_ 2** anexa um provedor de impressão à lista de pedido do provedor de impressão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**pOrder**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do provedor de impressão.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada ao chamar [**AddPrintProvidor**](addprintprovidor.md), nível 2, para adicionar o provedor de impressão especificado ao final da lista de pedido do provedor de impressão. O provedor será usado imediatamente para roteamento se a chamada for bem-sucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ PROVIDOR \_ INFO \_ 2W** (Unicode) e **\_ PROVIDOR \_ INFO \_ 2A** (ANSI)<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




