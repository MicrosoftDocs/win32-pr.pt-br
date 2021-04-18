---
description: A \_ estrutura PROVIDOR info \_ 2 acrescenta um provedor de impressão à lista de pedidos do provedor de impressão.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Estrutura de PROVIDOR_INFO_2 (winspool. h)
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
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810412"
---
# <a name="providor_info_2-structure"></a>Estrutura de informações de PROVIDOR \_ \_ 2

A estrutura **PROVIDOR \_ info \_ 2** acrescenta um provedor de impressão à lista de pedidos do provedor de impressão.

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

Essa estrutura é usada ao chamar [**AddPrintProvidor**](addprintprovidor.md), nível 2, para adicionar o provedor de impressão especificado ao final da lista de pedidos do provedor de impressão. O provedor será usado imediatamente para roteamento se a chamada for realizada com sucesso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ PROVIDOR \_ info \_ 2W** (Unicode) e **\_ PROVIDOR \_ info \_ 2a** (ANSI)<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




