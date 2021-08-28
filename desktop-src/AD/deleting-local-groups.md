---
title: Excluindo grupos locais
description: este tópico mostra como excluir um grupo local de um servidor membro ou computador que executa o Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Excluindo grupos locais AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe960804e083ecaf8ef12e412a43b7b8db4800f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881472"
---
# <a name="deleting-local-groups"></a>Excluindo grupos locais

este tópico mostra como excluir um grupo local de um servidor membro ou computador que executa o Windows 2000 Professional.

**Para excluir um grupo local**

1.  Associe-se ao computador usando as seguintes regras:
    1.  Use uma conta com direitos suficientes para acessar esse computador.
    2.  Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI que ele está ligando a um computador: "WinNT:// <computer name> , &lt; Computer &gt; ". O &lt; parâmetro "nome &gt; do computador" é o nome do grupo de computadores a ser acessado. Esse parâmetro instrui a ADSI de que está ligando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar a qual tipo de objeto você está ligando.
    3.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Especifique "Group" como a classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)para excluir o grupo.

    Você não precisa chamar [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar a alteração no contêiner. A chamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma a exclusão do grupo diretamente para o diretório.

 

 
