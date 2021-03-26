---
title: Direct3D 11 em hardware de nível inferior
description: Esta seção discute como o Direct3D 11 foi projetado para dar suporte a hardware novo e existente, do DirectX 9 ao DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104562420"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>Direct3D 11 em hardware de nível inferior

Esta seção discute como o Direct3D 11 foi projetado para dar suporte a hardware novo e existente, do DirectX 9 ao DirectX 11.

Este diagrama mostra como o Direct3D 11 dá suporte a hardware novo e existente.

![diagrama do hardware ao qual o Direct3D 11 dá suporte](images/d3d11-on-downlevel-hardware.png)

Com o Direct3D 11, é introduzido um novo paradigma chamado níveis de recursos. Um nível de recurso é um conjunto bem definido de funcionalidades de GPU. Usando um nível de recurso, você pode direcionar um aplicativo Direct3D para ser executado em uma versão de nível inferior do hardware do Direct3D.

A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                  | Descrição                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Níveis de recursos do Direct3D](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | Este tópico discute os níveis de recurso do Direct3D.<br/>                                                                                                                       |
| [Exceções](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | Este tópico descreve as exceções ao usar o Direct3D 11 em hardware de nível inferior. <br/>                                                                                      |
| [Sombreadores de computação em hardware de nível inferior](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | Este tópico discute como usar [sombreadores de computação](direct3d-11-advanced-stages-compute-shader.md) em um aplicativo do Direct3D 11 no hardware do Direct3D 10.<br/>             |
| [Impedindo SRVs de sombreador de pixel nulo indesejado](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | Este tópico discute como contornar o driver recebendo exibições de recurso de sombreador **nulo** (SRVs) mesmo quando SRVs não **nulo** estão associados ao estágio de sombreador de pixel.<br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>Tópicos sobre como obter os níveis de recurso



| Tópico                                                                                                                                                                                                                                                                   | Descrição                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Como: obter o nível de recurso do dispositivo](overviews-direct3d-11-devices-downlevel-get.md)<br/> | Como obter um nível de recurso.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





