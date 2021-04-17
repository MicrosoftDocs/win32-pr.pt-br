---
title: Estrutura ICONRESDIR
description: Contém as dimensões e o formato de cor de uma imagem de ícone individual em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Menus de estrutura ICONRESDIR e outros recursos
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753895"
---
# <a name="iconresdir-structure"></a>Estrutura ICONRESDIR

Contém as dimensões e o formato de cor de uma imagem de ícone individual em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a>Membros

<dl> <dt>

**Largura**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

A largura do ícone, em pixels. Os valores aceitáveis são 16, 32 e 64.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

A altura do ícone, em pixels. Os valores aceitáveis são 16, 32 e 64.

</dd> <dt>

**ColorCount**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

O número de cores no ícone. Os valores aceitáveis são 2, 8 e 16.

</dd> <dt>

**reservado**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Reservado deve ser definido com o mesmo valor do campo reservado no cabeçalho do arquivo de ícone.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **ICONRESDIR** será passada na estrutura [**RESDIR**](resdir.md) se a estrutura **RESDIR** descrever um ícone.

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

 

 





