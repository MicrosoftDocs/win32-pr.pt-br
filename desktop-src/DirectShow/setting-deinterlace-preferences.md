---
description: Definindo preferências de desinteressar
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Definindo preferências de desinteressar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33dae356618653f501b56f8b7a7eeb98e24ee92eb196cac78466e8cd26c01610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072570"
---
# <a name="setting-deinterlace-preferences"></a>Definindo preferências de desinteressar

O VMR (Video Mixing Renderer) dá suporte à desintercalação acelerada por hardware, o que melhora a qualidade de renderização para vídeo entrelaçado. Os recursos exatos disponíveis dependem do hardware subjacente. O aplicativo pode consultar os recursos de desintercalação de hardware e definir preferências de desintercalação por meio da interface [**IVMRDeinter preferencial**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) ou da interface [**IVMRDeintercontrol9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9). A desintercalação é executada por fluxo.

Há uma diferença importante no comportamento de entrelaçamento entre a VMR-7 e a VMR-9. Em sistemas em que o hardware gráfico não dá suporte à desintercalação avançada, a VMR-7 pode fazer fall back para a sobreposição de hardware e instruí-la a usar um desinteressamento de estilo BOB. Nesse caso, embora a VMR está relatando 30fps, o vídeo está sendo renderizado a 60 in flips por segundo.

Exceto no caso da VMR-7 usando sobreposição de hardware, a desintercalação é executada pelo mixer da VMR. O mixer usa a DXVA (Aceleração de Vídeo) DXVA (interface de driver de dispositivo) do DirectX para executar a desintervalação. Essa DDI não pode ser chamada por aplicativos e os aplicativos não podem substituir a funcionalidade de desintercalação da VMR. No entanto, um aplicativo pode selecionar o modo de desintercalação desejado, conforme descrito nesta seção.

> [!Note]  
> Esta seção descreve os **métodos IVMRDeintercontrol9,** mas as versões VMR-7 são quase idênticas.

 

Para obter os recursos de desintercalação de um fluxo de vídeo, faça o seguinte:

1.  Preencha uma [**estrutura VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) com uma descrição do fluxo de vídeo. Detalhes de como preencher essa estrutura são determinados posteriormente.
2.  Passe a estrutura para [**o método IVMRDeintermodControl9::GetNumberOfDeintermodModes.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) Chame o método duas vezes. A primeira chamada retorna o número de modos de desinteressação compatíveis com o hardware para o formato especificado. Aloce uma matriz de GUIDs desse tamanho e chame o método novamente, passando o endereço da matriz. A segunda chamada preenche a matriz com GUIDs. Cada GUID identifica um modo de desintercalação.
3.  Para obter as capabilities de um modo específico, chame o [**método IVMRDeinterceptControl9::GetDeintermodModeCaps.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) Passe a mesma **estrutura VMR9VideoDesc,** juntamente com um dos GUIDs da matriz. O método preenche uma estrutura [**VMR9Deinterceptcaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) com as funcionalidades de modo.

O código a seguir mostra essas etapas:


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



Agora, o aplicativo pode definir o modo de desintercalação para o fluxo, usando os seguintes métodos:

-   O [**método SetDeintermodMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) define o modo preferencial. Use GUID \_ NULL para desativar a desintercalação.
-   O [**método SetDeinterceptprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) especifica o comportamento se o modo solicitado não estiver disponível.
-   O [**método GetDeintermodMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) retorna o modo preferencial que você definiu.
-   O [**método GetActualDeintermode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) retorna o modo real em uso, que pode ser um modo de fallback, se o modo preferencial não estiver disponível.

As páginas de referência de método dão mais informações.

**Usando a estrutura VMR9VideoDesc**

No procedimento dado anteriormente, a primeira etapa é preencher uma estrutura **VMR9VideoDesc** com uma descrição do fluxo de vídeo. Comece recebendo o tipo de mídia do fluxo de vídeo. Você pode fazer isso chamando [**IPin::ConnectionMediaType no**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) pino de entrada do filtro VMR. Em seguida, confirme se o fluxo de vídeo está entrelaçado. Somente [**os formatos VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) podem ser entrelaçados. Se o tipo de formato for FORMAT \_ VideoInfo, ele deverá ser um quadro progressivo. Se o tipo de formato for FORMAT VideoInfo2, verifique o campo \_ **dwInterinfoFlags** para o sinalizador \_ ISInterlaced AMINTER DIGIT. A presença desse sinalizador indica que o vídeo está entrelaçado.

Suponha que a **variável pBMI** seja um ponteiro para a [**estrutura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no bloco de formato. De definir os seguintes valores na **estrutura VMR9VideoDesc:**

-   **dwSize:** de definido este campo como `sizeof(VMR9VideoDesc)` .
-   **dwSampleWidth:** de definir este campo como `pBMI->biWidth` .
-   **dwSampleHeight:** de definir este campo como `abs(pBMI->biHeight)` .
-   **SampleFormat:** este campo descreve as características de intercalação do tipo de mídia. Verifique o **campo dwInterheadFlags** na estrutura **VIDEOINFOHEADER2** e defina **SampleFormat** igual ao sinalizador [**\_ SampleFormat VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) equivalente. Uma função auxiliar para fazer isso é dada abaixo.
-   **InputSampleFreq:** esse campo fornece a frequência de entrada, que pode ser calculada do **campo AvgTimePerFrame** na estrutura **VIDEOINFOHEADER2.** No caso geral, de definido **dwNumerator** como 10000000 e de definir **dwDenominator** como **AvgTimePerFrame**. No entanto, você também pode verificar algumas taxas de quadros conhecidas:

    | Tempo médio por quadro | Taxa de quadros (fps) | Numerador | Denominador |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59.94 (NTSC)     | 60000     | 1001        |
    | 333667                 | 29.97 (NTSC)     | 30000     | 1001        |
    | 417188                 | 23.97 (NTSC)     | 24.000     | 1001        |
    | 200000                 | 50,00 (PAL)      | 50        | 1           |
    | 400000                 | 25.00 (PAL)      | 25        | 1           |
    | 416667                 | 24h (Filme)     | 24        | 1           |

    

     

-   **OutputFrameFreq:** esse campo fornece a frequência de saída, que pode ser calculada com base no valor **InputSampleFreq** e nas características de intercalação do fluxo de entrada:
    -   **Demarque OutputFrameFreq.dwDenominator** igual a **InputSampleFreq.dwDenominator**.
    -   Se o vídeo de entrada for intercalado, desmarque **OutputFrameFreq.dwNumerator** como 2 x **InputSampleFreq.dwNumerator**. (Após a desintercalação, a taxa de quadros é dobrada.) Caso contrário, demarque o **valor como InputSampleFreq.dwNumerator**.
-   **dw Ltda:** de definir este campo como `pBMI->biCompression` .

A função auxiliar a seguir converte sinalizadores AMINTER \_ *LTDA X* em [**valores de \_ SampleFormat VMR9:**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat)


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



