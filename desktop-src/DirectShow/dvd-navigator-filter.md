---
description: Filtro de navegador de DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtro de navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a395001daeac5f90be85bea972d1d4f118198ee4343960cb4eed0d958e1677aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016004"
---
# <a name="dvd-navigator-filter"></a>Filtro de navegador de DVD

O filtro Navegador de DVD é o filtro de origem para um DVD-Video de filtro de reprodução. Ele abre todos os arquivos necessários em um volume DVD-Video, navega pelos arquivos .vob lineares do DVD-Video e analisado o fluxo de programas MPEG-2 resultante, dividindo o fluxo em três pinos de saída (vídeo, áudio, subtípico).

O filtro Navegador de DVD também implementa as interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) que permitem que um aplicativo de reprodução de DVD controle DVD-Video reprodução.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter,</strong></a> <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td>Não aplicável.</td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de saída</td>
<td>Tipos base:<br/>
<ul>
<li>Vídeo: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li>Áudio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li>Subtípico: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Tipos estendidos:<br/> Vídeo:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
</ul>
Áudio:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
</ul>
Subimagem:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Para habilitar os tipos estendidos, chame <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> e de definir o <br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtrar CLSID</td>
<td>CLSID_DVDNavigator</td>
</tr>
<tr class="odd">
<td>CLSID da página de propriedades</td>
<td>Nenhuma página de propriedades.</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérito</a></td>
<td>Merit_do_not_use</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 




