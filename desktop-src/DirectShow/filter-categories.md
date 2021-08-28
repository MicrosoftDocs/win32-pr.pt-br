---
description: as tabelas a seguir listam os clsids para as categorias de filtro de DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtrar categorias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e8c2b5e5f9e477633774cb24e707aa9d71060
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476322"
---
# <a name="filter-categories"></a>Filtrar categorias

as tabelas a seguir listam os clsids para as categorias de filtro de DirectShow.

-   [DirectShow Filtrar categorias](#directshow-filter-categories)
-   [Outras categorias de filtro](#other-filter-categories)
-   [DirectShow Meta categoria do filtro](#directshow-filter-meta-category)
-   [DMO Às](#dmo-categories)
-   [Tópicos relacionados](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow Filtrar categorias

As categorias listadas aqui são enumeradas pelo [mapeador de filtro](filter-mapper.md). Por padrão, no entanto, o mapeador de filtro ignora as categorias com méritos de mérito \_ \_ não \_ usam ou menos. Para obter mais informações, consulte [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Todas as categorias listadas aqui também podem ser enumeradas com o [enumerador de dispositivo do sistema](system-device-enumerator.md).

As categorias a seguir são declaradas em UUIDs. h. Inclua o arquivo de cabeçalho DShow. h.




| Nome amigável | CLSID | Núcleo | 
|---------------|-------|-------|
| Fontes de captura de áudio | <strong>CLSID_AudioInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Compactadores de áudio | <strong>CLSID_AudioCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Renderizadores de áudio | <strong>CLSID_AudioRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Filtros de controle de dispositivo | <strong>CLSID_DeviceControlCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| DirectShow Filter | <strong>CLSID_LegacyAmFilterCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Renderizadores externos | <strong>CLSID_TransmitCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Renderizadores Midi | <strong>CLSID_MidiRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Fontes de captura de vídeo | <strong>CLSID_VideoInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Compactadores de vídeo | <strong>CLSID_VideoCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de descompactação de fluxo WDM | <strong>CLSID_DVDHWDecodersCategory</strong><blockquote>[!Note]<br />Esta categoria contém decodificadores de DVD de hardware.</blockquote><br /> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de captura de fluxo WDM | <strong>AM_KSCATEGORY_CAPTURE</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos Crossbar de streaming WDM | <strong>AM_KSCATEGORY_CROSSBAR</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de renderização de streaming WDM | <strong>AM_KSCATEGORY_RENDER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de divisão/divisor de streaming WDM | <strong>AM_KSCATEGORY_SPLITTER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de áudio de TV de streaming WDM | <strong>AM_KSCATEGORY_TVAUDIO</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de sintonização de TV de streaming WDM | <strong>AM_KSCATEGORY_TVTUNER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Codecs VBI de streaming WDM | <strong>AM_KSCATEGORY_VBICODEC</strong> | <strong>MERIT_DO_NOT_USE</strong> | 




 

As categorias a seguir são declaradas no arquivo de cabeçalho KS. h.



| Nome amigável                          | CLSID                                   | Núcleo                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Transformações de comunicação de streaming WDM | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **MÉRITO \_ \_ não \_ use** |
| Transformações de dados de streaming WDM          | **KSCATEGORY \_ DATAtransform**           | **MÉRITO \_ \_ não \_ use** |
| Transformações de interface de streaming WDM     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **MÉRITO \_ \_ não \_ use** |
| dispositivos Mixer de Streaming WDM            | **MIXER de KSCATEGORY \_**                   | **MÉRITO \_ \_ não \_ use** |



 

As categorias a seguir são declaradas no arquivo de cabeçalho Bdamedia. h. Inclua os seguintes arquivos de cabeçalho: KS. h, ksmedia. h e bdamedia. h.



| Nome amigável                       | CLSID                                       | Núcleo                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Provedores de rede BDA               | **\_provedor de \_ rede \_ BDA KSCATEGORY**      | **MÉRITO \_ normal**       |
| Componentes do receptor BDA             | **\_ \_ componente receptor do KSCATEGORY BDA \_**    | **MÉRITO \_ \_ não \_ use** |
| Filtros de renderização BDA               | **\_coletor de IP KSCATEGORY \_**                    | **MÉRITO \_ \_ não \_ use** |
| Filtros de origem BDA                  | **\_ \_ sintonizador de rede BDA KSCATEGORY \_**         | **MÉRITO \_ \_ não \_ use** |
| Renderizadores de informações de transporte BDA | **\_informações de \_ transporte \_ BDA KSCATEGORY** | **MÉRITO \_ normal**       |



 

> [!Note]  
> os decodificadores são registrados na categoria "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Outras categorias de filtro

as categorias listadas aqui podem ser enumeradas com o enumerador de dispositivo do sistema, mas não são visíveis para o mapeador de filtro e não são usadas pelo [Conexão inteligente](intelligent-connect.md).

As categorias a seguir são declaradas no arquivo de cabeçalho QEdit. h.



| Nome amigável            | CLID                             | Núcleo                   |
|--------------------------|----------------------------------|-------------------------|
| Efeitos de vídeo (1 entrada)  | **\_VIDEOEFFECTS1CATEGORY CLSID** | **MÉRITO \_ \_ não \_ use** |
| Efeitos de vídeo (2 entradas) | **\_VIDEOEFFECTS2CATEGORY CLSID** | **MÉRITO \_ \_ não \_ use** |



 

essas categorias contêm efeitos de vídeo e transições para [DirectShow serviços de edição](directshow-editing-services.md):

-   "Efeitos de vídeo (1 entrada)" contém efeitos de vídeo.
-   "Efeitos de vídeo (2 entrada)" contém transições de vídeo.

Para obter mais informações, consulte [enumerando efeitos e transições](enumerating-effects-and-transitions.md).

As categorias a seguir são declaradas no arquivo de cabeçalho UUIDs. h. Inclua o arquivo de cabeçalho DShow. h.



| Nome amigável       | CLID                                | Núcleo                   |
|---------------------|-------------------------------------|-------------------------|
| Codificadores do encapi     | **\_MEDIAENCODERCATEGORY CLSID**     | **MÉRITO \_ \_ não \_ use** |
| Multiplexadores de encapi | **\_MEDIAMULTIPLEXERCATEGORY CLSID** | **MÉRITO \_ \_ não \_ use** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow Meta-Category de filtro



| Nome amigável                 | CLSID                            | Núcleo          |
|-------------------------------|----------------------------------|----------------|
| Categorias de filtro do ActiveMovie | **\_ACTIVEMOVIECATEGORIES CLSID** | Não aplicável |



 

Essa meta-categoria contém uma lista de categorias de filtro. se uma categoria de filtro não aparecer nessa lista, o [mapeador de filtro](filter-mapper.md) ignorará a categoria, o que significa que o filtro não está disponível para o [Conexão inteligente](intelligent-connect.md).

Para enumerar a lista de categorias de filtro, chame [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o valor CLSID \_ ActiveMovieCategories. Os monikers retornados por esse método dão suporte às propriedades a seguir.



| Nome da propriedade  | Descrição                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| FriendlyName | Nome da categoria (VT \_ BSTR).                                                              |
| Núcleo        | Mérito de categoria (VT \_ i4). Se essa propriedade estiver ausente, trate como **mérito \_ não \_ \_ usar**. |
| CLSID        | CLSID da categoria (VT \_ BSTR).                                                             |



 

Para adicionar uma nova categoria de filtro a essa lista, chame [**IFilterMapper2:: createcategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>DMO Às

os DMOs (objetos de mídia do DirectX) usam um mecanismo de enumeração diferente dos filtros DirectShow. Para obter mais informações, consulte [registrando um DMO](registering-a-dmo.md). no entanto, você pode usar o enumerador de dispositivo do sistema para enumerar DMO categorias. os monikers são associados ao [filtro de Wrapper de DMO](dmo-wrapper-filter.md) e inicializam automaticamente o filtro com o DMO.

além disso, algumas das categorias de DMO são mapeadas para DirectShow categorias de filtro para fins de conexão inteligente:



| DMO Categorias                    | DirectShow Equivalente              |
|---------------------------------|------------------------------------|
| **\_codificador de áudio DMOCATEGORY \_** | **\_AUDIOCOMPRESSORCATEGORY CLSID** |
| **\_decodificador de áudio DMOCATEGORY \_** | **\_LEGACYAMFILTERCATEGORY CLSID**  |
| **\_codificador de vídeo DMOCATEGORY \_** | **\_VIDEOCOMPRESSORCATEGORY CLSID** |
| **\_decodificador de vídeo DMOCATEGORY \_** | **\_LEGACYAMFILTERCATEGORY CLSID**  |



 

observe que as categorias de efeito de vídeo e de efeito de áudio não são mapeadas para nenhuma categoria de DirectShow.

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

 

 




