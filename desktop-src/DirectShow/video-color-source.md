---
description: Fonte de cores do vídeo
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Fonte de cores do vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331640a9240ef0ea16ff565180503066f22ce5ae2550fa1e1ec524dcf05c8fa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071930"
---
# <a name="video-color-source"></a>Fonte de cores do vídeo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A fonte de cores do vídeo cria uma imagem de vídeo contínua de uma cor sólida.

ID de classe (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**

Nome da variável CLSID: **CLSID \_ Colorize**

Propriedades



| Propriedade | Type      | Padrão | Descrição                                   |
|----------|-----------|---------|-----------------------------------------------|
| Colorida  | **DWORD** | 0       | Especifica a cor a ser gerada. Consulte Observações. |



 

## <a name="remarks"></a>Comentários

A fonte de cores do vídeo é usada com objetos de origem. Primeiro, crie um novo objeto de origem. Em seguida, defina o GUID do subobjeto do objeto de origem como CLSID \_ colorname chamando o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Para definir a cor, crie um objeto [setter de propriedade](property-setter.md) e aplique a propriedade "Color" no tempo zero. O valor dessa propriedade é um número hexadecimal com o formato *0xAARRGGBB*, em que *AA* é o valor alfa, *RR* é o valor vermelho, *gg* é o valor verde e *BB* é o valor azul. Valores Alfa variam de 0x00 (transparente) a 0xFF (opaco). A propriedade é estática e deve ser aplicada no tempo zero.

Se você não especificar o valor alfa, o padrão será zero (transparente). Em um projeto de vídeo de cor de 32 bits, isso causará transições ou efeitos que usam alfa para renderizar a fonte de cores do vídeo como completamente transparente. Para ser seguro, sempre especifique o alfa. Por exemplo, o preto opaco é **0xFF000000**.

O exemplo de código a seguir mostra como usar esse objeto. Para obter mais informações sobre como usar o [**IPropertySetter**](ipropertysetter.md), consulte [definindo propriedades em efeitos e transições](setting-properties-on-effects-and-transitions.md):


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



O exemplo a seguir mostra a representação XML do objeto criado no exemplo anterior. Nesse caso, o elemento [**param**](param-element.md) não oferece suporte a elementos [**at**](at-element.md) ou [**lineares**](linear-element.md) , porque o objeto não oferece suporte a propriedades dinâmicas:


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



