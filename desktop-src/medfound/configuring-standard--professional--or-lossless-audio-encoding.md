---
description: Quando o Windows de áudio de mídia enumera tipos de saída, ele identifica cada tipo enumerado como Standard, Professional ou Sem perda.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configurando a codificação de áudio padrão, Professional ou sem perda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa4184af8bc6b83710a3710ac1a278de71de0b7221dc11757bdeba46af8c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743533"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Configurando a codificação de áudio padrão, Professional ou sem perda

Quando o Windows de áudio de mídia enumera tipos de saída, ele identifica cada tipo enumerado como Standard, Professional ou Sem perda. Você pode determinar se um tipo de saída é Standard, Professional ou Sem perda executando as etapas a seguir.

1.  Chame [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter uma interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que representa o tipo de saída.
2.  Chame [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) para obter uma estrutura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contém informações sobre o tipo de saída.
3.  O **membro pbFormat** da estrutura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) aponta para uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que contém informações adicionais sobre o tipo de saída. **Inspecione o membro wFormatTag** da **estrutura WAVEFORMATEX.** Um valor de 0x161 indica Standard, um valor de 0x162 indica Professional e um valor de 0x163 indica Sem perda.

Se você definir propriedades no codificador Windows Media Audio antes de enumerar tipos de saída, poderá limitar o número de tipos de saída enumerados. Por exemplo, se você definir as propriedades VBR adequadamente, poderá limitar os tipos de saída enumerados àqueles que estão na categoria Sem perda.

## <a name="standard-audio-encoding"></a>Codificação de áudio padrão

Você pode usar as etapas a seguir para configurar a codificação de áudio Standard.

1.  De definir as propriedades de sua escolha no codificador.
2.  Enumerar os possíveis tipos de saída.
3.  Inspecione os tipos enumerados e escolha um que tenha uma marca de formato de áudio 0x161.
4.  De definir o tipo de saída para o tipo escolhido chamando [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="professional-audio-encoding"></a>Professional Codificação de áudio

Você pode usar as etapas a seguir para configurar Professional codificação de áudio.

1.  De definir as propriedades de sua escolha no codificador.
2.  Enumerar os possíveis tipos de saída.
3.  Inspecione os tipos enumerados e escolha um que tenha uma marca de formato de áudio 0x162.
4.  De definir o tipo de saída para o tipo escolhido chamando [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="lossless-audio-encoding"></a>Codificação de áudio sem perda

Você pode usar as etapas a seguir para configurar a codificação de áudio sem perda.

1.  De definir [**a propriedade \_ VBRENABLED MFPKEY**](mfpkey-vbrenabledproperty.md) como VARIANT **\_ TRUE.**
2.  De definir [**a propriedade \_ \_ \_ VBRQUALITY ENUMERADA ENUMERADA MFPKEY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) como **VARIANT \_ TRUE.**
3.  De definir [**a propriedade MFPKEY \_ DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) como 100.
4.  Enumerar tipos de saída.
5.  De definir o tipo de saída como um dos tipos enumerados na etapa 4 chamando [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

O código a seguir enumera todos os tipos de saída sem perda para o codificador Windows Media Audio. O código imprime o valor da marca de formato de áudio para cada tipo enumerado. Como todos os tipos enumerados são sem perda, todas essas marcas de formato têm um valor de 0x163. Suponha que pIMT seja um ponteiro para uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um objeto codificador de Áudio de Mídia Windows e que pStore seja um ponteiro para uma interface **IPropertyStore** no mesmo objeto. Suponha também que hr seja uma variável do tipo **HRESULT** declarada anteriormente no código.


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

[Configurando a codificação de áudio](configuringaudioencoding.md)
</dt> </dl>

 

 
