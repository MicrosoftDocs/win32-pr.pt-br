---
title: Erro e tratamento de exceção atributos ACF
description: Use os atributos a seguir para tratamento de erros.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF MIDL , atributos, erro e tratamento de exceções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f780145854a463da9a983c7dccbb24b01c2eca16437bf1254f93ec34def5395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384422"
---
# <a name="error-and-exception-handling-acf-attributes"></a>Erro e tratamento de exceção atributos ACF

Use os atributos a seguir para tratamento de erros.



| Atributo                                                                | Uso                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**status de \_ falha do**](comm-status.md)[**\_ comm**](fault-status.md) | Deixe o aplicativo cliente tratar exceções normalmente, fazendo com que erros de comunicação e servidor sejam retornados ao cliente como valores de parâmetro. Em seguida, o aplicativo cliente pode chamar a função de tempo de executar [**RPC DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) para retransmitir uma mensagem de erro para o usuário. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Importando arquivos e bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> </dl>

 

 