---
title: Convertendo formatos de nome de conta de domínio
description: As funções do Microsoft Win32 para trabalhar com o SCM (gerenciador de controle de serviço) em um servidor host usam \ 0034; nome \\ de usuário do domínio \ 0034; formato para contas de serviço.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aaa1b3664cc0ad372f82b498153862e69013fb1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881602"
---
# <a name="converting-domain-account-name-formats"></a>Convertendo formatos de nome de conta de domínio

As funções do Microsoft Win32 para trabalhar com o SCM (gerenciador de controle de serviço) em um servidor host usam o formato " nome de usuário de domínio " para &lt; &gt; \\ &lt; contas de &gt; serviço. Por exemplo, se você chamar a função [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para recuperar a conta de usuário na qual o serviço é executado, a função retornará o nome no formato "Fabrikam \\ jeffsmith". Para se vincular à conta de usuário no diretório, por exemplo, para alterar a senha da conta, é necessário o nome diferenciado da conta, que tem o formato "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".

Para converter entre os vários formatos de nome, use a função [**TranslateName,**](/windows/desktop/api/secext/nf-secext-translatenamea) que pode converter um nome em outros formatos, como um NOME UPN.

 

 
