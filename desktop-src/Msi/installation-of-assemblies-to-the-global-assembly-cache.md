---
description: o Windows Installer instala Common Language Runtime assemblies no cache de assembly global usando o .NET Framework da Microsoft.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Instalação de assemblies no cache de assembly global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dec84b507491da5b3ec4b2352044dc899230b41f41d2c81a943fba83b3ba0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634204"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Instalação de assemblies no cache de assembly global

o Windows Installer instala Common Language Runtime assemblies no cache de assembly global usando o .NET Framework da Microsoft. ao instalar assemblies no cache de assembly global, o instalador não pode usar a mesma estrutura de diretório e regras de versão de arquivo que ele usa ao instalar componentes de Windows Installer regulares. os componentes de Windows Installer regulares podem ser instalados em vários locais de diretório por produtos diferentes. Os assemblies podem existir apenas uma vez no cache de assembly. Cada assembly é adicionado e removido do cache de assembly como um indivisível inteiro; Portanto, todos os arquivos que compõem um assembly são sempre instalados ou removidos juntos.

o custo do disco de componentes de Windows Installer regulares e assemblies de Common Language Runtime são calculados de forma diferente. o custo total do disco de um componente Windows Installer regular inclui custos locais, custos de origem e custos de remoção. Para obter detalhes, consulte [custos de arquivo](file-costing.md). esse método não pode ser usado para Common Language Runtime assemblies de custo porque eles podem ter clientes diferentes do Windows Installer. o custo dos assemblies de Common Language Runtime deve ser determinado consultando o Common Language Runtime de .NET Framework da Microsoft.

o Windows Installer usa um processo transacional de duas etapas para instalar produtos que contêm assemblies Common Language Runtime. Isso permite a reversão da instalação e remoção do assembly. Para obter mais informações, consulte [reversão de assemblies no cache de assembly global](rollback-of-assemblies-in-the-global-assembly-cache.md).

observe que os assemblies instalados no cache de assembly global por uma instalação no [contexto de instalação](installation-context.md) por usuário não são protegidos por Windows proteção de arquivo. os Assemblies que são instalados no cache de assembly global por uma instalação no contexto de instalação por máquina são protegidos pelo [Proteção de Recursos do Windows](../wfp/windows-resource-protection-portal.md).

 

 
