---
description: Cada definição de objeto MIB contém uma cláusula de acesso (SNMPv1) ou MAX-ACCESS (SNMPv2C) que define os direitos de acesso ao objeto.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Cláusulas ACCESS e MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810627"
---
# <a name="access-and-max-access-clauses"></a>Cláusulas ACCESS e MAX-ACCESS

Cada definição de objeto MIB contém uma cláusula de acesso (SNMPv1) ou MAX-ACCESS (SNMPv2C) que define os direitos de acesso ao objeto.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

A tabela a seguir lista o mapeamento da cláusula de acesso SNMPv1.



| Cláusula de acesso MIB | Qualificador CIM       |
|-------------------|---------------------|
| somente leitura         | **Ler**            |
| leitura/gravação        | **Leitura**, **gravação** |
| somente gravação        | **Gravar**           |
| Não acessível    | **Não \_ acessível** |



 

A tabela a seguir lista o mapeamento da cláusula de acesso MAX do SNMPv2C.



| MIB-cláusula de acesso     | Qualificador CIM       |
|-----------------------|---------------------|
| somente leitura             | **Ler**            |
| leitura/gravação            | **Leitura**, **gravação** |
| ler-criar           | **Ler**            |
| acessível para notificação | **Não \_ acessível** |
| Não acessível        | **Não \_ acessível** |



 

Quando um objeto MIB é mapeado para não acessível e não é uma propriedade com chave da classe, não há nenhum mapeamento do objeto MIB em si.

 

 



