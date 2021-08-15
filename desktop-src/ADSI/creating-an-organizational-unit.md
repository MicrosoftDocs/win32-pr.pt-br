---
title: Criando uma unidade organizacional
description: Agora que você tem o objeto de domínio, pode começar a criar unidades organizacionais.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Criando um ADSI de Unidade Organizacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf2db91c02836e2425cd25e72afe6e57ff6619948372a20d03079d65eee5c882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961985"
---
# <a name="creating-an-organizational-unit"></a>Criando uma unidade organizacional

Agora que você tem o objeto de domínio, pode começar a criar unidades organizacionais. A Fabrikam tem duas divisões: Vendas e Produção. A empresa planeja contratar dois administradores Windows 2000 para gerenciar cada divisão. Joe Worden, como administrador corporativo, criará duas novas unidades organizacionais no domínio fabrikam. Ao criar uma unidade organizacional, Joe pode agrupar vários objetos e permitir que outra pessoa gerencie esses objetos. O exemplo de código a seguir cria a UO (Unidade Organizacional de Vendas).


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



O [**método IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) aceita o nome da classe e o nome do novo objeto. Neste ponto, o objeto não está confirmado no Active Directory. No entanto, você terá uma referência de objeto ADSI/COM no cliente. Com esse objeto ADSI, você pode definir ou modificar atributos usando o [**método IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put) O **método IADs.Put** aceita o nome do atributo e o valor do atributo. Ainda assim, nada está comprometido com o diretório; tudo é armazenado em cache no cliente. Quando você chama o [**método IADs.SetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) as alterações, nesse caso, a criação de objeto e a modificação de atributo, são comprometidas no diretório. Essas alterações são transacionados, o que significa que você verá o novo objeto com todos os atributos definidos ou nenhum objeto.

Você também pode aninhar unidades organizacionais. O exemplo de código a seguir supõe que a divisão Vendas seja dividida ainda mais nas regiões Leste e Oeste.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Isso também se aplica à região Oeste.

Para se vincular diretamente à região Leste na organização Vendas, especifique o nome diferenciado.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Se você já tiver se vinculado ao objeto pai (Vendas), poderá se vincular ao objeto filho (Leste) do objeto pai usando o nome relativo do objeto filho.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Para garantir que os objetos foram criados, use o snap-in Usuários e Computadores do Active Directory MMC para exibir as novas unidades organizacionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Movendo usuários existentes para a unidade organizacional](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




