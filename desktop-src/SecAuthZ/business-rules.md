---
description: Uma regra de negócio permite que um aplicativo use lógica em tempo de execução para qualificar as permissões concedidas ao cliente.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Regras de negócio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172318"
---
# <a name="business-rules"></a>Regras de negócio

Uma regra de negócio permite que um aplicativo use lógica em tempo de execução para qualificar as permissões concedidas ao cliente.

Uma regra de negócio é um script escrito na linguagem de programação Visual Basic Scripting Edition (VBScript) ou escrito usando o software de desenvolvimento Microsoft JScript que está associado a um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) . Quando um aplicativo verifica o acesso a uma operação, o Gerenciador de autorização primeiro verifica se o cliente atual tem acesso a todas as tarefas que contêm essa operação, mas que não estão associadas às regras de negócio. Se o acesso não for concedido dessa forma, o Gerenciador de autorização executará scripts de regra comercial associados a qualquer tarefa que contenha a operação.

Um aplicativo passa informações para um script de regra de negócio como um par de matrizes que representam os nomes e valores dos parâmetros. O script tem acesso a esses parâmetros por meio de um objeto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que é criado quando o script é executado.

Um script de regra de negócio não pode ser atribuído a uma tarefa contida por um escopo delegado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Qualificando o acesso com a lógica de negócios em C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



