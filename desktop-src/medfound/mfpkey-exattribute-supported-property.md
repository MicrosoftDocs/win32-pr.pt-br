---
description: Especifica se uma Media Foundation transformação (MFT) copia atributos de exemplos de entrada para exemplos de saída.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Propriedade MFPKEY_EXATTRIBUTE_SUPPORTED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827910"
---
# <a name="mfpkey_exattribute_supported-property"></a>\_Propriedade com suporte do FILEATTRIBUTE MFPKEY \_

Especifica se uma Media Foundation transformação (MFT) copia atributos de exemplos de entrada para exemplos de saída.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**BOOL de variante \_**

BOOL do VT \_

**boolVal**



## <a name="remarks"></a>Comentários

Esse atributo pode ter os valores a seguir.



| Valor              | Descrição                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANTE \_ true**  | O MFT copia atributos dos exemplos de entrada para os exemplos de saída.                                                                                 |
| **VARIANTE \_ falso** | A sessão de mídia copia atributos de exemplos de entrada para exemplos de saída. Ele não substitui nenhum atributo que o MFT define na saída Samples. |



 

Para obter esse atributo, chame **QueryInterface** no MFT para a interface **IPropertyStore** .

O valor padrão é **Variant \_ false**. Se o MFT não expor a interface **IPropertyStore** ou se essa propriedade não estiver definida, trate o valor como **variante \_ false**.

Esta propriedade é somente para leitura.

> [!NOTE] 
> Este atributo não se aplica a MFTs assíncronas. Os atributos não serão copiados dos exemplos de entrada para os exemplos de saída para MFTs assíncronas, independentemente do valor desse atributo.

## <a name="examples"></a>Exemplos

O exemplo a seguir retornará VARIANT \_ true se um MFT copiar atributos de exemplo.


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




