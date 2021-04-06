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
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a><span data-ttu-id="478b4-103">Configurando codificação de áudio Standard, Professional ou Lossless</span><span class="sxs-lookup"><span data-stu-id="478b4-103">Configuring Standard, Professional, or Lossless Audio Encoding</span></span>

<span data-ttu-id="478b4-104">Quando o codificador de áudio do Windows Media enumera tipos de saída, ele identifica cada tipo enumerado como Standard, Professional ou Lossless.</span><span class="sxs-lookup"><span data-stu-id="478b4-104">When the Windows Media Audio encoder enumerates output types, it identifies each enumerated type as either Standard, Professional, or Lossless.</span></span> <span data-ttu-id="478b4-105">Você pode determinar se um tipo de saída é Standard, Professional ou Lossless executando as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="478b4-105">You can determine whether an output type is Standard, Professional, or Lossless by performing the following steps.</span></span>

1.  <span data-ttu-id="478b4-106">Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter uma interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que representa o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="478b4-106">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to obtain an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface that represents the output type.</span></span>
2.  <span data-ttu-id="478b4-107">Chame [**IMFMediaType:: Getrepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) para obter uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contém informações sobre o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="478b4-107">Call [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) to get an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains information about the output type.</span></span>
3.  <span data-ttu-id="478b4-108">O membro **pbFormat** da estrutura [**do \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) aponta para uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que contém informações adicionais sobre o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="478b4-108">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure points to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure that contains additional information about the output type.</span></span> <span data-ttu-id="478b4-109">Inspecione o membro **wFormatTag** da estrutura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="478b4-109">Inspect the **wFormatTag** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="478b4-110">Um valor de 0x161 indica Standard, um valor de 0x162 indica Professional e um valor de 0x163 indica sem perdas.</span><span class="sxs-lookup"><span data-stu-id="478b4-110">A value of 0x161 indicates Standard, a value of 0x162 indicates Professional, and a value of 0x163 indicates Lossless.</span></span>

<span data-ttu-id="478b4-111">Se você definir propriedades no codificador de áudio do Windows Media antes de enumerar os tipos de saída, poderá limitar o número de tipos de saída enumerados.</span><span class="sxs-lookup"><span data-stu-id="478b4-111">If you set properties on the Windows Media Audio encoder before you enumerate output types, you can limit the number of output types that are enumerated.</span></span> <span data-ttu-id="478b4-112">Por exemplo, se você definir as propriedades de VBR de forma adequada, poderá limitar os tipos de saída enumerados para aqueles que estão na categoria sem perdas.</span><span class="sxs-lookup"><span data-stu-id="478b4-112">For example, if you set the VBR properties appropriately, you can limit the enumerated output types to those that are in the Lossless category.</span></span>

## <a name="standard-audio-encoding"></a><span data-ttu-id="478b4-113">Codificação de áudio padrão</span><span class="sxs-lookup"><span data-stu-id="478b4-113">Standard Audio Encoding</span></span>

<span data-ttu-id="478b4-114">Você pode usar as etapas a seguir para configurar a codificação de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="478b4-114">You can use the following steps to configure Standard audio encoding.</span></span>

1.  <span data-ttu-id="478b4-115">Defina as propriedades de sua escolha no codificador.</span><span class="sxs-lookup"><span data-stu-id="478b4-115">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="478b4-116">Enumere os tipos de saída possíveis.</span><span class="sxs-lookup"><span data-stu-id="478b4-116">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="478b4-117">Inspecione os tipos enumerados e escolha um que tenha uma marca de formato de áudio de 0x161.</span><span class="sxs-lookup"><span data-stu-id="478b4-117">Inspect the enumerated types and choose one that has an audio format tag of 0x161.</span></span>
4.  <span data-ttu-id="478b4-118">Defina o tipo de saída para o tipo escolhido chamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="478b4-118">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="professional-audio-encoding"></a><span data-ttu-id="478b4-119">Codificação de áudio profissional</span><span class="sxs-lookup"><span data-stu-id="478b4-119">Professional Audio Encoding</span></span>

