---
description: As exceções podem ser iniciadas pelo hardware ou software e podem ocorrer no modo kernel, bem como no código do modo de usuário. A manipulação de exceção estruturada fornece um mecanismo único para o tratamento de exceções de modo kernel e de modo de usuário.
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: Tratamento de exceção (tratamento de erro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253776619100095ae1ba9c92fa2caa373bc950bdf6725c6ef5d0239520320bd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260866"
---
# <a name="exception-handling-error-handling"></a>Tratamento de exceção (tratamento de erro)

As exceções podem ser iniciadas pelo hardware ou software e podem ocorrer no modo kernel, bem como no código do modo de usuário. A manipulação de exceção estruturada fornece um mecanismo único para o tratamento de exceções de modo kernel e de modo de usuário.

A execução de determinadas sequências de instrução pode resultar em exceções iniciadas pelo hardware. Por exemplo, uma violação de acesso é gerada pelo hardware quando um processo tenta ler ou gravar em um endereço virtual ao qual não tem o acesso apropriado.

Eventos que exigem tratamento de exceção também podem ocorrer durante a execução de uma rotina de software (por exemplo, quando um valor de parâmetro inválido é especificado). Quando isso acontece, um thread pode iniciar uma exceção explicitamente chamando a função [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) . Essa função permite que o thread de chamada Especifique informações que descrevem a exceção.

Uma exceção pode ser continuável ou não continuável. Uma exceção não continuável surge quando o evento não é continuável no hardware ou se a continuação não faz sentido. Uma exceção não continuável não encerra o aplicativo. Portanto, um aplicativo pode ser capaz de capturar a exceção e executar. No entanto, uma exceção não continuável normalmente surge como resultado de uma pilha corrompida ou outro problema sério, dificultando a recuperação da exceção.

 

 
