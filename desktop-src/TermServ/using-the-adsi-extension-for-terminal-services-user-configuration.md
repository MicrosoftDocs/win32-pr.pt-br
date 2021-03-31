---
title: Usando a extensão ADSI para Serviços de Área de Trabalho Remota configuração de usuário
description: A administração de propriedades de usuário específicas de Serviços de Área de Trabalho Remota é possível usando os métodos implementados pela extensão ADSI (Active Directory Service Interfaces), que é empacotada com a biblioteca de vínculo dinâmico Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando a extensão ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917609"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Usando a extensão ADSI para Serviços de Área de Trabalho Remota configuração de usuário

A extensão de interface de serviço de Active Directory (ADSI) para Serviços de Área de Trabalho Remota configuração de usuário é uma biblioteca que é empacotada com a biblioteca de vínculo dinâmico Tsuserex.dll. A administração de propriedades de usuário específicas do Serviços de Área de Trabalho Remota é possível usando os métodos implementados pela extensão. Os métodos permitem a configuração das propriedades que estão disponíveis na interface de extensão para usuários Serviços de Área de Trabalho Remota.

A extensão ADSI para Serviços de Área de Trabalho Remota configuração de usuário dá suporte ao exame e à manipulação de Serviços de Área de Trabalho Remota Propriedades de usuário armazenadas no banco de dados do serviço de diretório. A extensão também dá suporte à configuração de propriedades do usuário que são armazenadas no Active Directory, por meio da API do protocolo LDAP.

O provedor implementa os seguintes métodos:

-   [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get). Esse método procura uma propriedade específica ou um conjunto de propriedades em uma instância da classe.
-   [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put). Esse método configura uma propriedade específica ou um conjunto de propriedades em uma instância da classe.

Consulte a [referência para a extensão ADSI para serviços de área de trabalho remota configuração de usuário](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) para obter uma lista das propriedades específicas do usuário serviços de área de trabalho remota que você pode configurar.

Para obter mais informações sobre como acessar e modificar atributos com ADSI, consulte [acessando e manipulando dados com ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).

Para obter mais informações sobre como usar as convenções de nomenclatura ADSI e as cadeias de caracteres de AdsPath, consulte as informações sobre [provedores de serviço ADSI](/windows/desktop/ADSI/adsi-system-providers) individuais na documentação do SDK (Software Development Kit) do [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform.

 

 