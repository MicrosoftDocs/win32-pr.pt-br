---
description: Filtro de navegador de DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtro de navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d248e490201536e92afeb38f520028e29ea9a5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477292"
---
# <a name="dvd-navigator-filter"></a>Filtro de navegador de DVD

O filtro Navegador de DVD é o filtro de origem para um DVD-Video de filtro de reprodução. Ele abre todos os arquivos necessários em um volume DVD-Video, navega pelos arquivos .vob lineares do DVD-Video e analisará o fluxo de programas MPEG-2 resultante, dividindo o fluxo em três pinos de saída (vídeo, áudio, subtípico).

O filtro Navegador de DVD também implementa as interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) que permitem que um aplicativo de reprodução de DVD controle DVD-Video reprodução.




| | | Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter,</strong></a> <strong>ISpecifyPropertyPages</strong> | | Tipos de mídia de pino de entrada | MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM | | Interfaces de pino de entrada | Não aplicável. | | Tipos de mídia de pino de | Tipos base:<br /><ul><li>Vídeo: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li>Áudio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li>Subtípico: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Tipos estendidos:<br /> Vídeo:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li></ul>Áudio:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li></ul>Subimagem:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Para habilitar os tipos estendidos, chame <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> e de definir o <br /> | | Interfaces de pino de | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar CLSID | CLSID_DVDNavigator | | ClSID da página de propriedades | Nenhuma página de propriedades. | | Arquivo executável | qdvd.dll | | <a href="merit.md">|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 




