---
description: Exemplo de DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Exemplo de DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fc51cc45ad879ccbc5ccd232b782e4b9f5511071d8d2492c135efcb322969c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079196"
---
# <a name="dmoenum-sample"></a>Exemplo de DMOEnum

## <a name="description"></a>Descrição

Esse aplicativo de exemplo enumera todos os DMOS ( [objetos de mídia do DirectX](directx-media-objects.md) ) registrados no sistema do usuário e exibe informações sobre eles.

O exemplo usa a função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) e a interface [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) para enumerar o DMOs. ele usa a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) e outras interfaces DMO para recuperar informações sobre cada DMO.

## <a name="usage"></a>Uso

Quando o aplicativo é iniciado, ele enumera todos os DMOs instalados. se você selecionar uma categoria de DMO específica, o aplicativo exibirá apenas o DMOs nessa categoria. para exibir informações sobre um DMO, selecione o DMO na lista. o aplicativo exibe o número de fluxos, os tipos de mídia preferenciais, o servidor DLL para esse DMO e outras informações sobre a DMO. Para incluir ou excluir DMOs com chave, alterne a caixa de seleção **incluir DMOs com chave?** .

## <a name="downloading-the-sample"></a>Baixando o exemplo

para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

este exemplo é instalado no seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ \\ multimídia \\ DirectShow \\ Misc \\ DMOEnum.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



