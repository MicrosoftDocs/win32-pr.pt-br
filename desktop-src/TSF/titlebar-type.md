---
title: Enumeração de TITLEBAR_TYPE (Softkbdc. h)
description: Os elementos da \_ enumeração de tipo TITLEBAR são usados para especificar tipos de titlebars que estão disponíveis para uma janela de teclado flexível.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- Estrutura de serviços de texto de enumeração TITLEBAR_TYPE
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105792635"
---
# <a name="titlebar_type-enumeration"></a>\_Enumeração de tipo TITLEBAR

Os elementos da enumeração de **\_ tipo TITLEBAR** são usados para especificar tipos de titlebars que estão disponíveis para uma janela de teclado flexível.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR \_ nenhum**
</dt> <dd>

A janela teclado soft não usa nenhuma TitleBar.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**\_garra da TITLEBAR \_ \_ somente horizontal**
</dt> <dd>

A janela teclado soft usa apenas uma barra de garra horizontal.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**\_garra da TITLEBAR \_ somente verticalmente \_**
</dt> <dd>

A janela teclado soft usa apenas uma barra vertical.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**botão de garra da TITLEBAR \_ \_**
</dt> <dd>

A janela teclado soft usa apenas um botão de garra.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





