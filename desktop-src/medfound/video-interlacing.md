---
description: Entrelaçamento de vídeo
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Entrelaçamento de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340c727f8faaaf20ff82eff58d0c651601071dea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474332"
---
# <a name="video-interlacing"></a>Entrelaçamento de vídeo

Este tópico descreve como fontes de mídia e decodificadores devem lidar com conteúdo de vídeo entrelaçados.

Para decodificar e renderizar o vídeo entrelaçado corretamente, as seguintes informações são necessárias:

-   Progressivo ou entrelaçado. Um fluxo de vídeo pode conter quadros progressivos, quadros entrelaçados ou uma combinação de ambos.

-   Predominância de campo. A predominância de campo descreve qual campo aparece primeiro, o campo superior ou o campo inferior.

-   Repita o primeiro campo. Esse sinalizador é usado na pulldown 3:2, quando o quadro é progressivo, mas o fluxo é entrelaçado. Nesse contexto, o primeiro campo pode ser o campo superior ou inferior.

-   Campos intercalados ou campo único. Um exemplo pode conter um único campo ou dois campos intercalados. Se um exemplo contiver um único campo, a altura da amostra será metade da altura do quadro, pois o exemplo contém apenas metade das linhas de verificação de um quadro. Campos intercalados são recomendados, a menos que as características do conteúdo de origem ditam o contrário.

Qualquer uma dessas características pode mudar de um exemplo para o próximo. No entanto, os componentes de vídeo precisam saber algo sobre o conteúdo geral antes do início do streaming. Por exemplo, se o vídeo for entrelaçado, o renderização de vídeo aprimorado (EVR) precisará reservar memória de vídeo para a desintercalação. Se o vídeo for quadros totalmente progressivos, por outro lado, o EVR poderá otimizar o pipeline de renderização. Adicionar uma etapa de desintercalação ao pipeline aumenta a latência de renderização.

Informações sobre o entrelaçamento são armazenadas em dois locais:

-   Informações gerais sobre o entrelaçamento em um fluxo são colocadas no tipo de mídia. Para obter mais informações sobre tipos de mídia, consulte [Tipos de mídia](media-types.md).

-   As informações que podem mudar com cada amostra são colocadas no exemplo como um atributo. Para obter mais informações sobre exemplos, consulte [Amostras de mídia](media-samples.md).

## <a name="interlace-information-in-the-media-type"></a>Informações intercalar no tipo de mídia

O [**atributo \_ MF MT INTER DIGIT \_ \_ MODE no**](mf-mt-interlace-mode-attribute.md) tipo de mídia descreve como o fluxo como um todo é entrelaçado. O valor desse atributo é um membro da [**enumeração MFVideoIntermodMode.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) Um tipo de mídia de vídeo sempre deve ter esse atributo.

-   Se o fluxo contiver apenas quadros progressivos, sem quadros entrelaçados, use MFVideoInter frame \_ Progressivo.
-   Se o fluxo contiver apenas quadros entrelaçados e cada amostra contiver dois campos intercalados, use MFVideoInterpper \_ FieldInterleavedUpperFirst ou MFVideoInterpper \_ FieldInterleavedLowerFirst.
-   Se o fluxo contiver apenas quadros entrelaçados e cada amostra contiver um único campo, use MFVideoInterpper \_ FieldSingleUpper ou MFVideoInterpper \_ FieldSingleLower. Se os campos alternam entre superior e inferior, não importa qual desses dois valores será usado. Se o formato contiver apenas campos superiores ou apenas campos inferiores, de definir o valor que corresponde ao conteúdo.
-   Se o fluxo contiver uma combinação de quadros entrelaçados e progressivos ou se a predominância de campo mudar, de definir o tipo de mídia como MFVideoInter digitado \_ MixedInter digitorProgressive. Use atributos de exemplo para descrever cada quadro.

A tabela a seguir resume esse atributo.



