---
description: Serviços COM+ sem componentes
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Serviços COM+ sem componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089317"
---
# <a name="com-services-without-components"></a>Serviços COM+ sem componentes

Com o COM+ 1,5, você pode usar os serviços fornecidos pelo COM+ sem a necessidade de criar um componente para conter os métodos que chamam esses serviços. Isso beneficia muito os desenvolvedores que normalmente não usam componentes, mas desejam usar serviços COM+, como transações ou o controlador COM+. Usando serviços COM+ sem componentes, os desenvolvedores podem evitar a sobrecarga de criar um componente que é usado para acessar apenas os serviços COM+ de que precisam.

Por exemplo, ambientes de script tradicionalmente têm sido os maiores consumidores de serviços COM+, mas nunca podiam usar esses serviços com eficiência, pois os serviços precisavam ser agrupados em um componente COM+. Esse requisito de agrupamento aumentou os custos de desempenho devido à maior comunicação e duplicação de dados necessários para que o ambiente de script interaja com o componente. Usando serviços sem componentes, esses custos são minimizados.

Os tópicos descritos na tabela a seguir fornecem informações em segundo plano e tarefas sobre como usar serviços COM+ sem componentes. Esse recurso destina-se a desenvolvedores de Visual C++ avançados que se preocupam com o desempenho.



| Tópico                                                                                                 | Descrição                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Conceitos dos serviços COM+ sem componentes](com--services-without-components-concepts.md)<br/> | Fornece uma visão geral do uso dos serviços COM+ sem componentes.<br/>                     |
| [Serviços COM+ sem tarefas de componentes](com--services-without-components-tasks.md)<br/>       | Fornece instruções para usar o COM+ para criar e usar serviços sem componentes.<br/> |



 

 

 




