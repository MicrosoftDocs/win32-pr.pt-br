---
description: Define os níveis de multisampling de cena completa que o dispositivo pode aplicar.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: D3DMULTISAMPLE_TYPE enumeração (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6173abf04f42b0632441b436706318796a5d0af758928e61dd3f19d30bda881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027966"
---
# <a name="d3dmultisample_type-enumeration"></a>Enumeração DE TIPO D3DMULTISAMPLE \_

Define os níveis de multisampling de cena completa que o dispositivo pode aplicar.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ NONE**
</dt> <dd>

Nenhum nível de multisampling de cena completa está disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE \_ NÃO MASKABLE** 
</dt> <dd>

Habilita o valor de qualidade de vários exemplos. Consulte Observações.

</dd> <dt>

<span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**EXEMPLOS DE D3DMULTISAMPLE \_ 2 \_**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**EXEMPLOS DE D3DMULTISAMPLE \_ 3 \_**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**EXEMPLOS DE D3DMULTISAMPLE \_ 4 \_**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE \_ 5 \_ EXEMPLOS**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**EXEMPLOS DE D3DMULTISAMPLE \_ 6 \_**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**EXEMPLOS DE D3DMULTISAMPLE \_ 7 \_**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**EXEMPLOS DE D3DMULTISAMPLE \_ 8 \_**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**EXEMPLOS DE D3DMULTISAMPLE \_ 9 \_**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE \_ 10 \_ AMOSTRAS**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE \_ 11 \_ SAMPLES**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE \_ 12 \_ AMOSTRAS**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE \_ 13 \_ SAMPLES**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE \_ 14 \_ AMOSTRAS**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE \_ 15 \_ EXEMPLOS**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE \_ 16 \_ EXEMPLOS**
</dt> <dd>

Nível de multisampling de cena completa disponível.

</dd> <dt>

<span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Além de habilizar a multisampling de cena completa em [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, haverá estados de renderização que ativam e desligam vários aspectos em níveis finos.

A multisampling é válida somente em uma cadeia de permuta que está sendo criada ou redefinida com o efeito de permuta D3DSWAPEFFECT \_ DISCARD.

O valor de antialiação multisample pode ser definido com os parâmetros (ou subparâmetros) nos métodos a seguir.



| Método                                                                                             | Parâmetros                         | Submetr parâmetros                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | MultiSampleType e pQualityLevels |                                    |
| [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | pPresentationParameters            | MultiSampleType e pQualityLevels |
| [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | pPresentationParameters            | MultiSampleType e pQualityLevels |
| [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | MultiSampleType e pQualityLevels |                                    |
| [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | MultiSampleType e pQualityLevels |                                    |
| [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | pPresentationParameters            | MultiSampleType e pQualityLevels |



 

Não é uma boa prática alternar de um tipo multisample para outro para aumentar a qualidade da aninhamento.

D3DMULTISAMPLE NONE permite efeitos de permuta que não sejam o \_ descarte, o bloqueio e assim por diante.

Se o dispositivo de exibição dá suporte a multiampling maskable (mais de uma amostra para um formato de destino de renderização de vários exemplos mais suporte a antialias) ou apenas multisampling não maskable (somente suporte a antialias), o driver do dispositivo fornece o número de níveis de qualidade para o tipo de vários exemplos D3DMULTISAMPLE \_ NONMASKABLE. Os aplicativos que usam apenas multisampling para fins de antialiação só precisam consultar o número de níveis de qualidade de várias amostras não maskáveis que o driver dá suporte.

Os níveis de qualidade com suporte pelo dispositivo podem ser obtidos com o parâmetro pQualityLevels [**de IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype). Os níveis de qualidade usados pelo aplicativo são definidos com o parâmetro MultiSampleQuality [**de IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) [**e IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).

Consulte D3DRS \_ MULTISAMPLEMASK para discutir sobre multisampling maskable.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**PARÂMETROS D3DPRESENT \_**](d3dpresent-parameters.md)
</dt> <dt>

[**D3DSURFACE \_ DESC**](d3dsurface-desc.md)
</dt> </dl>

 

 
