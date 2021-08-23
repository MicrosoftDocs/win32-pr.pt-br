---
title: Direct3D 11 no hardware de nível baixo
description: Esta seção discute como o Direct3D 11 foi projetado para dar suporte a hardwares novos e existentes, do DirectX 9 ao DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb9dde5bfaa32808752206ebe96702aaaf10cc39c1e053675ddfced765331be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045504"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>Direct3D 11 no hardware de nível baixo

Esta seção discute como o Direct3D 11 foi projetado para dar suporte a hardwares novos e existentes, do DirectX 9 ao DirectX 11.

Este diagrama mostra como o Direct3D 11 dá suporte a hardware novo e existente.

![diagrama do hardware compatível com o Direct3d 11](images/d3d11-on-downlevel-hardware.png)

Com o Direct3D 11, um novo paradigma é introduzido chamado níveis de recurso. Um nível de recurso é um conjunto bem definido de funcionalidades de GPU. Usando um nível de recurso, você pode direcionar um aplicativo Direct3D para ser executado em uma versão de nível inferior do hardware Direct3D.

A seção [Referência 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre como vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportam em vários níveis de recurso 10Level9.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                  | Descrição                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Níveis de recursos do Direct3D](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | Este tópico discute os níveis de recursos do Direct3D.<br/>                                                                                                                       |
| [Exceções](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | Este tópico descreve exceções ao usar o Direct3D 11 em hardware de nível baixo. <br/>                                                                                      |
| [Sombreadores de computação no hardware de nível baixo](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | Este tópico discute como usar [](direct3d-11-advanced-stages-compute-shader.md) sombreadores de computação em um aplicativo Direct3D 11 no hardware do Direct3D 10.<br/>             |
| [Impedindo SRVs de sombreador de pixel nulo indesejado](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | Este tópico discute como resolver o driver que está recebendo SRVs (exibições de recurso de sombreador **NULL)** mesmo quando SRVs não **NULL** estão vinculados ao estágio do sombreador de pixel.<br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>Tópicos sobre níveis de recursos



| Tópico                                                                                                                                                                                                                                                                   | Descrição                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Como obter o nível de recurso do dispositivo](overviews-direct3d-11-devices-downlevel-get.md)<br/> | Como obter um nível de recurso.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





