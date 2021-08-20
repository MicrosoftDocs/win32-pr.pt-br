---
title: Parâmetros de criação de recursos lado a lado
description: Há algumas restrições no tipo de recursos direct3D que você pode criar com o sinalizador D3D11 \_ RESOURCE \_ MISC \_ TILED. Esta seção fornece os parâmetros válidos para criar recursos lado a lado.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9668c21060cbb8f39884204780ce689b3e67196aef0bdcfef891836768f04af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279836"
---
# <a name="tiled-resource-creation-parameters"></a>Parâmetros de criação de recursos lado a lado

Há algumas restrições no tipo de recursos direct3D que você pode criar com o sinalizador [**D3D11 \_ RESOURCE \_ MISC \_ TILED.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Esta seção fornece os parâmetros válidos para criar recursos lado a lado.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo de recurso com suporte**
</dt> <dd>

Matriz Texture2D \[ \] (incluindo TextureCube \[ \] Array, que é uma variante da Matriz Texture2D \[ ) ou \] buffer.

**SEM suporte:** Texture1D \[ Array \] ou Texture3D, mas Texture3D pode ter suporte no futuro.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos com suporte**
</dt> <dd>

D3D11 \_ USAGE \_ DEFAULT.

**SEM suporte:** D3D11 \_ USO \_ DINÂMICO, D3D11 PREPARAÇÃO DE USO \_ ou USO \_ D3D11 \_ \_ IMUTÁVEL.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Sinalizadores de misc de recursos com suporte**
</dt> <dd>

D3D11 \_ RESOURCE \_ \_ MISC TILED (por definição), \_ MISC \_ TEXTURECUBE, \_ DRAWINDIRECT ARGS, BUFFER ALLOW RAW \_ \_ \_ \_ \_ VIEWS, BUFFER \_ \_ STRUCTURED, RESOURCE FIX ou GENERATE \_ \_ \_ \_ MIPS.

**SEM suporte:** \_ SHARED, \_ SHARED \_ KEYEDMUTEX, \_ GDI \_ COMPATIBLE, SHARED \_ \_ NTHANDLE, NTHANDLE, RESTRICTED CONTENT, RESTRICT SHARED \_ \_ \_ \_ \_ RESOURCE, RESTRICT SHARED RESOURCE \_ \_ DRIVER, GUARDED ou \_ \_ \_ \_ TILE \_ POOL.

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Sinalizadores de vinculação com suporte**
</dt> <dd>

RECURSO DE SOMBREADOR DE VINCULAÇÃO D3D11, \_ \_ DESTINO DE \_ \_ \_ RENDERIZAÇÃO, \_ ESTÊNCIL DE PROFUNDIDADE OU ACESSO NÃO \_ \_ \_ ORGANIZADO.

**SEM suporte:** \_ BUFFER CONSTANTE, BUFFER DE VÉRTICE observe que a associação de um Buffer lado a lado como \_ \_ um \_ \[ SRV/UAV/RTV ainda é ok , BUFFER DE ÍNDICE, SAÍDA DE \] \_ \_ \_ \_ FLUXO, BIND \_ DECODER ou BIND VIDEO \_ \_ \_ \_ ENCODER.

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formatos com suporte**
</dt> <dd>

Todos os formatos que devem estar disponíveis para determinada configuração, independentemente dela ser lado a lado, com algumas exceções.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc com suporte (contagem de várias amostras, qualidade)**
</dt> <dd>

Tudo o que seria suportado para a configuração fornecida, independentemente dela ser lado a lado, com algumas exceções.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Largura/altura/MipLevels/ArraySize com suporte**
</dt> <dd>

Extensão completa com suporte do Direct3D 11. Os recursos lado a lado não têm a restrição de tamanho total de memória imposta a recursos não lado a lado. Os recursos lado a lado são restritos apenas pelos limites gerais de espaço de endereço virtual. Para obter informações, consulte [Espaço de endereço disponível para recursos lado a lado.](address-space-available-for-tiled-resources.md)

</dd> </dl>

O conteúdo inicial da memória do pool de bloco é indefinido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos lado a lado](creating-tiled-resources.md)
</dt> </dl>

 

 




