---
description: Especifica se o SA (Alocador de Exemplo) do MFT deve alocar a Textura Direct3D subjacente usando o sinalizador D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE dados.
title: MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES (Mftransform.h)
ms.topic: reference
ms.date: 03/31/2018
ms.openlocfilehash: fedcfbe98344dd9b424c1a8ce90e847e98f1af51
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548701"
---
# <a name="mf_sa_d3d_allocate_displayable_resources-attribute"></a>Atributo MF \_ SA \_ D3D \_ ALLOCATE \_ \_ DISPLAYABLE RESOURCES

Especifica se o SA (Alocador de Exemplo) do MFT deve alocar a Textura Direct3D subjacente usando o sinalizador [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) dados. 

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo está disponível com Windows 10 build 20348. 

> [!NOTE]
> O **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** de membro da [enumeração D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) estará disponível em uma versão futura do SDK.

A camada Media Foundation plataforma define o **atributo MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** ao renderizar o vídeo. Um aplicativo também pode optar por definir esse atributo se quiser implementar seu próprio renderador de vídeo e usar recursos exibiáveis D3D11. 

## <a name="example"></a>Exemplo

O exemplo de código a seguir demonstra o uso do **atributo MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES.**

```cpp
class DecoderMFT : public IMFAttributes, public IMFTransform 
{ 
    //  
    ... Other implementation details ommitted 
    // 

public: 
    // Implementation of IMFAttributes::GetAttributes which is invoked by the MF Topology Loader 
    STDMETHODIMP GetAttribtues(IMFAttributes** attributes) 
    { 
        m_attributes.copyTo(attributes); 
        return S_OK; 
    } 

 

private: 
    // Private method to be called before DecoderMFT initializes its sample pool. 
    // A good place for this to happen is in the method which processes the  
    // 'MFT_MESSAGE_NOTIFY_BEGIN_STREAMING' event. 
    // At a minimum, this processing would be in DecoderMFT's implementation of IMFTransform::ProcessMessage.  

    HRESULT ConfigureTextureFlags() 
    { 
        UINT32 allocateDisplayables = MFGetAttributeUINT32(m_attributes.get(), 
            MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES, 0); 

        // If no MF_SA_* attributes which correspond to D3D misc flags are set then it is valid for 
        // miscFlags to be set to 0. 
        m_textureDesc.miscFlags = 0; 
        UINT32 sharedResources = 0; 

        if (allocateDisplayables != 0) 
        { 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_DISPLAYABLE; 
            // The following flag is required for the decoders output to 
            // use D3D11_RESOURCE_MISC_DISPLAYABLE. 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_EXCLUSIVE_WRITER; 

            // The following flags are required for the presentation API 
            // to consume and present these resources (also known as direct presentation). 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED_NTHANDLE; 

            sharedResources = 1; 
        } 
        else  
        { 
            // This handles the case when MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES was 0 or missing. 
            sharedResources = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED_WITHOUT_MUTEX, 0); 

            if (sharedResources != 0) 
            { 
                m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            } 
            else 
            { 
                UINT32 sharedKeyMutex = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED, 0); 

                if (sharedKeyMutex != 0) 
                { 
                    m_textureDesc.micsFlags |= D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX; 
                } 
            } 
        } 

        // Processing for other MF_SA_* attributes which imply D3D11_RESOURCE_MISC flag 
        // omitted from this sample. 

        return S_OK; 

    } 

    // Private method showing how DecoderMFT can create a texture with the flags required 
    // to satisfy "MF_SA_D3D11_ALLOCATE_DISPLAYBLE_RESOURCES".  
    // Because this is a private function we know the passed in pointer is always valid. 
    // This would be invoked by another private DecoderMFT function when allocating an MFSample 
    // for its sample pool. 

    HRESULT AllocateTextureForSample(ID3D11Texture2D** texture2D) 
    { 
        return m_d3dDevice->CreateTexture2D(&m_textureDesc, nullptr, texture2D); 
    } 

    // ... other members omitted 
    wil::com_ptr_nothrow<IMFAttributes> m_attributes; 
    wil::com_ptr_nothrow<ID3D11Device> m_d3dDevice; 

    // This a texture description for D3D11 resources. 
    D3D11_TEXTURE_2D_DESC m_textureDesc = {}; 

}; 
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 build 20348<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 




