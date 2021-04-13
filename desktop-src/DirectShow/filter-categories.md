---
description: As tabelas a seguir listam os CLSIDs para as categorias de filtro do DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtrar categorias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370071"
---
# <a name="filter-categories"></a>Filtrar categorias

As tabelas a seguir listam os CLSIDs para as categorias de filtro do DirectShow.

-   [Categorias de filtro do DirectShow](#directshow-filter-categories)
-   [Outras categorias de filtro](#other-filter-categories)
-   [Metacategoria de filtro do DirectShow](#directshow-filter-meta-category)
-   [Categorias de DMO](#dmo-categories)
-   [Tópicos relacionados](#related-topics)

## <a name="directshow-filter-categories"></a>Categorias de filtro do DirectShow

As categorias listadas aqui são enumeradas pelo [mapeador de filtro](filter-mapper.md). Por padrão, no entanto, o mapeador de filtro ignora as categorias com méritos de mérito \_ \_ não \_ usam ou menos. Para obter mais informações, consulte [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Todas as categorias listadas aqui também podem ser enumeradas com o [enumerador de dispositivo do sistema](system-device-enumerator.md).

As categorias a seguir são declaradas em UUIDs. h. Inclua o arquivo de cabeçalho DShow. h.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome amigável</th>
<th>CLSID</th>
<th>Núcleo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Fontes de captura de áudio</td>
<td><strong>CLSID_AudioInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Compactadores de áudio</td>
<td><strong>CLSID_AudioCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Renderizadores de áudio</td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Filtros de controle de dispositivo</td>
<td><strong>CLSID_DeviceControlCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Filtros do DirectShow</td>
<td><strong>CLSID_LegacyAmFilterCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Renderizadores externos</td>
<td><strong>CLSID_TransmitCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Renderizadores Midi</td>
<td><strong>CLSID_MidiRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Fontes de captura de vídeo</td>
<td><strong>CLSID_VideoInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Compactadores de vídeo</td>
<td><strong>CLSID_VideoCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivos de descompactação de fluxo WDM</td>
<td><strong>CLSID_DVDHWDecodersCategory</strong>
<blockquote>
[!Note]<br />
Esta categoria contém decodificadores de DVD de hardware.
</blockquote>
<br/></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivos de captura de fluxo WDM</td>
<td><strong>AM_KSCATEGORY_CAPTURE</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivos Crossbar de streaming WDM</td>
<td><strong>AM_KSCATEGORY_CROSSBAR</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivos de renderização de streaming WDM</td>
<td><strong>AM_KSCATEGORY_RENDER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivos de divisão/divisor de streaming WDM</td>
<td><strong>AM_KSCATEGORY_SPLITTER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivos de áudio de TV de streaming WDM</td>
<td><strong>AM_KSCATEGORY_TVAUDIO</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivos de sintonização de TV de streaming WDM</td>
<td><strong>AM_KSCATEGORY_TVTUNER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Codecs VBI de streaming WDM</td>
<td><strong>AM_KSCATEGORY_VBICODEC</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
</tbody>
</table>



 

As categorias a seguir são declaradas no arquivo de cabeçalho KS. h.



| Nome amigável                          | CLSID                                   | Núcleo                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Transformações de comunicação de streaming WDM | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **MÉRITO \_ \_ não \_ use** |
| Transformações de dados de streaming WDM          | **KSCATEGORY \_ DATAtransform**           | **MÉRITO \_ \_ não \_ use** |
| Transformações de interface de streaming WDM     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **MÉRITO \_ \_ não \_ use** |
| Dispositivos de mixer de streaming WDM            | **MIXER de KSCATEGORY \_**                   | **MÉRITO \_ \_ não \_ use** |



 

As categorias a seguir são declaradas no arquivo de cabeçalho Bdamedia. h. Inclua os seguintes arquivos de cabeçalho: KS. h, ksmedia. h e bdamedia. h.



| Nome amigável                       | CLSID                                       | Núcleo                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Provedores de rede BDA               | **\_provedor de \_ rede \_ BDA KSCATEGORY**      | **MÉRITO \_ normal**       |
| Componentes do receptor BDA             | **\_ \_ componente receptor do KSCATEGORY BDA \_**    | **MÉRITO \_ \_ não \_ use** |
| Filtros de renderização BDA               | **\_coletor de IP KSCATEGORY \_**                    | **MÉRITO \_ \_ não \_ use** |
| Filtros de origem BDA                  | **\_ \_ sintonizador de rede BDA KSCATEGORY \_**         | **MÉRITO \_ \_ não \_ use** |
| Renderizadores de informações de transporte BDA | **\_informações de \_ transporte \_ BDA KSCATEGORY** | **MÉRITO \_ normal**       |



 

> [!Note]  
> Os decodificadores são registrados na categoria "filtros do DirectShow" (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Outras categorias de filtro

As categorias listadas aqui podem ser enumeradas com o enumerador de dispositivo do sistema, mas não são visíveis para o mapeador de filtro e não são usadas pelo [Intelligent Connect](intelligent-connect.md).

As categorias a seguir são declaradas no arquivo de cabeçalho QEdit. h.



| Nome amigável            | CLID                             | Núcleo                   |
|--------------------------|----------------------------------|-------------------------|
| Efeitos de vídeo (1 entrada)  | **\_VIDEOEFFECTS1CATEGORY CLSID** | **MÉRITO \_ \_ não \_ use** |
| Efeitos de vídeo (2 entradas) | **\_VIDEOEFFECTS2CATEGORY CLSID** | **MÉRITO \_ \_ não \_ use** |



 

Essas categorias contêm efeitos de vídeo e transições para [serviços de edição do DirectShow](directshow-editing-services.md):

-   "Efeitos de vídeo (1 entrada)" contém efeitos de vídeo.
-   "Efeitos de vídeo (2 entrada)" contém transições de vídeo.

Para obter mais informações, consulte [enumerando efeitos e transições](enumerating-effects-and-transitions.md).

As categorias a seguir são declaradas no arquivo de cabeçalho UUIDs. h. Inclua o arquivo de cabeçalho DShow. h.



| Nome amigável       | CLID                                | Núcleo                   |
|---------------------|-------------------------------------|-------------------------|
| Codificadores do encapi     | **\_MEDIAENCODERCATEGORY CLSID**     | **MÉRITO \_ \_ não \_ use** |
| Multiplexadores de encapi | **\_MEDIAMULTIPLEXERCATEGORY CLSID** | **MÉRITO \_ \_ não \_ use** |



 

## <a name="directshow-filter-meta-category"></a>Filtro do DirectShow Meta-Category



| Nome amigável                 | CLSID                            | Núcleo          |
|-------------------------------|----------------------------------|----------------|
| Categorias de filtro do ActiveMovie | **\_ACTIVEMOVIECATEGORIES CLSID** | Não aplicável |



 

Essa meta-categoria contém uma lista de categorias de filtro. Se uma categoria de filtro não aparecer nessa lista, o [mapeador de filtro](filter-mapper.md) ignorará a categoria, o que significa que o filtro não está disponível para [conexão inteligente](intelligent-connect.md).

Para enumerar a lista de categorias de filtro, chame [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o valor CLSID \_ ActiveMovieCategories. Os monikers retornados por esse método dão suporte às propriedades a seguir.



| Nome da propriedade  | Descrição                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| FriendlyName | Nome da categoria (VT \_ BSTR).                                                              |
| Núcleo        | Mérito de categoria (VT \_ i4). Se essa propriedade estiver ausente, trate como **mérito \_ não \_ \_ usar**. |
| CLSID        | CLSID da categoria (VT \_ BSTR).                                                             |



 

Para adicionar uma nova categoria de filtro a essa lista, chame [**IFilterMapper2:: createcategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>Categorias de DMO

Os DMOs (objetos de mídia do DirectX) usam um mecanismo de enumeração diferente dos filtros do DirectShow. Para obter mais informações, consulte [registrando um DMO](registering-a-dmo.md). No entanto, você pode usar o enumerador de dispositivo do sistema para enumerar categorias DMO. Os monikers são associados ao [filtro de invólucro do DMO](dmo-wrapper-filter.md) e inicializam automaticamente o filtro com o DMO.

Além disso, algumas das categorias de DMO são mapeadas para categorias de filtro do DirectShow para fins de conexão inteligente:



| Categoria de DMO                    | Equivalente do DirectShow              |
|---------------------------------|------------------------------------|
| **\_codificador de áudio DMOCATEGORY \_** | **\_AUDIOCOMPRESSORCATEGORY CLSID** |
| **\_decodificador de áudio DMOCATEGORY \_** | **\_LEGACYAMFILTERCATEGORY CLSID**  |
| **\_codificador de vídeo DMOCATEGORY \_** | **\_VIDEOCOMPRESSORCATEGORY CLSID** |
| **\_decodificador de vídeo DMOCATEGORY \_** | **\_LEGACYAMFILTERCATEGORY CLSID**  |



 

Observe que as categorias de efeito de vídeo e de efeito de áudio não são mapeadas para nenhuma categoria do DirectShow.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes e GUIDs](constants-and-guids.md)
</dt> <dt>

[Enumerando dispositivos e filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Conexão inteligente](intelligent-connect.md)
</dt> <dt>

[Layout das chaves do registro](layout-of-the-registry-keys.md)
</dt> <dt>

[Usando o mapeador de filtro](using-the-filter-mapper.md)
</dt> <dt>

[Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




