---
title: Determinando as classes associadas a uma instância de objeto
description: Cada objeto no Active Directory Domain Services tem dois atributos cujos valores identificam a hierarquia de classes de objeto das quais o objeto é uma instância.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af65b5e1abf7f0bc68ae115cb409d2cdb556e08
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471492"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Determinando as classes associadas a uma instância de objeto

Cada objeto no Active Directory Domain Services tem dois atributos cujos valores identificam a hierarquia de classes de objeto das quais o objeto é uma instância.




| Atributo | Descrição | 
|-----------|-------------|
| <strong>structuralObjectClass</strong> | Identifica as classes estruturais e abstratas das quais o objeto é uma instância. Por exemplo, os valores de um objeto de usuário podem ser:<ul><li><strong>início</strong></li><li><strong>person</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 
| <strong>Objectclass</strong> | Identifica as classes incluídas em <strong>structuralObjectClass</strong>, além de todas as classes auxiliares anexadas dinamicamente. Por exemplo, se uma classe auxiliar de "veículo" estiver anexada a um objeto de usuário, os valores poderão ser:<ul><li><strong>início</strong></li><li><strong>Veículo</strong></li><li><strong>person</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 




 

Esteja ciente de que nenhum desses atributos inclui classes auxiliares vinculadas estaticamente às classes de objeto das quais o objeto é uma instância. Por exemplo, a classe auxiliar **securityPrincipal** está  vinculada estaticamente à classe de usuário porque está incluída nos valores **systemClass do** objeto user **classSchema;** ele não está incluído nos atributos **objectClass** ou **structuralObjectClass** de instâncias da classe de usuário.

 

 




