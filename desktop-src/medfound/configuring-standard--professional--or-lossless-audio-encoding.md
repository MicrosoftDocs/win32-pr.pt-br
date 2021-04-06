---
description: Quando o codificador de áudio do Windows Media enumera tipos de saída, ele identifica cada tipo enumerado como Standard, Professional ou Lossless.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configurando codificação de áudio Standard, Professional ou Lossless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646608"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Configurando codificação de áudio Standard, Professional ou Lossless

Quando o codificador de áudio do Windows Media enumera tipos de saída, ele identifica cada tipo enumerado como Standard, Professional ou Lossless. Você pode determinar se um tipo de saída é Standard, Professional ou Lossless executando as etapas a seguir.

1.  Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter uma interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que representa o tipo de saída.
2.  Chame [**IMFMediaType:: Getrepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) para obter uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contém informações sobre o tipo de saída.
3.  O membro **pbFormat** da estrutura [**do \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) aponta para uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que contém informações adicionais sobre o tipo de saída. Inspecione o membro **wFormatTag** da estrutura **WAVEFORMATEX** . Um valor de 0x161 indica Standard, um valor de 0x162 indica Professional e um valor de 0x163 indica sem perdas.

Se você definir propriedades no codificador de áudio do Windows Media antes de enumerar os tipos de saída, poderá limitar o número de tipos de saída enumerados. Por exemplo, se você definir as propriedades de VBR de forma adequada, poderá limitar os tipos de saída enumerados para aqueles que estão na categoria sem perdas.

## <a name="standard-audio-encoding"></a>Codificação de áudio padrão

Você pode usar as etapas a seguir para configurar a codificação de áudio padrão.

1.  Defina as propriedades de sua escolha no codificador.
2.  Enumere os tipos de saída possíveis.
3.  Inspecione os tipos enumerados e escolha um que tenha uma marca de formato de áudio de 0x161.
4.  Defina o tipo de saída para o tipo escolhido chamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="professional-audio-encoding"></a>Codificação de áudio profissional

Você pode usar as etapas a seguir para configurar a codificação de áudio profissional.

1.  Defina as propriedades de sua escolha no codificador.
2.  Enumere os tipos de saída possíveis.
3.  Inspecione os tipos enumerados e escolha um que tenha uma marca de formato de áudio de 0x162.
4.  Defina o tipo de saída para o tipo escolhido chamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="lossless-audio-encoding"></a>Codificação de áudio sem perdas

Você pode usar as etapas a seguir para configurar a codificação de áudio sem perdas.

1.  Defina a propriedade [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como **Variant \_ true**.
2.  Defina [**MFPKEY restringir a propriedade \_ \_ \_ VBRQUALITY enumerada**](mfpkey-constrain-enumerated-vbrqualityproperty.md) como **Variant \_ true**.
3.  Defina a propriedade [**MFPKEY \_ desejada \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) como 100.
4.  Enumerar tipos de saída.
5.  Defina o tipo de saída como um dos tipos enumerados na etapa 4 chamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

O código a seguir enumera todos os tipos de saída sem perdas para o codificador de áudio do Windows Media. O código imprime o valor da marca de formato de áudio para cada tipo enumerado. Como todos os tipos enumerados são sem perdas, todas essas marcas de formatação têm um valor de 0x163. Suponha que pIMT seja um ponteiro para uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um objeto do codificador de áudio do Windows Media e que Pstore seja um ponteiro para uma interface **IPropertyStore** no mesmo objeto. Suponha também que hr é uma variável do tipo **HRESULT** que foi declarada anteriormente no código.


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando codificação de áudio](configuringaudioencoding.md)
</dt> </dl>

 

 
