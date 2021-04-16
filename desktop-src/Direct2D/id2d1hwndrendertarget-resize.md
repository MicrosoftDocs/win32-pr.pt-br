---
title: Métodos de redimensionamento de ID2D1HwndRenderTarget (D2d1. h)
description: Altera o tamanho do destino de renderização para o tamanho de pixel especificado.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Redimensionar métodos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750922"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>Métodos ID2D1HwndRenderTarget:: Resize

Altera o tamanho do destino de renderização para o tamanho de pixel especificado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                         | Descrição                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Redimensionar (D2D1 \_ tamanho \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Altera o tamanho do destino de renderização para o tamanho de pixel especificado. <br/> |
| [**Redimensionar ( \_ tamanho de d2d1 \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Altera o tamanho do destino de renderização para o tamanho de pixel especificado.<br/>  |



## <a name="remarks"></a>Comentários

Depois que esse método é chamado, o conteúdo do buffer de fundo do destino de renderização não é definido, mesmo que a opção [**d2d1 \_ apresente as opções de retenção de \_ \_ \_ conteúdo**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) tenha sido especificada quando o destino de renderização foi criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
