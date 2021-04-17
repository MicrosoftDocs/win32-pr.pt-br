---
description: Especifica se uma Media Foundation transformação (MFT) dá suporte a DXVA (aceleração de vídeo do DirectX). Esse atributo se aplica somente a MFTs de vídeo.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: Atributo MF_SA_D3D_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762441"
---
# <a name="mf_sa_d3d_aware-attribute"></a>\_Atributo de \_ reconhecimento de D3D SA do MF \_

Especifica se uma Media Foundation transformação (MFT) dá suporte a DXVA (aceleração de vídeo do DirectX). Esse atributo se aplica somente a MFTs de vídeo.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Para consultar esse atributo, chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributo global do MFT. Se **GetAttributes** tiver sucesso, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Esse atributo informa ao cliente se o MFT pode usar o vídeo do Direct3D 9:

-   Se o atributo for diferente de zero, o cliente poderá dar ao MFT um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) antes de o streaming começar. Para fazer isso, o cliente envia a mensagem do Gerenciador de D3D do conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md) O cliente não é necessário para enviar esta mensagem.
-   Se esse atributo for zero (**false**), o MFT não oferecerá suporte ao vídeo do Direct3D 9 e o cliente não deverá enviar a mensagem do Gerenciador de D3D do conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md)

O valor padrão desse atributo é **false**. Trate este atributo como somente leitura. Não altere o valor; o MFT ignorará as alterações no valor.

Para obter mais informações sobre como implementar esse atributo em uma MFT personalizada, consulte [MFTs com reconhecimento de Direct3D](direct3d-aware-mfts.md).

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="examples"></a>Exemplos

O código a seguir testa se uma MFT dá suporte a DXVA.


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs com reconhecimento de Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Suporte a DXVA 2,0 no Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[\_modo de \_ DXVA da topologia MF \_](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




