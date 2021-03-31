---
description: Se um aplicativo precisar ser registrado, crie o pacote de instalação conforme descrito na seção Adicionando e removendo chaves do registro na instalação ou remoção de componentes.
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: Adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36804633a51e0e2f4beafc37e9f830e1743a5ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921528"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a>Adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro

Se um aplicativo precisar ser registrado, crie o pacote de instalação conforme descrito na seção [adicionando e removendo chaves do registro na instalação ou remoção de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). O registro é usado pelo instalador para anúncio e pelo recurso Adicionar ou remover programas no painel de controle. Se um aplicativo não estiver registrado, ele não poderá ser anunciado e não estará listado no recurso Adicionar ou remover programas no painel de controle.

Você pode omitir o registro de um aplicativo removendo a ação [RegisterProduct](registerproduct-action.md), a ação [RegisterUser](registeruser-action.md), a ação [PublishProduct](publishproduct-action.md)e a [ação PublishFeatures](publishfeatures-action.md) da tabela [InstallExecuteSequence](installexecutesequence-table.md) e da [tabela AdvtExecuteSequence](advtexecutesequence-table.md). Todas essas ações devem ser removidas ou algum rastreamento do aplicativo pode permanecer no registro. A remoção de todas essas ações impede que o aplicativo seja listado no recurso Adicionar ou remover programas no painel de controle e impede o anúncio do aplicativo. Remover todas essas ações também impede que o aplicativo seja registrado com os dados de configuração de Windows Installer. Isso significa que você não pode remover, reparar ou reinstalar o aplicativo usando as [Opções de linha de comando](command-line-options.md)Windows Installer ou a API (interface de programação de aplicativo) do Windows Installer.

Para ocultar um aplicativo do recurso Adicionar ou remover programas no painel de controle e ainda ser capaz de usar o Windows Installer para gerenciar um aplicativo, deixe as ações de registro nas tabelas de sequência e defina a [**Propriedade ARPSYSTEMCOMPONENT**](arpsystemcomponent.md) na [tabela de propriedades](property-table.md) como 1 (uma). O aplicativo não aparece no recurso Adicionar ou remover programas, mas você pode usar o Windows Installer para instalar sob demanda, desinstalar, reparar e reinstalar o aplicativo.

 

 



