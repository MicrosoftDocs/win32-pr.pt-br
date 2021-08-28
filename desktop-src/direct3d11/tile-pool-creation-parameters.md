---
title: Parâmetros de criação de pool de blocos
description: Use os parâmetros nesta seção para definir pools de partes por meio da API ID3D11Device CreateBuffer.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7350dc01c845542b97674189a120c0d55db95c282dc80b11fda66230618f99b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119466"
---
# <a name="tile-pool-creation-parameters"></a>Parâmetros de criação de pool de blocos

Use os parâmetros nesta seção para definir pools de partes por meio da API [**ID3D11Device::CreateBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Tamanho**
</dt> <dd>

Tamanho da alocação, como um múltiplo de 64 KB. 0 é válido porque você pode usar posteriormente uma [**operação ID3D11DeviceContext2::ResizeTilePool.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Sinalizadores de misc de recursos com suporte**
</dt> <dd>

POOL DE PEÇAS DO MISC DO RECURSO D3D11 (identifica o recurso como um pool de \_ \_ \_ \_ peças), D3D11 \_ RESOURCE \_ MISC \_ SHARED, \_ SHARED \_ KEYEDMUTEX ou SHARED \_ \_ NTHANDLE.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos com suporte**
</dt> <dd>

Somente D3D11 \_ USAGE \_ DEFAULT.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos lado a lado](creating-tiled-resources.md)
</dt> </dl>

 

 