| MODO \_ \_ INTERESCALA MF \_ MT                       | Entrelaçado? | Amostras                                  | Primeiro campo    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MFVideoInterquot \_ Progressivo                 | Não          | Quadro progressivo                        | Não aplicável |
| MFVideoInterpper \_ FieldInterleavedUpperFirst  | Sim         | Campos intercalados                       | Superior primeiro    |
| MFVideoInterlow \_ FieldInterleavedLowerFirst  | Sim         | Campos intercalados                       | Inferior primeiro    |
| MFVideoInterpper \_ FieldSingleUpper            | Sim         | Campo único                             | Superior primeiro    |
| FieldSingleLower MFVideoInterlower \_            | Sim         | Campo único                             | Inferior primeiro    |
| MFVideoInteritor \_ MixedIntertoresOrProgressive | Pode variar    | Campos intercalados ou quadros progressivos | Pode variar       |



 

Campos intercalados e campos individuais não podem ser mistos. Alternar de um para outro requer uma alteração de tipo de mídia.

## <a name="interlace-flags-on-samples"></a>Sinalizadores intercalar em exemplos

As informações que podem mudar de um exemplo para o próximo são indicadas usando atributos de exemplo. Use a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para obter ou definir esses atributos.

Todos os atributos de entrelaçamento listados nesta seção têm valores boolianas. Efetivamente, cada um desses atributos pode ter três valores: **TRUE,** **FALSE** ou não definido. Se um atributo não for definido, o valor será retirado do tipo de mídia. Se um atributo for definido, o valor substituirá o tipo de mídia. Algumas combinações de sinalizadores e tipos de mídia não são válidas.




| Atributo | Descrição | 
|-----------|-------------|
| <a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a> | Se <strong>TRUE</strong>, o quadro será entrelaçado. Se <strong>FALSE</strong>, o quadro será progressivo.<br /> De definir esse atributo em cada exemplo se o tipo de mídia for MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a> | O significado desse sinalizador depende se os exemplos contêm campos intercalados ou campos individuais.<br /><ul><li>Campos intercalados: se <strong>TRUE</strong>, o campo inferior será o primeiro. Se <strong>FALSE</strong>, o campo superior será o primeiro.<br /></li><li>Campos individuais: se <strong>TRUE</strong>, o exemplo conterá um campo inferior. Se <strong>FALSE</strong>, o exemplo conterá um campo superior.<br /></li></ul>De definir esse atributo em cada exemplo de intercala se o tipo de mídia for MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower ou MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a> | Se <strong>TRUE</strong>, o primeiro campo será repetido. Se <strong>FALSE</strong> ou não for definido, o primeiro campo não será repetido. | 
| <a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a> | Se <strong>TRUE</strong>, o exemplo conterá um único campo. Se <strong>FALSE</strong>, o exemplo conterá campos intercalados. | 




 

A tabela a seguir mostra quais sinalizadores são obrigatórios, opcionais ou proibidos, com base no tipo de mídia.



| Tipo de Mídia         | Sinalizador entrelaçado                      | Sinalizador BottomFieldFirst                    | Sinalizador RepeatFirstField | Sinalizador de únicofield                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| Progressivo        | Adicional Se definido, deve ser **false**. | Não definir.                              | Não definir.           | Não definir.                          |
| Campos intercalados | Adicional Se definido, deve ser **verdadeiro**.  | Adicional Se definido, deve corresponder ao tipo de mídia. | Não definir.           | Adicional Se definido, deve ser **false**. |
| Campos únicos      | Adicional Se definido, deve ser **verdadeiro**.  | Obrigatórios.                                | Não definir.           | Defina como **true**.                     |
| Mixed              | Obrigatórios.                            | Obrigatórios.                                | Obrigatórios.             | Adicional Se definido, deve ser **false**. |



 

Nos casos em que o atributo é opcional, o tipo de mídia já define as informações. É válido definir o atributo para corresponder, mas não obrigatório.

