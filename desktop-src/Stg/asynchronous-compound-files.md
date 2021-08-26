---
title: Arquivos compostos assíncronos
description: Arquivos Compostos Assíncronos, a implementação fornecida pelo sistema do armazenamento assíncrono, permite o download eficiente de arquivos compostos da Internet em geral e da Web em particular.
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15404f33041fb52f5baa5230f69434ce390b985c41374235c1f3979ef6c2f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034977"
---
# <a name="asynchronous-compound-files"></a>Arquivos compostos assíncronos

Arquivos Compostos Assíncronos, a implementação fornecida pelo sistema do armazenamento assíncrono, permite o download eficiente de arquivos compostos da Internet em geral e da Web em particular. A arquitetura básica dos Arquivos Compostos Assíncronos é mostrada no diagrama a seguir.

![arquitetura básica de arquivos compostos assíncronos](images/asy-stor.png)

A implementação de Arquivos Compostos Assíncronos pode funcionar com novos tipos de moniker assíncronos que entendem os protocolos da Internet e podem se vincular a um objeto identificado por uma URL. Esse moniker retornaria um ponteiro [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ou [**IStorage assíncrono**](/windows/desktop/api/Objidl/nn-objidl-istorage) da chamada do cliente para [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage).

Arquivos Compostos em geral são implementados sobre um objeto de matriz de byte, uma abstração de um arquivo que representa os dados de um objeto como uma matriz de byte simples. O objeto de matriz de byte expõe sua funcionalidade por meio da interface [**ILockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Se uma matriz de byte dá suporte ao armazenamento assíncrono não bloqueado, ela retorna E PENDING para a implementação de arquivo composto, que, por sua vez, propaga o erro de volta para o \_ chamador.

Para manter o controle dos dados disponíveis durante um download, uma matriz de byte que dá suporte ao armazenamento assíncrono expõe a interface [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) em um objeto wrapper fornecido pelo sistema especificamente para essa finalidade. O código de download fornecido por um moniker assíncrono chama essa interface para preencher a matriz de byte de forma assíncrona, pois os dados estão disponíveis. O objeto wrapper também expõe uma interface **ILockBytes,** que a implementação de Arquivos Compostos Assíncronos usa para ler e gravar dados de e para a matriz.

Os objetos de armazenamento e fluxo assíncronos fornecem um ponto de conexão para a interface [**IProgressNotify,**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) que é implementada pelo código de download do moniker assíncrono. A implementação de Arquivos Compostos Assíncronos chama **IProgressNotify** para fornecer ao download informações sobre o status da operação de download.

 

 