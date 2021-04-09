---
description: Os desenvolvedores podem estender a infraestrutura WMI desenvolvendo provedores WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Criando provedores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011833"
---
# <a name="creating-wmi-providers"></a>Criando provedores WMI

Os desenvolvedores podem estender a infraestrutura WMI desenvolvendo provedores WMI. Provedores WMI são objetos COM que implementam um conjunto especificado de interfaces e, até recentemente, foram sempre implementados em C++. Agora você pode usar linguagens gerenciadas como C# para implementar provedores WMI. A versão 3,5 do .NET Framework introduziu a estrutura de extensões do provedor WMI que torna isso possível. Para saber mais sobre como criar provedores WMI usando essa estrutura, leia o artigo criando [provedores WMI acoplados usando a extensão 2,0 do provedor de WMI.net](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> Você também pode criar um provedor usando a MI (infraestrutura de gerenciamento do Windows), a versão de próxima geração do WMI. Para obter mais informações, consulte [como implementar um provedor de mi](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

A tabela a seguir descreve o conteúdo nesta seção.



| Tópico                                                      | Descrição                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Fornecendo dados ao WMI](providing-data-to-wmi.md)         | Fornece uma visão geral das etapas envolvidas na criação de um provedor WMI.         |
| [Desenvolvendo um provedor WMI](developing-a-wmi-provider.md) | Descreve as tarefas que você deve executar ao criar vários tipos de provedores de WMI. |



 

 

 
