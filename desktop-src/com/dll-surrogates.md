---
title: Substitutos de DLL
description: Substitutos de DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808efe4a431a703282a705000d2fe18f6b4cfcde121d95c39fe65541b0260503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993246"
---
# <a name="dll-surrogates"></a>Substitutos de DLL

O COM possibilita criar servidores DLL que podem ser carregados em um processo EXE substituto. Isso combina a facilidade de escrever servidores DLL com os benefícios da implementação executável. Ferramentas de desenvolvimento como Microsoft Visual Studio facilitam a escrita de servidores DLL, mas um servidor DLL em si tem limites. Executar o servidor DLL em um processo substituto oferece vários benefícios possíveis:

-   Isolamento de falha e a capacidade de serviço de vários clientes simultaneamente.
-   Em um ambiente distribuído, uma implementação de servidor DLL pode ser usada para serviços de clientes remotos.
-   Ele pode permitir que os clientes ajudem a se proteger contra código de servidor não seguro, permitindo que eles acessem os serviços que o servidor DLL fornece.
-   Executar um servidor DLL em um substituto fornece a DLL com a segurança do substituto.

O COM fornece um processo substituto padrão ou você pode escrever um substituto personalizado se tiver necessidades especiais.

Os tópicos a seguir fornecem mais informações sobre substitutos de DLL:

-   [Requisitos do servidor DLL](dll-server-requirements.md)
-   [Usando o substituto System-Supplied usuário](using-the-system-supplied-surrogate.md)
-   [Escrevendo um substituto personalizado](writing-a-custom-surrogate.md)

 

 




