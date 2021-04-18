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
# <a name="error-and-exception-handling-acf-attributes"></a>Atributos ACF de tratamento de erro e exceção

Use os atributos a seguir para tratamento de erros.



| Atributo                                                                | Uso                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| status de falha de [**\_ status de comunicação**](comm-status.md)[**\_**](fault-status.md) | Permita que o aplicativo cliente manipule exceções normalmente, fazendo com que os erros de comunicação e de servidor sejam retornados ao cliente como valores de parâmetro. O aplicativo cliente pode então chamar a função de tempo de execução RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) para retransmitir uma mensagem de erro ao usuário. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Importando arquivos e bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> </dl>

 

 