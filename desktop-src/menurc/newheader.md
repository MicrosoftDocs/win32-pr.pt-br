---
title: Estrutura NEWHEADER
description: Contém o número de componentes de ícone ou cursor em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menus de estrutura NEWHEADER e outros recursos
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918125"
---
# <a name="newheader-structure"></a>Estrutura NEWHEADER

Contém o número de componentes de ícone ou cursor em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Reserved**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Reservado deve ser zero.

</dd> <dt>

**ResType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tipo de recurso. Esse membro deve ter um dos valores a seguir.



| Valor                                                                                                                                                                                                       | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <dt>**Res \_ CURSOR**</dt> <dt>2</dt> </dl> | Tipo de recurso de cursor.<br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <dt>**Res \_ ÍCONE**</dt> <dt>1</dt> </dl>       | Tipo de recurso de ícone.<br/>   |



 

</dd> <dt>

**ResCount**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de componentes de ícone ou cursor no grupo de recursos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma ou mais estruturas [**RESDIR**](resdir.md) seguem imediatamente a estrutura **NEWHEADER** no arquivo. res. O membro **ResCount** especifica o número de estruturas **RESDIR** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





