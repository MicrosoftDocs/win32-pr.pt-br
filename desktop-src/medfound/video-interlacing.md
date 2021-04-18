---
description: Entrelaçamento de vídeo
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Entrelaçamento de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813654"
---
# <a name="video-interlacing"></a>Entrelaçamento de vídeo

Este tópico descreve como as fontes de mídia e os decodificadores devem lidar com conteúdo de vídeo entrelaçado.

Para decodificar e renderizar o vídeo entrelaçado corretamente, as seguintes informações são necessárias:

-   Progressivo ou entrelaçado. Um fluxo de vídeo pode conter quadros progressivos, quadros entrelaçados ou uma mistura de ambos.

-   Campo predominância. O campo predominância descreve qual campo aparece primeiro, o campo superior ou o campo inferior.

-   Repita o primeiro campo. Esse sinalizador é usado na reestruturação de 3:2, quando o quadro é progressivo, mas o fluxo é entrelaçado. Nesse contexto, o primeiro campo pode ser o campo superior ou inferior.

-   Campos intercalados ou campo único. Um exemplo pode conter um único campo ou dois campos intercalados. Se um exemplo contiver um único campo, a altura de amostra será metade da altura do quadro, pois o exemplo contém apenas metade das linhas de varredura de um quadro. Os campos intercalados são recomendados, a menos que as características do conteúdo de origem ditem de outra forma.

Qualquer uma dessas características pode mudar de uma amostra para a próxima. No entanto, os componentes de vídeo precisam saber algo sobre o conteúdo geral antes de o streaming começar. Por exemplo, se o vídeo estiver entrelaçado, o processador de vídeo avançado (EVR) precisa reservar memória de vídeo para o desentrelaçamento. Se o vídeo for totalmente progressivo, por outro lado, o EVR poderá otimizar o pipeline de renderização. Adicionar uma etapa de desentrelaçamento ao pipeline aumenta a latência de renderização.

As informações sobre o entrelaçamento são armazenadas em dois locais:

-   As informações gerais sobre o entrelaçamento em um fluxo são colocadas no tipo de mídia. Para obter mais informações sobre tipos de mídia, consulte [tipos de mídia](media-types.md).

-   As informações que podem ser alteradas com cada exemplo são colocadas no exemplo como um atributo. Para obter mais informações sobre exemplos, consulte [amostras de mídia](media-samples.md).

## <a name="interlace-information-in-the-media-type"></a>Entrelaçar informações no tipo de mídia

O atributo do [**\_ \_ \_ modo de entrelaçamento MF MT**](mf-mt-interlace-mode-attribute.md) no tipo de mídia descreve como o fluxo como um todo é entrelaçado. O valor desse atributo é um membro da enumeração [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) . Um tipo de mídia de vídeo sempre deve ter esse atributo.

-   Se o fluxo contiver apenas quadros progressivos, sem quadros entrelaçados, use MFVideoInterlace \_ progressivo.
-   Se o fluxo contiver apenas quadros entrelaçados e cada amostra contiver dois campos intercalados, use MFVideoInterlace \_ FieldInterleavedUpperFirst ou MFVideoInterlace \_ FieldInterleavedLowerFirst.
-   Se o fluxo contiver apenas quadros entrelaçados e cada amostra contiver um único campo, use MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower. Se os campos forem alternados entre superior e inferior, não importa quais desses dois valores são usados. Se o formato contiver apenas campos maiúsculos ou apenas campos inferiores, defina o valor que corresponde ao conteúdo.
-   Se o fluxo contiver uma combinação de quadros entrelaçados e progressivos, ou se o campo predominância alternar, defina o tipo de mídia como MFVideoInterlace \_ MixedInterlaceOrProgressive. Use atributos de exemplo para descrever cada quadro.

A tabela a seguir resume esse atributo.



| \_modo de \_ entrelaçamento do MF MT \_                       | Entrelaçadas? | Exemplos                                  | Primeiro campo    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MFVideoInterlace \_ progressivo                 | No          | Quadro progressivo                        | Não aplicável |
| MFVideoInterlace \_ FieldInterleavedUpperFirst  | Yes         | Campos intercalados                       | Primeiro superior    |
| MFVideoInterlace \_ FieldInterleavedLowerFirst  | Yes         | Campos intercalados                       | Primeiro abaixo    |
| MFVideoInterlace \_ FieldSingleUpper            | Yes         | Campo único                             | Primeiro superior    |
| MFVideoInterlace \_ FieldSingleLower            | Yes         | Campo único                             | Primeiro abaixo    |
| MFVideoInterlace \_ MixedInterlaceOrProgressive | Pode variar    | Campos intercalados ou quadros progressivos | Pode variar       |



 

