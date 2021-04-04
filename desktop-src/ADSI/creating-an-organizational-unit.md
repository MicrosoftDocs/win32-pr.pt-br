---
title: Criando uma unidade organizacional
description: Agora que você tem o objeto de domínio, você pode começar a criar unidades organizacionais.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Criando um ADSI de unidade organizacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915907"
---
# <a name="creating-an-organizational-unit"></a>Criando uma unidade organizacional

Agora que você tem o objeto de domínio, você pode começar a criar unidades organizacionais. A Fabrikam tem duas divisões: vendas e produção. A empresa está planejando contratar dois administradores do Windows 2000 para gerenciar cada divisão. Joe Worden, como administrador corporativo, criará duas novas unidades organizacionais no domínio fabrikam. Ao criar uma unidade organizacional, Joe pode agrupar vários objetos e permitir que outra pessoa gerencie esses objetos. O exemplo de código a seguir cria a UO (unidade organizacional Sales).


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



O método [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) aceita o nome da classe e o nome do novo objeto. Neste ponto, o objeto não está confirmado em Active Directory. Você, no entanto, terá uma referência de objeto ADSI/COM no cliente. Com esse objeto ADSI, você pode definir ou modificar atributos usando o método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) . O método **IADs. put** aceita o nome do atributo e o valor do atributo. Ainda assim, nada é confirmado no diretório; Tudo é armazenado em cache no cliente. Quando você chama o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , as alterações, nesse caso, a criação de objetos e a modificação de atributos, são confirmadas no diretório. Essas alterações são transacionadas, o que significa que você verá o novo objeto com todos os atributos que você definiu ou nenhum objeto.

Você também pode aninhar unidades organizacionais. O exemplo de código a seguir pressupõe que a divisão de vendas esteja dividida mais nas regiões leste e oeste.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Isso também se aplica à região oeste.

Para associar diretamente à região leste da organização Sales, especifique o nome distinto.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Se você já tiver associado ao objeto pai (vendas), poderá associar ao objeto filho (leste) do objeto pai usando o nome relativo do objeto filho.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Para garantir que os objetos tenham sido criados, use o snap-in Active Directory usuários e computadores do MMC para exibir as novas unidades organizacionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Movendo usuários existentes para a unidade organizacional](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




