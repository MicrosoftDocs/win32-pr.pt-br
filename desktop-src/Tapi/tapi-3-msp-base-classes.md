---
description: Este documento descreve o design e o uso das classes base do MSP. o uso dessas classes não é necessário, mas a maioria dos desenvolvedores vai perceber que simplificam a tarefa de criar um MSP baseado em DirectShow para a TAPI 3s new MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Classes base TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34d4f9f67618c3637bfaff149773ab7b0de4b93f33c8bca8e5eb892527735e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012336"
---
# <a name="tapi-3-msp-base-classes"></a>Classes base TAPI 3 MSP

Este documento descreve o design e o uso das classes base do MSP. o uso dessas classes não é necessário, mas a maioria dos desenvolvedores vai perceber que simplificam a tarefa de criar um MSP baseado em DirectShow para o novo MSPI da TAPI 3.

O código-fonte para as classes base MSP pode ser encontrado no diretório de exemplos do SDK (Software Development Kit) da plataforma.

presume-se familiaridade com com, ATL, DirectShow e C++. O leitor também deve conhecer o material geral em [sobre o MSP (provedor de serviços de mídia)](about-the-media-service-provider-msp-.md) e na [MSPI (interface do provedor de serviços de mídia)](media-service-provider-interface-mspi-.md).

o ATL 2,1 é necessário para o Windows 2000. a partir do Windows XP, tanto o ATL 2,1 quanto o 3,0 serão compilados.

Bibliotecas de classe base MSP (disponíveis no SDK):

-   Mspbase. lib
-   Mspid. lib
-   Strmbase. lib
-   Tmuid. lib
    > [!Note]  
    > A vinculação dinâmica em vez de estática deve ser usada.

     

Arquivos de cabeçalho de classe base MSP (disponíveis no SDK):

-   Mspaddr. h
-   Mspbase. h
-   Mspcall. h
-   Msplog. h
-   Mspstrm. h
-   Mspterm. h
-   Mspthrd. h
-   Msptmac. h
-   Msptmvc. h
-   Msptrmvc. h
-   Msptrmac. h
-   Msptrmar. h
-   Msputils. h

Arquivos de origem da classe base MSP (disponível nas amostras do SDK):

-   Mspaddr. cpp
-   Mspcall. cpp
-   Msplog. cpp
-   Mspstrm. cpp
-   Mspterm. cpp
-   Mspthrd. cpp
-   Msptrmac. cpp
-   Msptrmar. cpp
-   Msptrmvc. cpp
-   Msputils. cpp

 

 



