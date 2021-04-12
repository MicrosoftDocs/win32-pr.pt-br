---
description: O COM+ oferece aos desenvolvedores mais controle sobre seus aplicativos, permitindo níveis de isolamento de transação configuráveis.
ms.assetid: a59e262c-41f2-4c80-a04c-50a39af8b009
title: Configurando níveis de isolamento da transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d789b9eaed6dfdd2f2419c7eae391d628e75b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456958"
---
# <a name="configuring-transaction-isolation-levels"></a>Configurando níveis de isolamento da transação

O COM+ oferece aos desenvolvedores mais controle sobre seus aplicativos, permitindo níveis de isolamento de transação configuráveis. As versões do COM+ anteriores ao COM+ 1,5 sempre usaram o nível mais alto de isolamento para transações. Embora esse nível garanta que a integridade dos dados seja sempre preservada, ela pode levar a problemas de desempenho, como tempos limite, quando muitas transações precisam ser executadas em um banco de dados grande. Com os níveis de isolamento configuráveis, os desenvolvedores experientes podem aumentar a simultaneidade para melhorar o desempenho e a escalabilidade.

O COM+ fornece os seguintes níveis de isolamento de transação.



| Nível            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serializado       | Os dados lidos por uma transação atual não podem ser alterados por outra transação até que a transação atual seja concluída. Nenhum dado novo pode ser inserido que afetaria a transação atual. Esse é o nível de isolamento mais seguro e é o padrão.                                                                                                                                                                                                                                                                                                                                                    |
| Leitura repetida  | Os dados lidos por uma transação atual não podem ser alterados por outra transação até que a transação atual seja concluída. Qualquer tipo de dados novos pode ser inserido durante uma transação.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Leitura confirmada   | Uma transação não pode ler dados que estão sendo modificados por outra transação que não foi confirmada. Esse é o nível de isolamento padrão em Microsoft SQL Server.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Leitura não confirmada | Uma transação pode ler qualquer dado, mesmo que esteja sendo modificada por outra transação. Esse é o nível de isolamento menos seguro, mas permite a simultaneidade mais alta.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Qualquer              | Há suporte para qualquer nível de isolamento. Essa configuração é usada com mais frequência pelos componentes downstream para evitar conflitos. Essa configuração é útil porque qualquer componente downstream deve ser configurado com um nível de isolamento igual ou menor que o nível de isolamento de seu componente upstream imediato. Portanto, um componente downstream que tem seu nível de isolamento configurado como sempre usa o mesmo nível de isolamento que seu componente upstream imediato usa. Se o objeto raiz em uma transação tiver seu nível de isolamento configurado como qualquer, seu nível de isolamento se tornará serializado. |



 

> [!Note]  
> Se um componente downstream estiver configurado com um nível de isolamento mais alto que um componente upstream e tentar se inscrever em uma transação, ocorrerá um erro e a transação será anulada.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurar o nível de isolamento da transação](setting-the-transaction-isolation-level.md)
</dt> </dl>

 

 



