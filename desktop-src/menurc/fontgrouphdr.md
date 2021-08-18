---
title: Estrutura FONTGROUPHDR
description: Contém as informações necessárias para que um aplicativo acesse uma fonte específica. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menus de estrutura FONTGROUPHDR e outros recursos
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51b307b7f5798a57e344096fe46227edf97babbf3547c4c851d71fd8ecdc28da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734474"
---
# <a name="fontgrouphdr-structure"></a>Estrutura FONTGROUPHDR

Contém as informações necessárias para que um aplicativo acesse uma fonte específica. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a>Membros

<dl> <dt>

**NumberOfFonts**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de fontes individuais associadas a este recurso.

</dd> <dt>

**DE**
</dt> <dd>

Tipo: **[ **dialuguel**](direntry.md)**

</dd> <dd>

Uma estrutura que contém um identificador ordinal exclusivo para cada fonte no recurso. O membro **de** é um espaço reservado para a matriz de comprimento variável de estruturas de [**dialuguel**](direntry.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **FONTGROUPHDR** segue os dados para as fontes individuais no. Arquivo Res. O compilador de recurso adiciona automaticamente a estrutura **FONTGROUPHDR** , geralmente como a última entrada no arquivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Dialugado**](direntry.md)
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





