---
description: Os desenvolvedores podem estender a infraestrutura WMI desenvolvendo provedores WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Criando provedores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cb15b911cb549e28e3536da0a9da31de8df1d6f395ede5f9c9176d21239abc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679736"
---
# <a name="creating-wmi-providers"></a>Criando provedores WMI

Os desenvolvedores podem estender a infraestrutura WMI desenvolvendo provedores WMI. Os provedores WMI são objetos COM que implementam um conjunto especificado de interfaces e, até recentemente, sempre foram implementados no C++. Agora você pode usar linguagens gerenciadas como C# para implementar provedores WMI. A versão 3.5 do .NET Framework introduziu a estrutura extensões do provedor WMI que possibilita isso. Para saber mais sobre como criar provedores WMI usando essa estrutura, leia o artigo Escrevendo provedores WMI a coupled usando [WMI.NET Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> Você também pode criar um provedor usando a MI (infraestrutura Windows gerenciamento), a versão da próxima geração do WMI. Para obter mais informações, [consulte How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

A tabela a seguir descreve o conteúdo nesta seção.



| Tópico                                                      | Descrição                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Fornecendo dados ao WMI](providing-data-to-wmi.md)         | Fornece uma visão geral das etapas envolvidas na criação de um provedor WMI.         |
| [Desenvolvendo um provedor WMI](developing-a-wmi-provider.md) | Descreve as tarefas que você deve executar ao criar vários tipos de provedores WMI. |



 

 

 
