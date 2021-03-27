---
title: Parâmetros de criação de recursos por lado
description: Há algumas restrições sobre o tipo de recursos do Direct3D que você pode criar com o sinalizador diD3D11 de \_ recursos diversos do recurso \_ \_ . Esta seção fornece os parâmetros válidos para a criação de recursos em ladrilho.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/13/2019
ms.locfileid: "103638845"
---
# <a name="tiled-resource-creation-parameters"></a>Parâmetros de criação de recursos por lado

Há algumas restrições sobre o tipo de recursos do Direct3D que você pode criar com o sinalizador [**diD3D11 de \_ recursos \_ diversos \_ do recurso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . Esta seção fornece os parâmetros válidos para a criação de recursos em ladrilho.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo de recurso com suporte**
</dt> <dd>

\[Matriz Texture2D \] (incluindo \[ matriz TextureCube \] , que é uma variante da \[ matriz Texture2D \] ) ou buffer.

**Sem suporte:** Texture1D \[ array \] ou Texture3D, mas o Texture3D pode ter suporte no futuro.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos com suporte**
</dt> <dd>

Padrão de uso de D3D11 \_ \_ .

**Sem suporte:** Uso \_ \_ dinâmico de D3D11, \_ preparo de uso de D3D11 \_ ou \_ uso \_ inalterável de D3D11.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Sinalizadores diversos de recurso com suporte**
</dt> <dd>

\_Recurso D3D11 \_ misc. \_ lado a lado (por definição), \_ misc \_ TEXTURECUBE, \_ DRAWINDIRECT \_ args, \_ buffer \_ permite \_ \_ exibições brutas, \_ buffer \_ estruturado, \_ Resource \_ fixe ou \_ gerar \_ MIPS.

**Sem suporte:** \_ COMPARTILHAMENTO compartilhado \_ , \_ KEYEDMUTEX compartilhado \_ , \_ compatível com GDI, \_ \_ NTHANDLE compartilhados, \_ \_ conteúdo restrito, \_ restringir \_ \_ recurso compartilhado, \_ restringir \_ \_ \_ Driver de recurso compartilhado, \_ protegido ou \_ pool de blocos \_ .

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Sinalizadores de associação com suporte**
</dt> <dd>

\_Recurso D3D11 BIND \_ Shader \_ , \_ destino de renderização \_ , \_ \_ estêncil de profundidade ou \_ acesso não ordenado \_ .

**Sem suporte:** \_ Buffer de constantes \_ , o \_ buffer de vértice \_ \[ Observe que a associação de um buffer de ladrilhos como SRV/UAV/RTV ainda é ok \] , \_ \_ buffer de índice, \_ \_ saída de fluxo, \_ \_ decodificador de associação ou \_ \_ codificador de vídeo de ligação \_ .

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formatos com suporte**
</dt> <dd>

Todos os formatos que devem estar disponíveis para determinada configuração, independentemente dela ser lado a lado, com algumas exceções.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc com suporte (contagem de multiamostras, qualidade)**
</dt> <dd>

Tudo o que seria suportado para a configuração fornecida, independentemente dela ser lado a lado, com algumas exceções.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Largura/altura/MipLevels/matrizes com suporte**
</dt> <dd>

Extensões completas com suporte do Direct3D 11. Os recursos em ladrilho não têm a restrição sobre o tamanho total da memória imposta em recursos que não são de lado do ladrilho. Os recursos em ladrilhos são restritos pelos limites gerais de espaço de endereço virtual. Para obter informações, consulte [espaço de endereço disponível para recursos em ladrilho](address-space-available-for-tiled-resources.md).

</dd> </dl>

O conteúdo inicial da memória do pool de bloco é indefinido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos em ladrilhos](creating-tiled-resources.md)
</dt> </dl>

 

 




