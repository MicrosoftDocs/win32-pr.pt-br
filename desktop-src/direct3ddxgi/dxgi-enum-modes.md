---
description: Opções para enumeração de modos de exibição.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105754087"
---
# <a name="dxgi_enum_modes"></a>\_modos de enumeração dxgi \_

Opções para enumeração de modos de exibição.



| Constante/valor                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**Dxgi \_ Modos de enumeração \_ \_ entrelaçados**</dt> <dt>1UL</dt> </dl>                 | Incluir modos entrelaçados.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**Dxgi \_ 2UL \_ de \_ dimensionamento de modos de enumeração**</dt> <dt></dt> </dl>                          | Incluir modos de dimensionamento ampliado.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**Dxgi \_ Modos de enumeração 4UL \_ \_ estéreo**</dt> <dt></dt> </dl>                             | Incluir modos estéreo.<br/> **Direct3D 11:** Esse valor de enumeração tem suporte a partir do Windows 8.<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**Dxgi \_ Modos de enumeração \_ \_ desabilitados 8UL \_ estéreo**</dt> <dt></dt> </dl> | Incluir modos estéreo ocultos porque o usuário desabilitou o estéreo. Os aplicativos do painel de controle podem usar essa opção para mostrar os recursos de estéreo que foram desabilitados como parte de uma interface do usuário que habilita e desabilita o estéreo.<br/> **Direct3D 11:** Esse valor de enumeração tem suporte a partir do Windows 8.<br/> |



## <a name="remarks"></a>Comentários

Essas opções de sinalizador são usadas em [**IDXGIOutput:: Getdisplaymodelist**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) para enumerar os modos de exibição.

Essas opções de sinalizador também são usadas em [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) para enumerar modos de exibição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




