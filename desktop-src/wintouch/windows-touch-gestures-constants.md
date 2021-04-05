---
title: Constantes de gestos do Windows Touch (WinUser. h)
description: Esta seção lista as constantes usadas para gestos do Windows Touch.
ms.assetid: C5C3C533-A781-47EF-8209-2D94A94C9097
topic_type:
- apiref
api_name:
- GESTURECONFIGMAXCOUNT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/18/2020
ms.openlocfilehash: be1d8fe9354c7160643dcefb2d35938453ad5b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918494"
---
# <a name="windows-touch-gestures-constants"></a>Constantes de gestos do Windows Touch

Esta seção lista as constantes usadas para gestos do Windows Touch.

<dl> <dt>

**GESTURECONFIGMAXCOUNT**
</dt> <dd> <dl> <dt>

256
</dt> <dt>

Define o número máximo de configurações de gesto que podem ser incluídas em uma única chamada para [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) ou [**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig).

</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |

## <a name="see-also"></a>Confira também

[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig), [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [gestos de toque do Windows](multi-touch-gestures.md)
