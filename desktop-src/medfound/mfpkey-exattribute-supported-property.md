---
description: Especifica se uma transformação Media Foundation (MFT) copia atributos de exemplos de entrada para exemplos de saída.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED propriedade (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248609828df3ef977112058ffe0d169104e68c181fa455ef27f2adcea0220aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663504"
---
# <a name="mfpkey_exattribute_supported-property"></a>Propriedade MFPKEY \_ EXATTRIBUTE \_ SUPPORTED

Especifica se uma transformação Media Foundation (MFT) copia atributos de exemplos de entrada para exemplos de saída.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**VARIANT \_ BOOL**

BOOL da VT \_

**boolVal**



## <a name="remarks"></a>Comentários

Esse atributo pode ter os valores a seguir.



| Valor              | Descrição                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | O MFT copia atributos dos exemplos de entrada para os exemplos de saída.                                                                                 |
| **VARIANT \_ FALSE** | A Sessão de Mídia copia atributos de exemplos de entrada para exemplos de saída. Ele não substitui nenhum atributos que o MFT define nos exemplos de saída. |



 

Para obter esse atributo, chame **QueryInterface** no MFT para a interface **IPropertyStore.**

O valor padrão é **VARIANT \_ FALSE.** Se o MFT não expor a interface **IPropertyStore** ou se essa propriedade não estiver definida, trate o valor **como VARIANT \_ FALSE.**

Esta propriedade é somente para leitura.

> [!NOTE] 
> Esse atributo não se aplica a MFTs assíncronos. Os atributos não serão copiados dos exemplos de entrada para os exemplos de saída para MFTs assíncronos, independentemente do valor desse atributo.

## <a name="examples"></a>Exemplos

O exemplo a seguir retornará VARIANT \_ TRUE se um MFT copia atributos de exemplo.


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




