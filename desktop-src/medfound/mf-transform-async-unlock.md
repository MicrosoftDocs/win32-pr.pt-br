---
description: Habilita o uso de uma Media Foundation de transformação assíncrona (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: Atributo MF_TRANSFORM_ASYNC_UNLOCK (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82a0a8f328095c3a5c567171fa6a625a77e5623d126dfb2be9f34fef556984be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244172"
---
# <a name="mf_transform_async_unlock-attribute"></a>\_Atributo de \_ desbloqueio assíncrono de transformação MF \_

Habilita o uso de uma Media Foundation de transformação assíncrona (MFT).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

MFTs assíncronas não são compatíveis com versões anteriores do Microsoft Media Foundation. Para evitar que aplicativos existentes acidentalmente usem uma MFT assíncrona, esse atributo deve ser definido como um valor diferente de zero antes que uma MFT assíncrona possa ser usada. O pipeline de Media Foundation define automaticamente o atributo, para que a maioria dos aplicativos não precise usar esse atributo. No entanto, se um aplicativo usar uma MFT assíncrona fora do pipeline de Media Foundation, o aplicativo deverá definir esse atributo.

Os MFTs síncronos não exigem esse atributo.

Para testar se uma MFT é assíncrona, obtenha o valor do [atributo \_ \_ assíncrono de transformação MF](mf-transform-async.md) na MFT.

## <a name="examples"></a>Exemplos

O código a seguir desbloqueia uma MFT assíncrona.


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




