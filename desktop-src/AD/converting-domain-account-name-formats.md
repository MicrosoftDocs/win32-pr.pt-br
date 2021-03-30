---
title: Convertendo formatos de nome de conta de domínio
description: As funções do Microsoft Win32 para trabalhar com o SCM (Gerenciador de controle de serviço) em um servidor host usam o \ 0034; domínio \\ nome de usuário \ 0034; formato para contas de serviço.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640426"
---
# <a name="converting-domain-account-name-formats"></a>Convertendo formatos de nome de conta de domínio

As funções do Microsoft Win32 para trabalhar com o SCM (Gerenciador de controle de serviço) em um servidor host usam o <domain> \\ <username> formato "" para contas de serviço. Por exemplo, se você chamar a função [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para recuperar a conta de usuário sob a qual seu serviço é executado, a função retornará o nome no formato "fabrikam \\ jeffsmith". Para se associar à conta de usuário no diretório, por exemplo, para alterar a senha da conta, é necessário o nome distinto da conta, que tem o formato "CN = Jeff Smith, CN = Users, DC = Fabrikam, DC = COM".

Para converter entre os vários formatos de nome, use a função [**transtardianame**](/windows/desktop/api/secext/nf-secext-translatenamea) , que pode converter um nome para outros formatos, como um UPN (nome principal do usuário).

 

 