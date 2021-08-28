---
description: filtro de sobreposição Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: filtro de sobreposição Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b51dceb2a7f82a91fe30275cacfaad4ad78eded
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987349"
---
# <a name="overlay-mixer-2-filter"></a>filtro de sobreposição Mixer 2

o filtro de sobreposição Mixer 2 é idêntico ao filtro de [Mixer de sobreposição](overlay-mixer-filter.md) , exceto:

-   Ele dá suporte apenas a tipos de mídia com formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
-   Ele tem um mérito maior, o que permite que ele seja adicionado automaticamente a um grafo de filtro.

a sobreposição Mixer 2 é fornecida para que o filtro Graph Manager a adicione ao grafo quando ele renderiza um vídeo não MPEG-2 em DVD. a opção de usar o Mixer de sobreposição ou a sobreposição Mixer 2 é manipulada pelo componente que cria o grafo, o filtro Graph gerenciador, o construtor Graph builder ou o construtor de Graph de DVD. Da perspectiva do aplicativo, eles são o mesmo filtro, com as mesmas interfaces e funcionalidade.

a tabela a seguir contém informações específicas para a sobreposição Mixer 2. Para todos os outros dados de filtro, consulte a documentação do Mixer de sobreposição.




| Rótulo | Valor |
|--------|-------|
| Tipos de mídia de pino de entrada | Tipo de formato: Format_VIDEOINFO2 | 
| CLSID do filtro | CLSID_OverlayMixer2 | 
| <a href="merit.md">Núcleo</a> | <ul><li>MERIT_UNLIKELY</li><li>Windows Vista ou posterior: MERIT_DO_NOT_USE</li></ul> | 




 

no Windows Vista ou posterior, o mérito do filtro de sobreposição Mixer 2 é um mérito \_ \_ não \_ usado, pois os renderizadores de vídeo mais recentes (vmr-7, vmr-9 e EVR) dão suporte a formatos **VIDEOINFOHEADER2** e, portanto, não é necessário usar a Mixer de sobreposição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 



