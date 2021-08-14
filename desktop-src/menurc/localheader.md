---
title: Estrutura LOCALHEADER
description: Contém as coordenadas x e y de um hotspot associado ao cursor identificado por uma estrutura RESDIR. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Menus de estrutura LOCALHEADER e outros recursos
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ec46b802b847b73c99cc81939531d8f9ec1a6a2e0addb4c928d5610ac5b80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870314"
---
# <a name="localheader-structure"></a>Estrutura LOCALHEADER

Contém as coordenadas x e y de um hotspot associado ao cursor identificado por uma estrutura [**RESDIR**](resdir.md) . A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**xHotSpot**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A coordenada x do ponto de acesso do cursor, em pixels.

</dd> <dt>

**yHotSpot**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A coordenada y do ponto de acesso do cursor, em pixels.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **LOCALHEADER** é o primeiro dado gravado no recurso [de \_ cursor de RT](/windows/desktop/menurc/resource-types) se uma estrutura [**RESDIR**](resdir.md) contém informações sobre um cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CURSORDIR**](cursordir.md)
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

