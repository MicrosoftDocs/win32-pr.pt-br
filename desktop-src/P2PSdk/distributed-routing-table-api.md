---
description: A API de DRT (tabela de roteamento distribuído) permite que os aplicativos publiquem e resolvam chaves numéricas em uma rede de mesmo nível.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: API de Tabela de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adabac4e2e885a7ac635daf5de2dfbacc94dafd4972a6b35f1f4649c3428e92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011604"
---
# <a name="distributed-routing-table-api"></a>API de Tabela de roteamento distribuído

A API de DRT (tabela de roteamento distribuído) permite que os aplicativos publiquem e resolvam chaves numéricas em uma rede de mesmo nível.

Um aplicativo que utiliza o DRT pode realizar o seguinte:

-   Crie tabelas de roteamento distribuídas específicas do aplicativo.
-   Registre chaves e associe essas chaves a dados de aplicativos e endereços IP.
-   Pesquise por chaves e recupere os endereços IP e os dados de aplicativo associados a eles. Essa funcionalidade pode ser usada para construir tabelas de hash distribuídas (DHTs), sistemas de resolução de nomes sem servidor e redes de malha de sobreposição de várias topologias.

> [!Note]  
> Os administradores e usuários de aplicativos habilitados para DRT devem fazer com que os usuários finais de seus aplicativos reconheçam as informações que estão sendo publicadas. Os servidores da Microsoft não são empregados por essa tecnologia e as informações não são enviadas à Microsoft.

 

A documentação fornecida para essa API é dividida em três seções.



| Seção                                                                                | Descrição                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Sobre tabelas de roteamento distribuído](about-distributed-routing-tables.md)               | Informações detalhando o ciclo de vida e as alterações de estado da API DRT.<br/>                                    |
| [Usando o API de Tabela de roteamento distribuído](using-the-distributed-routing-table-api.md) | Informações detalhando o uso geral da API DRT.<br/>                                                   |
| [Referência de API de Tabela de roteamento distribuído](distributed-routing-table-api-reference.md) | Informações detalhando as funções, as estruturas de dados e as constantes enumeradas que compõem a API DRT.<br/> |



 

 

 




