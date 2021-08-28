---
title: Criando grupos locais
description: Somente grupos locais podem ser criados para servidores membros e Windows 2000 Professional.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Criando o AD de Grupos Locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06410572e6e5897280b2a03c99b387dbf81b3cca
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881589"
---
# <a name="creating-local-groups"></a>Criando grupos locais

Somente grupos locais podem ser criados para servidores membros e Windows 2000 Professional.

**Para criar um grupo local para um servidor membro ou computador executando Windows 2000 Professional**

1.  A bind ao computador usando as seguintes regras:
    1.  Use uma conta com direitos suficientes para acessar esse computador.
    2.  Use o seguinte formato de cadeia de caracteres de associação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI de que ele está sendo vinculado a um computador: "WinNT:// <computer name> , &lt; computador &gt; ".

        O parâmetro " &lt; nome do computador " é o nome dos grupos de &gt; computadores a acessar.

        Na cadeia de caracteres de associação, o parâmetro " &lt; computador " instrui a &gt; ADSI de que ele está sendo vinculado a um computador. A ADSI disponibiliza esses dados para o analisador do provedor WinNT para que ele possa ignorar algumas consultas de resolução de ambiguidade para determinar a qual tipo de objeto você está se vinculando.

    3.  A bind à [**interface IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Especifique "localGroup" como a classe [**usando IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para adicionar o grupo.
    > [!Note]  
    > Se você especificar "group" como a classe , a ADSI usará "localGroup". Não especifique a classe como "globalGroup". Grupos da classe "globalGroup" não podem ser criados em servidores membros ou em um computador que executa Windows NT Workstation/Windows 2000 Professional. Se você especificar "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) criará o grupo no cache de propriedades, mas [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) não gravará o grupo no banco de dados de segurança e não retornará um erro.

     

3.  Escreva o grupo no banco de dados de segurança do computador [**usando IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 
