---
description: Especifica como alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: Atributo MF_SA_D3D11_USAGE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164762"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>\_Atributo de \_ uso de D3D11 do MF SA \_

Especifica como alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia. O uso reflete diretamente se um exemplo pode ser acessado pela CPU ou pela GPU.

## <a name="data-type"></a>Tipo de dados

**D3D11 \_ USO** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um valor [**de \_ uso de D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .

### <a name="microsoft-media-foundation-transforms"></a>Transformações de Microsoft Media Foundation

Nesse contexto, o atributo se aplica somente quando a Microsoft Media Foundation transformação (MFT) retorna **true** para o atributo [MF \_ SA \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) .

Se uma MFT der suporte ao Direct3D 11, esse atributo fornecerá uma dica para o MFT ao alocar superfícies do Microsoft Direct3D para saída. Defina o atributo da seguinte maneira:

1.  Chame [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obter o repositório de atributos de MFT.
2.  Chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

O pipeline de Media Foundation define o atributo antes de o streaming começar. O MFT deve tentar honrar a configuração ao alocar superfícies. Se isso não for possível, o MFT poderá ignorar o atributo, em vez de falhar a alocação.

Além disso, se o MFT exigir superfícies de Direct3D para entrada, ele poderá expor esse atributo como uma dica de como as superfícies de entrada devem ser alocadas. Consulte o atributo da seguinte maneira:

1.  Chame [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obter os atributos de fluxo de entrada.
2.  Chamar [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Exemplo de alocador

Esse atributo pode ser definido no exemplo de alocador de vídeo, no método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
