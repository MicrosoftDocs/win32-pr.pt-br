---
description: Definindo preferências de desentrelaçamento
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Definindo preferências de desentrelaçamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645626"
---
# <a name="setting-deinterlace-preferences"></a>Definindo preferências de desentrelaçamento

O VMR (Video mixagem Renderer) dá suporte ao desentrelaçamento acelerado por hardware, o que melhora a qualidade de renderização para vídeo entrelaçado. Os recursos exatos que estão disponíveis dependem do hardware subjacente. O aplicativo pode consultar os recursos de desentrelaçamento de hardware e definir as preferências de desentrelaçamento por meio da interface [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) ou da interface [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9). O desentrelaçamento é realizado em uma base por fluxo.

Há uma diferença importante no comportamento de entrelaçamento entre o VMR-7 e o VMR-9. Em sistemas em que o hardware de gráficos não dá suporte ao Desentrelaçamento avançado, o VMR-7 pode retornar à sobreposição de hardware e instruí-lo a usar um desentrelaçamento de estilo BOB. Nesse caso, embora o VMR esteja relatando 30fps, o vídeo está realmente sendo renderizado em 60 invertidos por segundo.

Exceto no caso do VMR-7 usando a sobreposição de hardware, o desentrelaçamento é executado pelo mixer do VMR. O mixer usa a DDI (interface de driver de dispositivo) de desentrelaçamento do DirectX Video Acceleration (DXVA) para executar o desentrelaçamento. Essa DDI não pode ser chamada por aplicativos e os aplicativos não podem substituir a funcionalidade de desentrelaçamento do VMR. No entanto, um aplicativo pode selecionar o modo de desentrelaçamento desejado, conforme descrito nesta seção.

> [!Note]  
> Esta seção descreve os métodos **IVMRDeinterlaceControl9** , mas as versões do VMR-7 são quase idênticas.

 

Para obter os recursos de desentrelaçamento de um fluxo de vídeo, faça o seguinte:

1.  Preencha uma estrutura [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) com uma descrição do fluxo de vídeo. Detalhes de como preencher essa estrutura são fornecidos posteriormente.
2.  Passe a estrutura para o método [**IVMRDeinterlaceControl9:: GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) . Chame o método duas vezes. A primeira chamada retorna o número de modos de desentrelaçamento que o hardware suporta para o formato especificado. Aloque uma matriz de GUIDs desse tamanho e chame o método novamente, passando o endereço da matriz. A segunda chamada preenche a matriz com GUIDs. Cada GUID identifica um modo de desentrelaçamento.
3.  Para obter o recursos de um modo específico, chame o método [**IVMRDeinterlaceControl9:: GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) . Passe a mesma estrutura **VMR9VideoDesc** , junto com um dos GUIDs da matriz. O método preenche uma estrutura [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) com os recursos do modo.

O código a seguir mostra estas etapas:


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



Agora o aplicativo pode definir o modo de desentrelaçamento para o fluxo, usando os seguintes métodos:

-   O método [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) define o modo preferencial. Use o GUID \_ NULL para desligar o desentrelaçamento.
-   O método [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) especifica o comportamento se o modo solicitado não estiver disponível.
-   O método [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) retorna o modo preferencial que você definiu.
-   O método [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) retorna o modo real em uso, que pode ser um modo de fallback, se o modo preferencial não estiver disponível.

As páginas de referência do método fornecem mais informações.

**Usando a estrutura VMR9VideoDesc**

No procedimento fornecido anteriormente, a primeira etapa é preencher uma estrutura **VMR9VideoDesc** com uma descrição do fluxo de vídeo. Comece obtendo o tipo de mídia do fluxo de vídeo. Você pode fazer isso chamando [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) no pino de entrada do filtro do VMR. Em seguida, confirme se o fluxo de vídeo está entrelaçado. Somente os formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) podem ser entrelaçados. Se o tipo de formato for FORMAT \_ VIDEOINFO, ele deverá ser um quadro progressivo. Se o tipo de formato for FORMAT \_ VideoInfo2, verifique o campo **dwInterlaceFlags** do \_ sinalizador isentrelaçated AMINTERLACE. A presença desse sinalizador indica que o vídeo está entrelaçado.

Suponha que a variável **pBMI** seja um ponteiro para a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no bloco de formato. Defina os seguintes valores na estrutura **VMR9VideoDesc** :

-   **dwSize**: defina esse campo como `sizeof(VMR9VideoDesc)` .
-   **dwSampleWidth**: defina esse campo como `pBMI->biWidth` .
-   **dwSampleHeight**: defina esse campo como `abs(pBMI->biHeight)` .
-   **SampleFormat**: Este campo descreve as características de entrelaçamento do tipo de mídia. Verifique o campo **dwInterlaceFlags** na estrutura **VIDEOINFOHEADER2** e defina **SampleFormat** igual ao sinalizador equivalente [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) . Uma função auxiliar para fazer isso é fornecida abaixo.
-   **InputSampleFreq**: esse campo fornece a frequência de entrada, que pode ser calculada a partir do campo **AvgTimePerFrame** na estrutura **VIDEOINFOHEADER2** . No caso geral, defina **dwNumerator** como 10 milhões e defina **dwDenominator** como **AvgTimePerFrame**. No entanto, você também pode verificar se há algumas taxas de quadros bem conhecidas:

    | Tempo médio por quadro | Taxa de quadros (FPS) | Numera | Denominador |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59,94 (NTSC)     | 60000     | 1001        |
    | 333667                 | 29,97 (NTSC)     | 30000     | 1001        |
    | 417188                 | 23,97 (NTSC)     | 24.000     | 1001        |
    | 200000                 | 50, 0 (PAL)      | 50        | 1           |
    | 400000                 | 25, 0 (PAL)      | 25        | 1           |
    | 416667                 | 24, 0 (filme)     | 24        | 1           |

    

     

-   **OutputFrameFreq**: esse campo fornece a frequência de saída, que pode ser calculada com base no valor de **InputSampleFreq** e nas características de intercalação do fluxo de entrada:
    -   Defina **OutputFrameFreq. dwDenominator** igual a **InputSampleFreq. dwDenominator**.
    -   Se o vídeo de entrada for intercalado, defina **OutputFrameFreq. dwNumerator** como 2 x **InputSampleFreq. dwNumerator**. (Após desentrelaçar, a taxa de quadros é duplicada.) Caso contrário, defina o valor como **InputSampleFreq. dwNumerator**.
-   **dwFourCC**: defina esse campo como `pBMI->biCompression` .

A função auxiliar a seguir converte os sinalizadores AMINTERLACE \_ *X* em valores [**\_ SampleFormat VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) :


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



 

 