Por exemplo, se o tipo de mídia for MFVideoInterlace \_ progressivo, ele implica que todos os quadros no fluxo são progressivos. Portanto, você pode definir o atributo **\_ entrelaçado MFSampleExtension** como **false** ou deixar a definição do atributo.

## <a name="recommendations"></a>Recomendações

Esta seção contém recomendações para vários tipos de conteúdo.

1. O vídeo é todos os quadros progressivos.

-   Defina o tipo de mídia como MFVideoInterlace \_ progressivo.

-   Não defina o atributo **\_ entrelaçado MFSampleExtension** ou defina-o como **false** em todos os quadros.

-   Não defina os atributos **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** ou **MFSampleExtension \_ singlefield** .

2. O vídeo é todos os campos entrelaçados com o mesmo campo predominância. Os exemplos contêm campos intercalados.

-   Defina o tipo de mídia como MFVideoInterlace \_ FieldInterleavedUpperFirst ou MFVideoInterlace \_ FieldInterleavedLowerFirst.

-   Não defina o atributo **\_ entrelaçado MFSampleExtension** ou defina-o como **true** em todos os quadros.

-   Não defina o atributo **MFSampleExtension \_ BottomFieldFirst** ou defina o valor em cada quadro para corresponder ao tipo de mídia.

-   Não defina o atributo **MFSampleExtension \_ RepeatFirstField** ou defina-o como **false** em todos os quadros.

-   Não defina o atributo **MFSampleExtension \_ únicofield** ou defina-o como **false** em todos os quadros.

3. O vídeo contém uma mistura de quadros entrelaçados e progressivos, com campos repetidos e predominância de campo variável (por exemplo, vídeo de DVD).

-   Defina o tipo de mídia como MFVideoInterlace \_ MixedInterlaceOrProgressive.

-   Em cada quadro, defina os atributos **MFSampleExtension \_ entrelaçado**, **MFSampleExtension \_ BottomFieldFirst** e **MFSampleExtension \_ RepeatFirstField** .

-   Não defina o atributo **MFSampleExtension \_ únicofield** ou defina-o como **false** em todos os quadros.

4. O vídeo é entrelaçado e os exemplos contêm campos únicos.

-   Defina o tipo de mídia como MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower.

-   Em cada quadro, defina o atributo **MFSampleExtension \_ BottomFieldFirst** .

-   Não defina o atributo **\_ entrelaçado MFSampleExtension** ou defina-o como **true** em todos os quadros.

-   Não defina o atributo **MFSampleExtension \_ RepeatFirstField** ou defina-o como **false** em todos os quadros.

-   Não defina o atributo **MFSampleExtension \_ únicofield** ou defina-o como **true** em todos os quadros.

A maior parte do conteúdo de vídeo se encaixa em uma dessas categorias.

## <a name="mpeg-2-mappings"></a>Mapeamentos MPEG-2

Para conteúdo MPEG-2, use os seguintes mapeamentos para converter os sinalizadores MPEG-2 em Media Foundation atributos de exemplo.

**estrutura da imagem \_**



| Valor         | Atributo de exemplo                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| frame         | **MFSampleExtension \_ Únicofield**  =  **falso**                                                                          |
| \_campo superior    | **MFSampleExtension \_ Únicofield**  =  **verdadeiro**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **false**<br/> |
| \_campo inferior | **MFSampleExtension \_ Únicofield**  =  **verdadeiro**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **true**<br/>  |



 

**quadro progressivo \_**



| Valor | Atributo de exemplo                              |
|-------|-----------------------------------------------|
| 0     | **MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**  |
| 1     | **MFSampleExtension \_ Falso entrelaçado**  =   |



 

**\_primeiro campo \_ principal**



| Valor | Atributo de exemplo                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ BottomFieldFirst**  =  **true**  |
| 1     | **MFSampleExtension \_ BottomFieldFirst**  =  **false** |



 

**repetir \_ primeiro \_ campo**



