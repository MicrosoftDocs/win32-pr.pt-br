---
description: A interface ID3DXRenderToEnvMap é usada para generalizar o processo de renderização para mapas de ambiente.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Interface ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752178"
---
# <a name="id3dxrendertoenvmap-interface"></a>Interface ID3DXRenderToEnvMap

A interface ID3DXRenderToEnvMap é usada para generalizar o processo de renderização para mapas de ambiente.

## <a name="members"></a>Membros

A interface **ID3DXRenderToEnvMap** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToEnvMap** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXRenderToEnvMap** tem esses métodos.



| Método                                                          | Descrição                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginCube**](id3dxrendertoenvmap--begincube.md)             | Inicie a renderização de um mapa de ambiente cúbico.<br/>                                                                                                                                    |
| [**BeginHemisphere**](id3dxrendertoenvmap--beginhemisphere.md) | Inicie a renderização de um mapa de ambiente Hemispheric.<br/>                                                                                                                              |
| [**BeginParabolic**](id3dxrendertoenvmap--beginparabolic.md)   | Inicie a renderização de um mapa de ambiente parabólico.<br/>                                                                                                                                |
| [**BeginSphere**](id3dxrendertoenvmap--beginsphere.md)         | Inicie a renderização de um mapa de ambiente esférico.<br/>                                                                                                                                |
| [**Completo**](id3dxrendertoenvmap--end.md)                         | Restaurar todos os destinos de renderização e, se necessário, compor todas as faces renderizadas na superfície do mapa do ambiente.<br/>                                                                           |
| [**Detecção Facial**](id3dxrendertoenvmap--face.md)                       | Inicie o desenho de cada face de um mapa de ambiente.<br/>                                                                                                                              |
| [**GetDesc**](id3dxrendertoenvmap--getdesc.md)                 | Recupera a descrição da superfície de renderização.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertoenvmap--getdevice.md)             | Recupera o dispositivo Direct3D associado ao mapa de ambiente.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertoenvmap--onlostdevice.md)       | Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.<br/> |
| [**OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)     | Use este método para readquirir recursos e salvar o estado inicial.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Um mapa de ambiente é usado para a geometria da cena de mapa de textura para fornecer uma cena mais sofisticada sem usar geometria complexa. Esta interface dá suporte à criação de superfícies para os seguintes tipos de geometria: Cube, meia Sphere ou Hemispheric, parabólico ou Sphere.

A interface **ID3DXRenderToEnvMap** é obtida chamando a função [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .

O tipo LPD3DXRenderToEnvMap é definido como um ponteiro para a interface **ID3DXRenderToEnvMap** .


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
