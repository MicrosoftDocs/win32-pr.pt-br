---
description: Objetos de streaming multimídia
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Objetos de streaming multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfefd7d16c832dc168204df771ff8f925bec3f1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471942"
---
# <a name="multimedia-streaming-objects"></a>Objetos de streaming multimídia

> [!Note]  
> Essa API está preterida. Novos aplicativos não devem usá-lo.

 

A tabela a seguir descreve os objetos de streaming de multimídia.




| CLSID | Descrição | Interfaces com suporte | 
|-------|-------------|----------------------|
| CLSID_AMMediaTypeStream | pode criar amostras de mídia para qualquer tipo de dados com suporte DirectShow | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li></ul> | 
| CLSID_AMAudioData | Implementação do objeto de contêiner <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> Audio. | <ul><li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></li></ul> | 
| CLSID_AMDirectDrawStream | o fluxo de mídia do DirectDraw que pode ser adicionado a um fluxo de multimídia DirectShow. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li></ul> | 
| CLSID_AMMultiMediaStream | DirectShow implementação do fluxo de multimídia. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></li></ul> | 
| CLSID_MediaStreamFilter | Fornece a funcionalidade de streaming de multimídia para o objeto CLSID_AMMultiMediaStream por meio da interface <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> . | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li></ul> | 
| N/D | Exemplos criados pelo objeto CLSID_AMMediaTypeStream. | <ul><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li></ul> | 
| N/D | Exemplos criados pelo fluxo do DirectDraw. | <ul><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li><li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li></ul> | 




 

 

 



