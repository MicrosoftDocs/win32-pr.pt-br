---
title: Arquivos compostos assíncronos
description: Os arquivos compostos assíncronos, a implementação fornecida pelo sistema do armazenamento assíncrono, permitem o download eficiente de arquivos compostos da Internet em geral e a Web em particular.
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04de2162b50283b12bc8deed6ec908d92e7584d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366491"
---
# <a name="asynchronous-compound-files"></a>Arquivos compostos assíncronos

Os arquivos compostos assíncronos, a implementação fornecida pelo sistema do armazenamento assíncrono, permitem o download eficiente de arquivos compostos da Internet em geral e a Web em particular. A arquitetura básica de arquivos compostos assíncronos é mostrada no diagrama a seguir.

![arquitetura básica de arquivos compostos assíncronos](images/asy-stor.png)

A implementação de arquivos compostos assíncronos pode funcionar com novos tipos de moniker assíncronos que entendem protocolos de Internet e podem ser associados a um objeto identificado por uma URL. Tal moniker retornaria um ponteiro de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ou [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) assíncrono da chamada do cliente para [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage).

Os arquivos compostos em geral são implementados na parte superior de um objeto de matriz de bytes, uma abstração de um arquivo que representa os dados de um objeto como uma matriz de bytes simples. O objeto da matriz de bytes expõe sua funcionalidade por meio da interface [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) . Se uma matriz de bytes der suporte ao armazenamento assíncrono não bloqueado, ela retornará E \_ pendente para a implementação de arquivo composto que, por sua vez, propaga o erro de volta para o chamador.

Para manter o controle dos dados disponíveis durante um download, uma matriz de bytes que dá suporte ao armazenamento assíncrono expõe a interface [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) em um objeto wrapper fornecido pelo sistema especificamente para essa finalidade. O código de download fornecido por um moniker assíncrono chama essa interface para preencher a matriz de bytes de forma assíncrona, pois os dados estão disponíveis. O objeto wrapper também expõe uma interface **ILockBytes** , que a implementação dos arquivos compostos assíncronos usa para ler e gravar dados de e para a matriz.

O armazenamento assíncrono e os objetos de fluxo fornecem um ponto de conexão para a interface [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) , que é implementada pelo código de download do moniker assíncrono. A implementação de arquivos compostos assíncronos chama **IProgressNotify** para fornecer ao Downloader informações sobre o status da operação de download.

 

 