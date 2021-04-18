---
title: Atributos ACF de tratamento de erro e exceção
description: Use os atributos a seguir para tratamento de erros.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- MIDL de ACF, atributos, erro e tratamento de exceção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105785438"
---
# <a name="error-and-exception-handling-acf-attributes"></a><span data-ttu-id="9b2e9-104">Atributos ACF de tratamento de erro e exceção</span><span class="sxs-lookup"><span data-stu-id="9b2e9-104">Error and Exception Handling ACF Attributes</span></span>

<span data-ttu-id="9b2e9-105">Use os atributos a seguir para tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="9b2e9-105">Use the following attributes for error handling.</span></span>



| <span data-ttu-id="9b2e9-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="9b2e9-106">Attribute</span></span>                                                                | <span data-ttu-id="9b2e9-107">Uso</span><span class="sxs-lookup"><span data-stu-id="9b2e9-107">Usage</span></span>                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b2e9-108">status de falha de [**\_ status de comunicação**](comm-status.md)[**\_**](fault-status.md)</span><span class="sxs-lookup"><span data-stu-id="9b2e9-108">[**comm\_status**](comm-status.md)[**fault\_status**](fault-status.md)</span></span> | <span data-ttu-id="9b2e9-109">Permita que o aplicativo cliente manipule exceções normalmente, fazendo com que os erros de comunicação e de servidor sejam retornados ao cliente como valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9b2e9-109">Let your client application handle exceptions gracefully by causing communication and server errors to be returned to the client as parameter values.</span></span> <span data-ttu-id="9b2e9-110">O aplicativo cliente pode então chamar a função de tempo de execução RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) para retransmitir uma mensagem de erro ao usuário.</span><span class="sxs-lookup"><span data-stu-id="9b2e9-110">The client application can then call the RPC run-time function [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) to relay an error message to the user.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9b2e9-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b2e9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b2e9-112">Importando arquivos e bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="9b2e9-112">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> </dl>

 

 