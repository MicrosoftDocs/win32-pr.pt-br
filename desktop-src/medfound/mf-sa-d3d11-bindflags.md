---
description: Especifica os sinalizadores de associação a serem usados ao alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: Atributo MF_SA_D3D11_BINDFLAGS (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296816"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>\_Atributo MF SA \_ D3D11 \_ BINDFLAGS

Especifica os sinalizadores de associação a serem usados ao alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um **ou** bit a bit de sinalizadores de [**\_ \_ sinalizador de ligação D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .

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

 

 
