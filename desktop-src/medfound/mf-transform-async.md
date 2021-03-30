---
description: Especifica se uma Media Foundation de transformação (MFT) executa o processamento assíncrono.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: Atributo MF_TRANSFORM_ASYNC (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647562"
---
# <a name="mf_transform_async-attribute"></a>\_Atributo assíncrono de transformação MF \_

Especifica se uma Media Foundation de transformação (MFT) executa o processamento assíncrono.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

O atributo é um valor booliano:

-   Se o atributo for diferente de zero, o MFT executará o processamento assíncrono.
-   Se o atributo for 0 ou não definido, o MFT será síncrono.

Para obter esse atributo, primeiro chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributos da MFT. Se esse método tiver sucesso, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o valor do atributo. Se um dos dois métodos falhar, o MFT será síncrono.

Para MFTs assíncronas, esse atributo deve ser definido como um valor diferente de zero. Para MFTs síncronos, esse atributo é opcional, mas deve ser definido como 0, se estiver presente.

MFTs assíncronas não são compatíveis com versões anteriores do Media Foundation. Para usar uma MFT assíncrona, o cliente deve definir o atributo de [**\_ \_ \_ desbloqueio do MF Transform Async**](mf-transform-async-unlock.md) no MFT. (O pipeline de Microsoft Media Foundation executa essa etapa automaticamente.)

## <a name="examples"></a>Exemplos

O código a seguir testa se uma MFT executa o processamento assíncrono.


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> <dt>

[**\_desbloqueio assíncrono de transformação MF \_ \_**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




