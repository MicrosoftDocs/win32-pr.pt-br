---
title: Criando grupos locais
description: Somente grupos locais podem ser criados para servidores membros e para o Windows 2000 Professional.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Criando AD de grupos locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293894"
---
# <a name="creating-local-groups"></a>Criando grupos locais

Somente grupos locais podem ser criados para servidores membros e para o Windows 2000 Professional.

**Para criar um grupo local para um servidor membro ou computador que executa o Windows 2000 Professional**

1.  Associe-se ao computador usando as seguintes regras:
    1.  Use uma conta com direitos suficientes para acessar esse computador.
    2.  Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ".

        O &lt; parâmetro "nome &gt; do computador" é o nome dos grupos de computadores a serem acessados.

        Na cadeia de caracteres de associação, &lt; o &gt; parâmetro "computador" INSTRUI a ADSI que ela está vinculando a um computador. A ADSI torna esses dados disponíveis para o analisador do provedor de WinNT para que ele possa ignorar algumas consultas de resolução de ambiguidades para determinar a qual tipo de objeto você está associando.

    3.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Especifique "local" como a classe usando [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para adicionar o grupo.
    > [!Note]  
    > Se você especificar "Group" como a classe, a ADSI usará "local". Não especifique a classe como "global". Os grupos de classe "global Group" não podem ser criados em servidores membros ou em um computador que esteja executando o Windows NT Workstation/Windows 2000 Professional. Se você especificar "global Group", [**IADsContainer. Create criará**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) o grupo no cache de propriedades, mas [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) não gravará o grupo no banco de dados de segurança e não retornará um erro.

     

3.  Grave o grupo no banco de dados de segurança do computador usando [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 