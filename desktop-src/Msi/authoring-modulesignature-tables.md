---
description: A tabela ModuleSignature contém todas as informações necessárias para identificar o módulo de mesclagem.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Criando tabelas ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752663"
---
# <a name="authoring-modulesignature-tables"></a>Criando tabelas ModuleSignature

A [tabela ModuleSignature](modulesignature-table.md) contém todas as informações necessárias para identificar o módulo de mesclagem.

O campo ModuleID é a chave primária para esta tabela e deve seguir a Convenção descrita em [nomeando chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md). Por exemplo, se o nome legível do módulo de mesclagem for MyLibrary e o GUID do módulo de mesclagem for {880DE2F0-CDD8-11D1-A849-006097ABDE17}, a entrada na coluna ModuleID da tabela ModuleSignature se tornará MyLibrary. 880DE2F0 \_ CDD8 11D1 A849 006097ABDE17 \_ \_ \_ .

Insira o identificador decimal para o idioma padrão do módulo de mesclagem no campo idioma da tabela ModuleSignature.

Insira a versão do módulo de mesclagem no campo versão.

 

 



