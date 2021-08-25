---
description: Especifica se uma transformação Media Foundation (MFT) executa o processamento assíncrono.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a647ca122c138f2ef7e90670798200fc3fa629be48d6242b4e71dbc93151e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714343"
---
# <a name="mf_transform_async-attribute"></a>Atributo \_ ASYNC MF TRANSFORM \_

Especifica se uma transformação Media Foundation (MFT) executa o processamento assíncrono.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

O atributo é um valor booliana:

-   Se o atributo for não zero, o MFT executará o processamento assíncrono.
-   Se o atributo for 0 ou não for definido, o MFT será síncrono.

Para obter esse atributo, primeiro chame [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o armazenamento de atributos do MFT. Se esse método for bem-sucedido, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o valor do atributo. Se um dos dois métodos falhar, o MFT será síncrono.

Para MFTs assíncronos, esse atributo deve ser definido como um valor não zero. Para MFTs síncronos, esse atributo é opcional, mas deve ser definido como 0 se estiver presente.

Os MFTs assíncronos não são compatíveis com versões anteriores do Media Foundation. Para usar um MFT assíncrono, o cliente deve definir o atributo [**MF \_ TRANSFORM \_ ASYNC \_ UNLOCK**](mf-transform-async-unlock.md) no MFT. (O Microsoft Media Foundation pipeline executa essa etapa automaticamente.)

## <a name="examples"></a>Exemplos

O código a seguir testa se um MFT executa o processamento assíncrono.


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
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos UWP da área \| de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs assíncronos](asynchronous-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> <dt>

[**DESBLOQUEIO \_ \_ ASSÍNCRONO DE TRANSFORMAÇÃO MF \_**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




