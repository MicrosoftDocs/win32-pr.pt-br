---
description: Uma regra de negócio permite que um aplicativo use a lógica em tempo de operação para qualificar as permissões concedidas ao cliente.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Regras de negócio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54260fc6c7dd56137b3065a07f0dcccf9df1c4d21add4b9e7f0cfa79b0300e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783622"
---
# <a name="business-rules"></a>Regras de negócio

Uma regra de negócio permite que um aplicativo use a lógica em tempo de operação para qualificar as permissões concedidas ao cliente.

Uma regra de negócio é um script escrito na linguagem de programação Visual Basic VBScript (Scripting Edition) ou escrito usando o software de desenvolvimento microsoft JScript associado a um objeto [**IAzTask.**](/windows/desktop/api/Azroles/nn-azroles-iaztask) Quando um aplicativo verifica o acesso de uma operação, o Gerenciador de Autorização primeiro verifica se o cliente atual tem acesso a tarefas que contêm essa operação, mas que não estão associadas a regras de negócios. Se o acesso não for concedido dessa forma, o Gerenciador de Autorização executa scripts de regra de negócios associados a qualquer tarefa que contenha a operação.

Um aplicativo passa informações para um script de regra de negócios como um par de matrizes que representam os nomes e valores dos parâmetros. O script tem acesso a esses parâmetros por meio de [**um objeto AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) criado quando o script é executado.

Um script de regra de negócios não pode ser atribuído a uma tarefa contida por um escopo delegado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Qualificando o acesso com lógica de negócios em C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



