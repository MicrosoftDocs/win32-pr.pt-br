---
description: Verificando os formatos DXVA-HD com suporte
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Verificando os formatos DXVA-HD com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b28586148bb96a918c8a230a25ff1477af73e0604d3b62e11e644e8276b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035404"
---
# <a name="checking-supported-dxva-hd-formats"></a>Verificando os formatos DXVA-HD com suporte

## <a name="checking-supported-input-formats"></a>Verificando os formatos de entrada com suporte

Para obter uma lista dos formatos de entrada compatíveis com o dispositivo DXVA-HD (Aceleração de Vídeo) do Microsoft DirectX, faça o seguinte:

1.  Chame [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obter as funcionalidades do dispositivo.
2.  Verifique o **membro InputFormatCount** da estrutura [**\_ VPDEVCAPS DXVAHD.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Esse membro fornece o número de formatos de entrada com suporte.
3.  Aloce uma matriz de **valores D3DFORMAT,** de tamanho **InputFormatCount.**
4.  Passe essa matriz para o [**método IDXVAHD \_ Device::GetVideoProcessorInputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) Os métodos preenchem a matriz com uma lista de formatos de entrada.

O código a seguir mostra essas etapas:


```C++
// Checks whether a DXVA-HD device supports a specified input format.

HRESULT CheckInputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[ caps.InputFormatCount ];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorInputFormats(
        caps.InputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.InputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.InputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="checking-supported-output-formats"></a>Verificando formatos de saída com suporte

Para obter uma lista dos formatos de saída compatíveis com o dispositivo DXVA-HD, faça o seguinte:

1.  Chame [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obter as funcionalidades do dispositivo.
2.  Verifique o **membro OutputFormatCount** da estrutura [**\_ VPDEVCAPS DXVAHD.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Esse membro fornece o número de formatos de entrada com suporte.
3.  Aloce uma matriz de **valores D3DFORMAT,** de tamanho **OutputFormatCount.**
4.  Passe essa matriz para o [**método IDXVAHD \_ Device::GetVideoProcessorOutputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) Os métodos preenchem a matriz com uma lista de formatos de saída.

O código a seguir mostra essas etapas:


```C++
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