<span data-ttu-id="478b4-120">Você pode usar as etapas a seguir para configurar a codificação de áudio profissional.</span><span class="sxs-lookup"><span data-stu-id="478b4-120">You can use the following steps to configure Professional audio encoding.</span></span>

1.  <span data-ttu-id="478b4-121">Defina as propriedades de sua escolha no codificador.</span><span class="sxs-lookup"><span data-stu-id="478b4-121">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="478b4-122">Enumere os tipos de saída possíveis.</span><span class="sxs-lookup"><span data-stu-id="478b4-122">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="478b4-123">Inspecione os tipos enumerados e escolha um que tenha uma marca de formato de áudio de 0x162.</span><span class="sxs-lookup"><span data-stu-id="478b4-123">Inspect the enumerated types and choose one that has an audio format tag of 0x162.</span></span>
4.  <span data-ttu-id="478b4-124">Defina o tipo de saída para o tipo escolhido chamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="478b4-124">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="lossless-audio-encoding"></a><span data-ttu-id="478b4-125">Codificação de áudio sem perdas</span><span class="sxs-lookup"><span data-stu-id="478b4-125">Lossless Audio Encoding</span></span>

<span data-ttu-id="478b4-126">Você pode usar as etapas a seguir para configurar a codificação de áudio sem perdas.</span><span class="sxs-lookup"><span data-stu-id="478b4-126">You can use the following steps to configure Lossless audio encoding.</span></span>

1.  <span data-ttu-id="478b4-127">Defina a propriedade [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="478b4-127">Set the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to **VARIANT\_TRUE**.</span></span>
2.  <span data-ttu-id="478b4-128">Defina [**MFPKEY restringir a propriedade \_ \_ \_ VBRQUALITY enumerada**](mfpkey-constrain-enumerated-vbrqualityproperty.md) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="478b4-128">Set the [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) property to **VARIANT\_TRUE**.</span></span>
3.  <span data-ttu-id="478b4-129">Defina a propriedade [**MFPKEY \_ desejada \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) como 100.</span><span class="sxs-lookup"><span data-stu-id="478b4-129">Set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property to 100.</span></span>
4.  <span data-ttu-id="478b4-130">Enumerar tipos de saída.</span><span class="sxs-lookup"><span data-stu-id="478b4-130">Enumerate output types.</span></span>
5.  <span data-ttu-id="478b4-131">Defina o tipo de saída como um dos tipos enumerados na etapa 4 chamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="478b4-131">Set the output type to one of the types enumerated in step 4 by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="478b4-132">O código a seguir enumera todos os tipos de saída sem perdas para o codificador de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="478b4-132">The following code enumerates all of the lossless output types for the Windows Media Audio encoder.</span></span> <span data-ttu-id="478b4-133">O código imprime o valor da marca de formato de áudio para cada tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="478b4-133">The code prints the value of the audio format tag for each enumerated type.</span></span> <span data-ttu-id="478b4-134">Como todos os tipos enumerados são sem perdas, todas essas marcas de formatação têm um valor de 0x163.</span><span class="sxs-lookup"><span data-stu-id="478b4-134">Because all of the enumerated types are lossless, all of those format tags have a value of 0x163.</span></span> <span data-ttu-id="478b4-135">Suponha que pIMT seja um ponteiro para uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um objeto do codificador de áudio do Windows Media e que Pstore seja um ponteiro para uma interface **IPropertyStore** no mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="478b4-135">Assume that pIMT is a pointer to an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a Windows Media Audio encoder object and that pStore is a pointer to an **IPropertyStore** interface on the same object.</span></span> <span data-ttu-id="478b4-136">Suponha também que hr é uma variável do tipo **HRESULT** que foi declarada anteriormente no código.</span><span class="sxs-lookup"><span data-stu-id="478b4-136">Also assume that hr is a variable of type **HRESULT** that was declared previously in the code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="478b4-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="478b4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="478b4-138">Configurando codificação de áudio</span><span class="sxs-lookup"><span data-stu-id="478b4-138">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> </dl>

 

 
