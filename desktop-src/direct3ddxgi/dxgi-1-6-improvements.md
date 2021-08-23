---
description: Este tópico descreve o que há de novo na infra-estrutura de gráficos do Microsoft DirectX (DXGI) 1,6 para várias versões do Windows 10.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: Aprimoramentos de DXGI 1,6
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 748878cc041b0987a013608556cd9ec30aaf638e0fcac1ef9386a4675f57ef0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727576"
---
# <a name="dxgi-16-improvements"></a>Aprimoramentos de DXGI 1,6

Este tópico descreve o que há de novo na infra-estrutura de gráficos do Microsoft DirectX (DXGI) 1,6 para várias versões do Windows 10.

## <a name="windows-10-october-2018-update"></a>Atualização de outubro de 2018 para o Windows 10

essas APIs foram adicionadas para o Windows 10, versão 1809 (10,0; Build 17763) &mdash; também conhecido como Atualização de outubro de 2018 para o Windows 10.

- Interface [**IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) e seus métodos.

## <a name="windows-10-april-2018-update"></a>Atualização de abril de 2018 do Windows 10

essas APIs foram adicionadas para Windows 10, versão 1803 (10,0; Build 17134) &mdash; também conhecido como Windows 10 atualização de abril de 2018.

- Enumeração de [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) .
- Interface [**IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) e seus métodos.

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

por Windows 10, versão 1709 (10,0; Build 16299) &mdash; também conhecido como Windows 10 Fall Creators Update &mdash; essas constantes foram adicionadas à enumeração [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) . 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Atualização do Windows 10 para Criadores

por Windows 10, versão 1703 (10,0; o Build 15063) &mdash; também é conhecido como Atualização do Windows 10 para Criadores &mdash; a seguinte funcionalidade foi adicionada à Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 para detectar exibições HDR.

### <a name="high-dynamic-range-hdr-detection"></a>Detecção de grande alcance de intervalo dinâmico (HDR)

Essas APIs foram adicionadas para detectar exibições HDR.

- Estrutura de [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3)
- Enumeração de [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)
- Enumeração de [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)
- Estrutura de [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)
- Função [**DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)
- Interface [**IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) e seus métodos
- Interface [**IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) e seus métodos

Além disso, as constantes foram adicionadas à enumeração de [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) para dar suporte a essas APIs.

## <a name="related-topics"></a>Tópicos relacionados
[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
