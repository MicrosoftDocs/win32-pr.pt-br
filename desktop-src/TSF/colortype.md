---
title: Enumeração COLORtype (Softkbdc. h)
description: Os elementos da enumeração COLORtype são usados para especificar tipos de cores que estão disponíveis para um teclado virtual.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Estrutura de serviços de texto de enumeração COLORtype
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755527"
---
# <a name="colortype-enumeration"></a>Enumeração COLORtype

Os elementos da enumeração **ColorType** são usados para especificar tipos de cores que estão disponíveis para um teclado virtual.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**
</dt> <dd>

Cor do plano de fundo.

</dd> <dt>

<span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**
</dt> <dd>

Cor de primeiro plano não selecionada.

</dd> <dt>

<span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**
</dt> <dd>

Cor do texto não selecionada.

</dd> <dt>

<span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**
</dt> <dd>

Cor de primeiro plano selecionada.

</dd> <dt>

<span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**
</dt> <dd>

Cor do texto selecionada.

</dd> <dt>

<span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**\_Tipo de cor máximo \_**
</dt> <dd>

Tipo de cor máximo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





