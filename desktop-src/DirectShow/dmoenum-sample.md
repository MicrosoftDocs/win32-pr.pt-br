---
description: Exemplo de DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Exemplo de DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163858"
---
# <a name="dmoenum-sample"></a>Exemplo de DMOEnum

## <a name="description"></a>Descrição

Esse aplicativo de exemplo enumera todos os DMOS ( [objetos de mídia do DirectX](directx-media-objects.md) ) registrados no sistema do usuário e exibe informações sobre eles.

O exemplo usa a função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) e a interface [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) para enumerar o DMOs. Ele usa a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) e outras interfaces DMO para recuperar informações sobre cada DMO.

## <a name="usage"></a>Uso

Quando o aplicativo é iniciado, ele enumera todos os DMOs instalados. Se você selecionar uma categoria de DMO específica, o aplicativo exibirá apenas o DMOs nessa categoria. Para exibir informações sobre um DMO, selecione o DMO na lista. O aplicativo exibe o número de fluxos, os tipos de mídia preferenciais, o servidor DLL para esse DMO e outras informações sobre o DMO. Para incluir ou excluir DMOs com chave, alterne a caixa de seleção **incluir DMOs com chave?** .

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ \\ multimídia \\ DirectShow \\ misc \\ DMOEnum.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



