---
description: o DirectShow classes base fornece funções auxiliares para lidar com a \_ estrutura do tipo de mídia AM \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Funções de tipo de mídia (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef47b944d5d445f57779f99cb8517a773a7efba19ae3f2133f896fcba7b86548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153154"
---
# <a name="media-type-functions"></a>Funções de tipo de mídia

o DirectShow classes base fornece funções auxiliares para lidar com a estrutura do [**\_ \_ tipo de mídia AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

A estrutura do **\_ \_ tipo de mídia am** contém um ponteiro (o membro **pbFormat** ) para outro bloco de memória, que é chamado de *bloco de formato*. Ao trabalhar com essa estrutura, portanto, você deve ter cuidado com a alocação de memória para evitar vazamentos de memória.

As seguintes funções alocam memória:

-   **CreateMediaType** aloca uma nova estrutura de **\_ \_ tipo de mídia am** e o bloco de formato.
-   **CopyMediaType** copia para uma estrutura **de \_ \_ tipo de mídia am** existente, mas aloca o bloco de formato.
-   **CreateAudioMediaType** Inicializa uma estrutura **de \_ \_ tipo de mídia am** existente e, opcionalmente, aloca o bloco de formato.

As seguintes funções liberam a memória:

-   **FreeMediaType** libera o bloco de formato.
-   O **DeleteMediaType** libera uma estrutura de **\_ \_ tipo de mídia am** , incluindo o bloco de formato.



| Função                                             | Descrição                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**CopyMediaType**](copymediatype.md)               | Copia uma estrutura de **tipo de \_ mídia \_ am** alocada para tarefa.                                                      |
| [**CreateAudioMediaType**](createaudiomediatype.md) | Inicializa uma estrutura de tipo de mídia de acordo com uma estrutura de formato Wave.                                           |
| [**CreateMediaType**](createmediatype.md)           | Aloca e Inicializa uma estrutura de **\_ \_ tipo de mídia am** de uma estrutura de **\_ \_ tipo de mídia am** existente. |
| [**DeleteMediaType**](deletemediatype.md)           | Exclui uma estrutura de **tipo de \_ mídia \_ am** alocada para tarefa.                                                     |
| [**FreeMediaType**](freemediatype.md)               | Libera uma estrutura de **\_ \_ tipo de mídia am** alocada para tarefa da memória.                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




