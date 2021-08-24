---
title: O dispositivo D1112 deve ser DX11
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: O dispositivo associado à superfície DXGI deve ser um dispositivo D3D11.
keywords:
- O dispositivo D1112 deve ser DX11 Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 24c8bf123d9e00eff90f216676ec03f7d68cbe692511118c36c1433cbf0354d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758106"
---
# <a name="d1112-device-must-be-dx11"></a>D1112: o dispositivo deve ser DX11

O dispositivo associado à superfície DXGI deve ser um dispositivo D3D11.



| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nível de erro | Aviso |



 

## <a name="possible-causes"></a>Possíveis causas

Houve uma tentativa de usar [**o CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) com uma superfície DXGI criada por um dispositivo não Direct3D11.

 

 




