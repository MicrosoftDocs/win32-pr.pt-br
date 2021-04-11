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
# <a name="business-rules"></a><span data-ttu-id="ebf84-103">Regras de negócio</span><span class="sxs-lookup"><span data-stu-id="ebf84-103">Business Rules</span></span>

<span data-ttu-id="ebf84-104">Uma regra de negócio permite que um aplicativo use lógica em tempo de execução para qualificar as permissões concedidas ao cliente.</span><span class="sxs-lookup"><span data-stu-id="ebf84-104">A business rule allows an application to use logic at run time to qualify permissions granted to the client.</span></span>

<span data-ttu-id="ebf84-105">Uma regra de negócio é um script escrito na linguagem de programação Visual Basic Scripting Edition (VBScript) ou escrito usando o software de desenvolvimento Microsoft JScript que está associado a um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="ebf84-105">A business rule is a script written in the Visual Basic Scripting Edition (VBScript) programming language or written using the Microsoft JScript development software that is associated with an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="ebf84-106">Quando um aplicativo verifica o acesso a uma operação, o Gerenciador de autorização primeiro verifica se o cliente atual tem acesso a todas as tarefas que contêm essa operação, mas que não estão associadas às regras de negócio.</span><span class="sxs-lookup"><span data-stu-id="ebf84-106">When an application checks access for an operation, Authorization Manager first checks if the current client has access to any tasks that contain that operation but that are not associated with business rules.</span></span> <span data-ttu-id="ebf84-107">Se o acesso não for concedido dessa forma, o Gerenciador de autorização executará scripts de regra comercial associados a qualquer tarefa que contenha a operação.</span><span class="sxs-lookup"><span data-stu-id="ebf84-107">If access is not granted this way, Authorization Manager runs business-rule scripts associated with any task that contains the operation.</span></span>

<span data-ttu-id="ebf84-108">Um aplicativo passa informações para um script de regra de negócio como um par de matrizes que representam os nomes e valores dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ebf84-108">An application passes information to a business-rule script as a pair of arrays that represent the names and values of parameters.</span></span> <span data-ttu-id="ebf84-109">O script tem acesso a esses parâmetros por meio de um objeto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que é criado quando o script é executado.</span><span class="sxs-lookup"><span data-stu-id="ebf84-109">The script has access to these parameters through an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is created when the script runs.</span></span>

<span data-ttu-id="ebf84-110">Um script de regra de negócio não pode ser atribuído a uma tarefa contida por um escopo delegado.</span><span class="sxs-lookup"><span data-stu-id="ebf84-110">A business-rule script cannot be assigned to a task contained by a delegated scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebf84-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ebf84-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebf84-112">Qualificando o acesso com a lógica de negócios em C++</span><span class="sxs-lookup"><span data-stu-id="ebf84-112">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



