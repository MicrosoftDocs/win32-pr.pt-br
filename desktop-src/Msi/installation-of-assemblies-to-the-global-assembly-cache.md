---
description: O Windows Installer instala Common Language Runtime assemblies no cache de assembly global usando a estrutura de Microsoft .NET.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Instalação de assemblies no cache de assembly global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719be313ad74374950092936bbd6124da779a0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164874"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Instalação de assemblies no cache de assembly global

O Windows Installer instala Common Language Runtime assemblies no cache de assembly global usando a estrutura de Microsoft .NET. Ao instalar assemblies no cache de assembly global, o instalador não pode usar a mesma estrutura de diretório e regras de versão de arquivo que ele usa ao instalar componentes de Windows Installer regulares. Os componentes de Windows Installer regulares podem ser instalados em vários locais de diretório por produtos diferentes. Os assemblies podem existir apenas uma vez no cache de assembly. Cada assembly é adicionado e removido do cache de assembly como um indivisível inteiro; Portanto, todos os arquivos que compõem um assembly são sempre instalados ou removidos juntos.

O custo do disco de componentes de Windows Installer regulares e assemblies de Common Language Runtime são calculados de forma diferente. O custo total do disco de um componente Windows Installer regular inclui custos locais, custos de origem e custos de remoção. Para obter detalhes, consulte [custos de arquivo](file-costing.md). Esse método não pode ser usado para Common Language Runtime assemblies de custo porque eles podem ter clientes diferentes do Windows Installer. O custo dos assemblies de Common Language Runtime deve ser determinado consultando a Common Language Runtime do Microsoft .NET Framework.

O Windows Installer usa um processo transacional de duas etapas para instalar produtos que contêm assemblies Common Language Runtime. Isso permite a reversão da instalação e remoção do assembly. Para obter mais informações, consulte [reversão de assemblies no cache de assembly global](rollback-of-assemblies-in-the-global-assembly-cache.md).

Observe que os assemblies instalados no cache de assembly global por uma instalação no [contexto de instalação](installation-context.md) por usuário não são protegidos pela proteção de arquivo do Windows. Os assemblies que são instalados no cache de assembly global por uma instalação no contexto de instalação por máquina são protegidos pelo [proteção de recursos do Windows](../wfp/windows-resource-protection-portal.md).

 

 
