---
description: A parte mais problemática de escrever componentes é lidar com possíveis erros.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Tratamento de erros no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089693"
---
# <a name="handling-errors-in-com"></a>Tratamento de erros no COM+

A parte mais problemática de escrever componentes é lidar com possíveis erros. Tentar determinar o que pode dar errado e o que fazer sobre ele pode ser desafiador nas melhores condições. Erros comuns que seu componente pode verificar e identificadores são conexões de rede com falha, erros de segurança e falhas associadas a objetos inacessíveis.

Além disso, você pode desenvolver seus próprios códigos de erro para relatar erros específicos da interface, como quando uma regra de negócios foi violada.

Ao manter o modelo de programação COM+, um objeto pode (e geralmente faz) chamar métodos de interface em outros objetos para executar o trabalho. Como os programadores podem escrever componentes em linguagens de programação diferentes, o COM+ requer que todos os mecanismos de tratamento de erros sejam neutros à linguagem, por exemplo: HRESULTs e coleções [**errorInfo**](errorinfo.md) .

Esta seção inclui tópicos, descritos na tabela a seguir, que discutem técnicas para lidar com erros em aplicativos COM+, recursos no COM+ que afetam o comportamento de falha e sugestões para diagnosticar erros COM+.



| Tópico                                                                                           | Descrição                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estratégias para lidar com erros no COM+](strategies-for-handling-errors-in-com-.md)<br/> | Lista e descreve as diretrizes básicas para lidar com erros no COM+, incluindo quando usar as coleções HRESULTs e [**errorInfo**](errorinfo.md) .<br/> |
| [Como o COM+ modifica valores de retorno](how-com--modifies-return-values.md)<br/>               | Identifica a única condição na qual o COM+ converte um HRESULT padrão em um código de erro COM+ antes de passá-lo de volta para o chamador.<br/>             |
| [Política de FailFast e isolamento de falhas](fault-isolation-and-failfast-policy.md)<br/>       | Mostra como o isolamento de falhas e a política de FailFast afetam o comportamento do COM+.<br/>                                                                          |
| [Localizando a origem de um erro](finding-the-source-of-an-error.md)<br/>                 | Descreve como você pode diagnosticar a origem e obter uma descrição dos erros do aplicativo. <br/>                                                       |
| [Interpretando códigos de erro](interpreting-error-codes.md)<br/>                             | Identifica o mecanismo predominante de tratamento de erros para Microsoft Visual C++, a linguagem Java e o Microsoft Visual Basic. <br/>                    |
| [Solução de problemas](troubleshooting.md)<br/>                                               | Fornece assistência adicional no diagnóstico de erros.<br/>                                                                                             |
| [Entrando em contato com o suporte](contacting-support.md)<br/>                                         | Identifica informações importantes de solução de problemas que você deve fornecer ao contatar o suporte.<br/>                                                     |



 

Para obter informações detalhadas sobre como lidar com erros associados a vários serviços COM+, consulte as seguintes seções:

-   [Acelerando as transações notificando o objeto raiz](speeding-transactions-by-notifying-the-root-object.md)
-   [Tratamento de erros](handling-errors-in-queued-components.md) (para componentes na fila)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Depurando aplicativos COM+](debugging-com--applications.md)
</dt> </dl>

 

 




