---
title: Usando a extensão ADSI para configuração Serviços de Área de Trabalho Remota usuário
description: A administração Serviços de Área de Trabalho Remota propriedades de usuário específicas do Serviços de Área de Trabalho Remota é possível usando os métodos implementados pela extensão ADSI (Interfaces de Serviço do Active Directory), que é empacotada com a biblioteca de vínculo dinâmico Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota , usando a extensão ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe63a725531c21b64ed0ac10abdeb4f710465532ab95f7c416c88f6142f1d55e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423686"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Usando a extensão ADSI para configuração Serviços de Área de Trabalho Remota usuário

A extensão ADSI (Interfaces de Serviço) do Active Directory para Serviços de Área de Trabalho Remota configuração do usuário é uma biblioteca que é empacotada com a biblioteca de vínculo dinâmico Tsuserex.dll. A administração Serviços de Área de Trabalho Remota propriedades específicas do usuário é possível usando os métodos implementados pela extensão. Os métodos permitem a configuração das propriedades que estão disponíveis na interface de extensão para Serviços de Área de Trabalho Remota usuários.

A extensão ADSI para Serviços de Área de Trabalho Remota configuração do usuário dá suporte ao exame e à manipulação Serviços de Área de Trabalho Remota propriedades de usuário armazenadas no banco de dados do Serviço de Diretório. A extensão também dá suporte à configuração de propriedades do usuário armazenadas no Active Directory, por meio da API LDAP (Lightweight Directory Access Protocol).

O provedor implementa os seguintes métodos:

-   [**IADs::Get.**](/windows/desktop/api/iads/nf-iads-iads-get) Esse método pesquisa uma propriedade específica ou um conjunto de propriedades em uma instância da classe .
-   [**IADs::P ut.**](/windows/desktop/api/iads/nf-iads-iads-put) Esse método configura uma propriedade específica ou um conjunto de propriedades em uma instância da classe .

Consulte a [Referência da Extensão ADSI](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) para Serviços de Área de Trabalho Remota configuração do usuário para ver uma lista das propriedades Serviços de Área de Trabalho Remota usuário específicas que você pode configurar.

Para obter mais informações sobre como acessar e modificar atributos com ADSI, consulte Acessando e manipulando [dados com ADSI.](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi)

Para obter mais informações sobre como usar convenções de nomenização ADSI e cadeias de caracteres AdsPath, consulte as informações sobre provedores de serviços [ADSI individuais](/windows/desktop/ADSI/adsi-system-providers) na documentação do SDK (Software Development Kit) do [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform.

 

 