---
title: TITLEBAR_TYPE enumeração (Softkbdc.h)
description: Elementos da enumeração TITLEBAR TYPE são usados para especificar tipos de barras de título que estão \_ disponíveis para uma janela de teclado suave.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- TITLEBAR_TYPE enumeração Estrutura de Serviços de Texto
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
ms.openlocfilehash: 941892a7ddbbcac85d66a00a24c1e80f301ab13c8c46f734cae11d074bdff637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950393"
---
# <a name="titlebar_type-enumeration"></a>\_Enumeração TITLEBAR TYPE

Elementos da **enumeração TITLEBAR \_ TYPE** são usados para especificar tipos de barras de título que estão disponíveis para uma janela de teclado suave.

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

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR \_ NONE**
</dt> <dd>

A janela de teclado suave não usa nenhuma barra de título.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR \_ GRIPPER \_ HORIZ \_ ONLY**
</dt> <dd>

A janela de teclado suave usa apenas uma barra de controle horizontal.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR \_ GRIPPER \_ VERTI \_ SOMENTE**
</dt> <dd>

A janela de teclado suave usa apenas uma barra de controle vertical.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**BOTÃO TITLEBAR \_ \_ GRIPPER**
</dt> <dd>

A janela de teclado suave usa apenas um botão de controle.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |



 

 





