---
description: O método GetBitmapBits recupera um quadro de vídeo no momento da mídia especificado. O quadro retornado está sempre no formato RGB de 24 bits.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: Método IMediaDet::GetBitmapBits (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c4a7332580d4e9a9fece5a66d390753566fbf54c615699663256c463cb401b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791996"
---
# <a name="imediadetgetbitmapbits-method"></a>Método IMediaDet::GetBitmapBits

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetBitmapBits` método recupera um quadro de vídeo no momento da mídia especificado. O quadro retornado está sempre no formato RGB de 24 bits.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StreamTime* 
</dt> <dd>

Tempo no qual recuperar o quadro de vídeo, em segundos.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Recebe o tamanho do buffer necessário. Se *pBuffer* for **NULL,** a variável receberá o tamanho do buffer necessário para recuperar o quadro. Se *pBuffer* não for **NULL,** esse parâmetro será ignorado.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Ponteiro para um buffer que recebe uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguida pelos bits DIB.

</dd> <dt>

*Largura* 
</dt> <dd>

Largura da imagem de vídeo, em pixels.

</dd> <dt>

*Altura* 
</dt> <dd>

Altura da imagem de vídeo, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                             | Descrição                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | Não foi possível adicionar o [**filtro Grabber de**](sample-grabber-filter.md) Exemplo ao grafo.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memória insuficiente.<br/>                                                                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>               | Erro de ponteiro **NULL.**<br/>                                                                |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>            | Erro inesperado.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de mídia inválido.<br/>                                                                    |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, de definir o nome do arquivo e o fluxo chamando [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream.**](imediadet-put-currentstream.md)

Para determinar o tamanho do buffer necessário, chame esse método com *pBuffer* igual a **NULL.** O tamanho é retornado na variável apontada por *pBufferSize*. Em seguida, crie o buffer e chame o método novamente, com *pBuffer* igual ao endereço do buffer. Quando o método retorna, o buffer contém uma **estrutura BITMAPINFOHEADER** seguida pelo bitmap. O bitmap é dimensionado para as dimensões especificadas nos parâmetros *Width* e *Height.*

Esse método coloca o detector de mídia no modo de captura de bitmap. Depois que esse método for chamado, os vários métodos de informações de fluxo no **IMediaDet** não funcionarão, a menos que você crie uma nova instância do detector de mídia.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="examples"></a>Exemplos

O código a seguir usa `GetBitmapBits` o método para criar um bitmap independente do dispositivo.


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaDet Interface**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




