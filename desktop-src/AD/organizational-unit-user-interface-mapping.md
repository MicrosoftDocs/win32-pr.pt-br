---
title: Mapeamento de Interface do Usuário organizacional
description: Este tópico descreve as folhas de propriedades de objeto da UO (Unidade Organizacional) no snap-in Usuários e Computadores do Active Directory de dados.
ms.assetid: 105c0f01-55d5-4dc2-887e-5e204ba82c4c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34d4f3e268e9448e9b835a4716cfa3f379ffb3cac93c2720e3f455a66384ed32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025514"
---
# <a name="organizational-unit-user-interface-mapping"></a>Mapeamento de Interface do Usuário organizacional

Este tópico descreve as folhas de propriedades de objeto da UO (Unidade Organizacional) no snap-in Usuários e Computadores do Active Directory de dados.

## <a name="general-property-sheet"></a>Folha de propriedades geral

A tabela a seguir mostra os rótulos de interface do usuário da **folha de propriedades** Geral.



| Rótulo da interface do usuário        | Atributo em Active Directory Domain Services |
|-----------------|-----------------------------------------------|
| Descrição     | [**Descrição**](/windows/desktop/ADSchema/a-description)     |
| Street          | [**Endereço da rua**](/windows/desktop/ADSchema/a-street)       |
| City            | [**Locality-Name**](/windows/desktop/ADSchema/a-l)             |
| Estado/Província  | [**State-or-Province-Name**](/windows/desktop/ADSchema/a-st)   |
| Cep/Cep | [**Cep**](/windows/desktop/ADSchema/a-postalcode)      |
| País/Região  | [**Nome do país**](/windows/desktop/ADSchema/a-c)              |



 

## <a name="managed-by-property-sheet"></a>Folha de propriedades gerenciada por

A tabela a seguir mostra os rótulos de interface do usuário da **folha de propriedades Gerenciado** por.



| Rótulo da interface do usuário         | Atributo em Active Directory Domain Services                                                                                   |
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nome             | [**Gerenciado por**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Office           | O [**atributo Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) da conta identificada pelo **Nome**. |
| Street           | O [**atributo Street-Address**](/windows/desktop/ADSchema/a-street) da conta identificada pelo **Nome**.                                    |
| City             | O [**atributo Locality-Name**](/windows/desktop/ADSchema/a-l) da conta identificada pelo **Nome**.                                          |
| Estado/Província   | O [**atributo State-Or-Province-Name**](/windows/desktop/ADSchema/a-st) da conta identificada pelo **Nome**.                                |
| País/região   | O [**atributo Country-Name**](/windows/desktop/ADSchema/a-c) da conta identificada pelo **Nome**.                                           |
| Número de telefone | O [**atributo Número de**](/windows/desktop/ADSchema/a-telephonenumber) Telefone da conta identificada pelo **Nome**.                         |
| Número de fax       | O [**atributo Facsimile-Telephone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) da conta identificada pelo **Nome**.      |



 

 

 