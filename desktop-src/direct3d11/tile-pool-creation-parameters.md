---
title: Parâmetros de criação de pool de blocos
description: Use os parâmetros nesta seção para definir pools de blocos por meio da API CreateBuffer ID3D11Device.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005039"
---
# <a name="tile-pool-creation-parameters"></a>Parâmetros de criação de pool de blocos

Use os parâmetros nesta seção para definir pools de blocos por meio da API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) .

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Tamanho**
</dt> <dd>

Tamanho da alocação, como um múltiplo de 64 KB. 0 é válido porque você pode usar posteriormente uma operação [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) .

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Sinalizadores diversos de recurso com suporte**
</dt> <dd>

\_ \_ \_ Pool de blocos diversos \_ do recurso D3D11 (identifica o recurso como um pool de blocos), D3D11 \_ \_ de recursos diversos \_ compartilhado, \_ \_ KEYEDMUTEX compartilhados ou \_ \_ NTHANDLE compartilhados.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos com suporte**
</dt> <dd>

\_Somente padrão de uso D3D11 \_ .

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos em ladrilhos](creating-tiled-resources.md)
</dt> </dl>

 

 