Campos intercalados e campos únicos não podem ser misturados. Alternar de um para outro requer uma alteração de tipo de mídia.

## <a name="interlace-flags-on-samples"></a>Sinalizadores de entrelaçamento em exemplos

As informações que podem mudar de uma amostra para a próxima são indicadas usando atributos de exemplo. Use a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para obter ou definir esses atributos.

Todos os atributos de entrelaçamento listados nesta seção têm valores Boolianos. Efetivamente, cada um desses atributos pode ter três valores: **true**, **false** ou não definido. Se um atributo não estiver definido, o valor será obtido do tipo de mídia. Se um atributo for definido, o valor substituirá o tipo de mídia. Algumas combinações de sinalizadores e tipos de mídia não são válidas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></td>
<td>Se for <strong>true</strong>, o quadro será entrelaçado. Se for <strong>false</strong>, o quadro será progressivo.<br/> Defina esse atributo em cada exemplo se o tipo de mídia for MFVideoInterlace_MixedInterlaceOrProgressive.<br/></td>
</tr>
<tr class="even">
<td><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></td>
<td>O significado desse sinalizador depende se os exemplos contêm campos intercalados ou campos únicos.<br/>
<ul>
<li>Campos intercalados: se <strong>for verdadeiro</strong>, o campo inferior será o primeiro. Se for <strong>false</strong>, o campo superior será primeiro.<br/></li>
<li>Campos únicos: se <strong>for true</strong>, o exemplo conterá um campo inferior. Se <strong>for false</strong>, o exemplo conterá um campo superior.<br/></li>
</ul>
Defina esse atributo em cada amostra de entrelaçamento se o tipo de mídia for MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower ou MFVideoInterlace_MixedInterlaceOrProgressive.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></td>
<td>Se <strong>for true</strong>, o primeiro campo será repetido. Se for <strong>false</strong> ou not set, o primeiro campo não será repetido.</td>
</tr>
<tr class="even">
<td><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></td>
<td>Se <strong>for true</strong>, o exemplo conterá um único campo. Se <strong>for false</strong>, o exemplo conterá campos intercalados.</td>
</tr>
</tbody>
</table>



 

A tabela a seguir mostra quais sinalizadores são necessários, opcionais ou proibidos, com base no tipo de mídia.



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

## <a name="directshow-mappings"></a>Mapeamentos do DirectShow

No DirectShow, as informações de entrelaçamento por amostra estão contidas no membro **dwTypeSpecificFlags** da estrutura de **\_ \_ Propriedades am SAMPLE2** . A tabela a seguir mostra os atributos equivalentes para Media Foundation.



| Sinalizador de exemplo do DirectShow              | Media Foundation atributo de exemplo                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ quadro intercalado do sinalizador de vídeo am \_ | **MFSampleExtension \_ Únicofield**  =  **falso**.                                                                                                                                    |
| \_Campo1 do \_ sinalizador de vídeo am \_             | **MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**.<br/> **MFSampleExtension \_ Singlefield**  =  **verdadeiro**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **false**.<br/> |
| \_Sinalizador de vídeo am \_ \_ campo2             | **MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**.<br/> **MFSampleExtension \_ Singlefield**  =  **verdadeiro**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **true**.<br/>  |
| \_sinalizador de vídeo am \_ \_ trançado              | **MFSampleExtension \_ Falso entrelaçado**  =  . (Esse sinalizador indica que o driver não deve desentrelaçar os dois campos.)                                                        |
| \_Sinalizador de vídeo am \_ \_ FIELD1FIRST        | **MFSampleExtension \_ BottomFieldFirst**  =  **false**. Se o conteúdo for entrelaçado e o \_ sinalizador FIELD1FIRST do sinalizador de vídeo am \_ \_ não estiver presente, defina esse atributo como **true**.        |
| \_campo de \_ repetição do sinalizador de vídeo am \_ \_      | **MFSampleExtension \_ RepeatFirstField**  =  **true**. Se o \_ sinalizador de campo de repetição do sinalizador de vídeo am \_ \_ \_ não estiver presente, defina esse atributo como **false**.                                    |



 

Se o exemplo do DirectShow não contiver sinalizadores de exemplo, use o valor de **dwInterlaceFlags** da estrutura **VIDEOINFOHEADER2** :



| Sinalizador de entrelaçamento do DirectShow    | Media Foundation atributo de exemplo                    |
|------------------------------|------------------------------------------------------|
| \_Isentrelaçado AMINTERLACE    | **MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**.        |
| AMINTERLACE \_ 1FieldPerSample | **MFSampleExtension \_ Singlefield**  =  **verdadeiro**.       |
| AMINTERLACE \_ Field1First     | **MFSampleExtension \_ BottomFieldFirst**  =  **false**. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 




