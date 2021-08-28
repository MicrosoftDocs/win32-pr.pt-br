---
description: Se um aplicativo precisar ser registrado, crie o pacote de instalação conforme descrito na seção Adicionando e removendo chaves do registro na instalação ou remoção de componentes.
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: Adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6d3884a91efefac9cab1409a36e1843941469aae9822154be5534313b05c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105456"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a>Adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro

Se um aplicativo precisar ser registrado, crie o pacote de instalação conforme descrito na seção [adicionando e removendo chaves do registro na instalação ou remoção de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). O registro é usado pelo instalador para anúncio e pelo recurso Adicionar ou remover programas no painel de controle. Se um aplicativo não estiver registrado, ele não poderá ser anunciado e não estará listado no recurso Adicionar ou remover programas no painel de controle.

Você pode omitir o registro de um aplicativo removendo a ação [RegisterProduct](registerproduct-action.md), a ação [RegisterUser](registeruser-action.md), a ação [PublishProduct](publishproduct-action.md)e a [ação PublishFeatures](publishfeatures-action.md) da tabela [InstallExecuteSequence](installexecutesequence-table.md) e da [tabela AdvtExecuteSequence](advtexecutesequence-table.md). Todas essas ações devem ser removidas ou algum rastreamento do aplicativo pode permanecer no registro. A remoção de todas essas ações impede que o aplicativo seja listado no recurso Adicionar ou remover programas no painel de controle e impede o anúncio do aplicativo. remover todas essas ações também impede que o aplicativo seja registrado com os dados de configuração de Windows Installer. isso significa que você não pode remover, reparar ou reinstalar o aplicativo usando as [opções de linha de comando](command-line-options.md)Windows Installer ou a API (interface de programação de aplicativo) do Windows Installer.

para ocultar um aplicativo do recurso adicionar ou remover programas no painel de controle e ainda ser capaz de usar o Windows Installer para gerenciar um aplicativo, deixe as ações de registro nas tabelas de sequência e defina a [**propriedade ARPSYSTEMCOMPONENT**](arpsystemcomponent.md) na [tabela de propriedades](property-table.md) como 1 (uma). o aplicativo não aparece no recurso adicionar ou remover programas, mas você pode usar o Windows Installer para instalar sob demanda, desinstalar, reparar e reinstalar o aplicativo.

 

 



