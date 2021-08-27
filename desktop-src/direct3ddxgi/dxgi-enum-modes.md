---
description: Opções para enumerar modos de exibição.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 568e3919955c2f5612cf88896a2cb6389ebc58fcb427e159824c1dc2feeebca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025626"
---
# <a name="dxgi_enum_modes"></a>MODOS DE ENUM DXGI \_ \_

Opções para enumerar modos de exibição.



| Constante/valor                                                                                                                                                                                                                                                                  | Descrição                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**DXGI \_ MODOS DE \_ ENUM \_ ENTRELAÇADOS**</dt> <dt>1UL</dt> </dl>                 | Inclua modos entrelaçados.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**DXGI \_ MODOS ENUM \_ \_ DIMENSIONANDO**</dt> <dt>2UL</dt> </dl>                          | Inclua modos de dimensionamento estendido.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**DXGI \_ MODOS ENUM \_ \_ ESTÉREO**</dt> <dt>4UL</dt> </dl>                             | Inclua modos estéreo.<br/> **Direct3D 11:** Esse valor de enumeração tem suporte a partir do Windows 8.<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**DXGI \_ MODOS DE ENUM \_ \_ DESABILITADOS \_ ESTÉREO**</dt> <dt>8UL</dt> </dl> | Inclua modos estéreos que estão ocultos porque o usuário desabilitou estéreo. Os aplicativos do painel de controle podem usar essa opção para mostrar recursos estéreos que foram desabilitados como parte de uma interface do usuário que habilita e desabilita estéreo.<br/> **Direct3D 11:** Esse valor de enumeração tem suporte a partir do Windows 8.<br/> |



## <a name="remarks"></a>Comentários

Essas opções de sinalizador são usadas [**em IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) para enumerar modos de exibição.

Essas opções de sinalizador também são usadas [**em IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) para enumerar modos de exibição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




