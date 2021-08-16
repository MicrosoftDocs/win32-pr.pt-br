---
title: Enumerando grupos locais
description: em servidores membros e computadores em execução no Windows 2000 Professional, você pode enumerar todos os grupos locais.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumerando grupos locais AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1584cf8650b3fa341e7a314e0b6f94120b28c50226f16230c53206d6e14b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191326"
---
# <a name="enumerating-local-groups"></a>Enumerando grupos locais

em servidores membros e computadores em execução no Windows 2000 Professional, você pode enumerar todos os grupos locais.

somente grupos locais podem ser criados em servidores membros e Windows 2000 Professional. No entanto, esses grupos locais podem conter:

-   Grupos universais e globais da floresta que contém o domínio ao qual o computador é membro.
-   Grupos locais de domínio do domínio desse computador.
-   Usuários de qualquer domínio na floresta.

**para enumerar os grupos locais em um servidor membro ou computador que executa o Windows 2000 Professional**

1.  Associe-se ao computador usando as seguintes regras:
    1.  Use uma conta com direitos suficientes para acessar esse computador.
    2.  Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ".

        "O <computer name> parâmetro" é o nome do grupo de computadores a ser acessado. Esse parâmetro instrui a ADSI de que está ligando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar a qual tipo de objeto você está ligando.

    3.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Defina um filtro que contenha "grupos" usando a propriedade [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) . Isso permite que você enumere o contêiner e recupere somente grupos.
3.  Enumere os objetos de grupo, usando o método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .
4.  Para cada objeto de grupo, use a interface [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup) para ler o nome e os membros do grupo.

 

 