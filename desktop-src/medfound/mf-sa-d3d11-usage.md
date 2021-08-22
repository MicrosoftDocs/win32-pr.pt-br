---
description: Especifica como alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: MF_SA_D3D11_USAGE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7364b9777d94baa1a6c25aead6631ad6b11dcddc12db83698da04affebe0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663946"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>Atributo MF \_ SA \_ D3D11 \_ USAGE

Especifica como alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia. O uso reflete diretamente se um exemplo é acessível pela CPU ou GPU.

## <a name="data-type"></a>Tipo de dados

**D3D11 \_ USO** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um [**valor DE USO D3D11. \_**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation transformação

Nesse contexto, o atributo se aplica somente quando a transformação Microsoft Media Foundation (MFT) retorna **TRUE** para o atributo [MF \_ SA \_ D3D11 \_ AWARE.](mf-sa-d3d11-aware.md)

Se um MFT dá suporte ao Direct3D 11, esse atributo fornece uma dica para o MFT ao alocar superfícies do Microsoft Direct3D para saída. De definir o atributo da seguinte forma:

1.  Chame [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obter o armazenamento de atributos MFT.
2.  Chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

O Media Foundation pipeline define o atributo antes do início do streaming. O MFT deve tentar manter a configuração quando aloca superfícies. Se isso não for possível, o MFT poderá ignorar o atributo, em vez de falhar na alocação.

Além disso, se o MFT exigir superfícies Direct3D para entrada, ele poderá expor esse atributo como uma dica de como as superfícies de entrada devem ser alocadas. Consulte o atributo da seguinte forma:

1.  Chame [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obter os atributos de fluxo de entrada.
2.  Chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Alocador de exemplo

Esse atributo pode ser definido no alocador de exemplo de vídeo, no método [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx.**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
