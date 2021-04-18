---
title: Substitutos de DLL
description: Substitutos de DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814420"
---
# <a name="dll-surrogates"></a>Substitutos de DLL

COM torna possível criar servidores DLL que podem ser carregados em um processo EXE substituto. Isso combina a facilidade de escrever servidores DLL com os benefícios da implementação executável. Ferramentas de desenvolvimento como Microsoft Visual Studio facilitam a gravação de servidores DLL, mas um servidor DLL em si tem limites. A execução do servidor DLL em um processo substituto oferece vários benefícios possíveis:

-   Isolamento de falhas e a capacidade de atender vários clientes simultaneamente.
-   Em um ambiente distribuído, uma implementação de servidor DLL pode ser usada para atender a clientes remotos.
-   Ele pode permitir que os clientes se protejam contra código de servidor não confiável, permitindo que eles acessem os serviços que o servidor DLL fornece.
-   A execução de um servidor DLL em um substituto fornece a DLL com a segurança do substituto.

O COM fornece um processo substituto padrão, ou você pode gravar um substituto personalizado se tiver necessidades especiais.

Os tópicos a seguir fornecem mais informações sobre os substitutos de DLL:

-   [Requisitos do servidor DLL](dll-server-requirements.md)
-   [Usando o System-Supplied substituto](using-the-system-supplied-surrogate.md)
-   [Gravando um substituto personalizado](writing-a-custom-surrogate.md)

 

 




