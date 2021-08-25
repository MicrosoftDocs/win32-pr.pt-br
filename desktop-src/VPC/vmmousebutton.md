---
title: Enumeração VMMouseButton (VPCCOMInterfaces. h)
description: Especifica o botão do mouse.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- VMMouseButton de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4922942ee72971e1bd0d0aaa14336b09c7ede804f83b865779b851f4dfff463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006506"
---
# <a name="vmmousebutton-enumeration"></a>Enumeração VMMouseButton

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica o botão do mouse.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton \_ à esquerda**
</dt> <dd>

O botão esquerdo do mouse.

</dd> <dt>

<span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton \_ à direita**
</dt> <dd>

O botão direito do mouse.

</dd> <dt>

<span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton \_ Center**
</dt> <dd>

O botão central do mouse.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

