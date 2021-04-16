---
description: Atalhos para páginas de referência de DVD do C++
ms.assetid: b37337b7-b3be-4f49-b350-df5e3c88e3cf
title: Atalhos para páginas de referência de DVD do C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7caed2aea59e41cf666c6ed63d220f986a8e36
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500508"
---
# <a name="shortcuts-to-c-dvd-reference-pages"></a>Atalhos para páginas de referência de DVD do C++

As interfaces a seguir são aquelas normalmente usadas ao escrever um aplicativo de DVD em C++.



| Interface                                    | Finalidade                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) | Controla a exibição de legendas ocultas.                                                              |
| [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)                   | Usado em técnicas de sincronização de comando avançado para controlar um objeto de comando.                 |
| [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)         | Emite comandos para o filtro de [navegador de DVD](dvd-navigator-filter.md) (os métodos "set").     |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) | Cria o grafo de filtro de DVD.                                                                    |
| [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)               | Consulta o navegador de DVD para informações de estado e informações sobre o disco (os métodos "Get"). |
| [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate)               | Salva informações, como indicadores, em disco.                                                   |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)   | Controla a "depuração de quadro" se o decodificador oferecer suporte a ele.                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