| Valor | Atributo de exemplo                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ RepeatFirstField**  =  **false** |
| 1     | **MFSampleExtension \_ RepeatFirstField**  =  **true**  |



 

## <a name="single-field-samples"></a>Exemplos de Single-Field

Se o tipo de mídia for MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower, significa que cada exemplo contém um único campo. No entanto, o tipo de mídia descreve o quadro inteiro. Portanto, cada buffer contém apenas metade do número de linhas de campo fornecidas no tipo de mídia. Por exemplo, se o tipo de mídia descrever o vídeo como 720 × 480, cada campo conterá 240 linhas de varredura e, portanto, cada buffer conterá apenas 240 linhas de pixels. Se você escrever um componente que aceite tipos de mídia com exemplos de campo único, deverá levar esse fato em conta ao acessar os dados no buffer.

A mesma regra se aplica à abertura geométrica (atributo de[ \_ \_ \_ abertura geométrica MF MT](mf-mt-geometric-aperture-attribute.md) ) e à abertura de exibição mínima (atributo de[ \_ \_ \_ \_ abertura de exibição mínima de MF MT](mf-mt-minimum-display-aperture-attribute.md) ). Essas regiões são especificadas em termos de todo o quadro, não dos campos individuais.

## <a name="directshow-mappings"></a>DirectShow Mapeamentos

no DirectShow, as informações de entrelaçamento por amostra estão contidas no membro **dwTypeSpecificFlags** da estrutura de **\_ \_ propriedades AM SAMPLE2** . A tabela a seguir mostra os atributos equivalentes para Media Foundation.



| sinalizador de exemplo de DirectShow              | Media Foundation atributo de exemplo                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ quadro intercalado do sinalizador de vídeo am \_ | **MFSampleExtension \_ Únicofield**  =  **falso**.                                                                                                                                    |
| \_Campo1 do \_ sinalizador de vídeo am \_             | **MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**.<br/> **MFSampleExtension \_ SingleField**  =  **TRUE.**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE.**<br/> |
| CAMPO \_ DO SINALIZADOR DE VÍDEO \_ \_ AM2             | **MFSampleExtension \_ TRUE**  =  **entrelaçado.**<br/> **MFSampleExtension \_ SingleField**  =  **TRUE.**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **TRUE.**<br/>  |
| TEAVE \_ DO SINALIZADOR DE VÍDEO \_ \_ AM              | **MFSampleExtension \_ FALSE**  =  **entrelaçado.** (Esse sinalizador indica que o driver não deve desinteressar os dois campos.)                                                        |
| AM \_ VIDEO \_ FLAG \_ FIELD1FIRST        | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE.** Se o conteúdo estiver entrelaçado e o sinalizador \_ FIELD1FIRST do SINALIZADOR DE VÍDEO AM não estiver presente, de definir \_ \_ esse atributo como **TRUE.**        |
| CAMPO \_ DE REPETIÇÃO DO SINALIZADOR DE VÍDEO \_ \_ \_ AM      | **MFSampleExtension \_ RepeatFirstField**  =  **TRUE.** Se o sinalizador AM \_ VIDEO FLAG REPEAT FIELD não estiver \_ \_ \_ presente, de definir esse atributo como **FALSE.**                                    |



 

Se o DirectShow exemplo não contém sinalizadores de exemplo, use o valor **dwInterheadFlags** da **estrutura VIDEOINFOHEADER2:**



| DirectShow sinalizador de intercala    | Media Foundation de exemplo                    |
|------------------------------|------------------------------------------------------|
| AMINTER FRAME \_ IsInterlaced    | **MFSampleExtension \_ TRUE**  =  **entrelaçado.**        |
| AMINTER OPERAÇÃO \_ 1FieldPerSample | **MFSampleExtension \_ SingleField**  =  **TRUE.**       |
| AMINTER METEOR \_ Field1First     | **MFSampleExtension \_ BottomFieldFirst**  =  **FALSE.** |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 




