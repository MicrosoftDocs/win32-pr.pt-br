---
description: Windows O instalador pode instalar vários pacotes usando o processamento de transações.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Multiple-Package instalação do Multiple-Package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d525c2904d25fb06403f85914f2b04fce2ebc57f22801a2413b2f09ad1c396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943407"
---
# <a name="multiple-package-installations"></a>Multiple-Package instalação do Multiple-Package

Windows O instalador pode instalar vários pacotes usando [*o processamento de transações*](t-gly.md). Essa funcionalidade está disponível a partir do Windows Installer 4.5. O instalador instalará todos os pacotes que pertencem a uma transação de vários pacotes ou a nenhum dos pacotes. Se todos os pacotes na transação não puderem ser instalados com êxito ou se o usuário cancelar a instalação, o instalador do Windows poderá reverter as alterações e restaurar o computador para seu estado original.

Um pacote de instalação de vários pacotes pode conter uma tabela [MsiEmbeddedChainer](msiembeddedchainer-table.md) que faz referência a uma função definida pelo usuário que usa as funções [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)e [**MsiEndTransaction.**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)

A [Tabela MsiPackageCertificate](msipackagecertificate-table.md) lista certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem uma instalação de vários pacotes. Você pode usar essa tabela para reduzir o número de vezes que [*sua*](u-gly.md) instalação de vários pacotes exibe um prompt de UAC (Controle de Conta de Usuário) que requer uma resposta de um administrador.

As funções Windows instalador a seguir podem fazer alterações no computador do usuário quando o instalador do Windows instala, repara, atualiza ou remove aplicativos. A partir do Windows 4.5, o instalador pode reverter as alterações [](t-gly.md) feitas por essas funções durante o processamento de transação de uma instalação de vários pacotes:

<dl>

[**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

Haverá uma exceção se o Windows instalador encontrar um pacote pertencente a uma instalação de vários pacotes que contém uma [ação ForceReboot](forcereboot-action.md) ou [ScheduleReboot.](schedulereboot-action.md) Nesse caso, o Windows Instalador não instala apenas esse pacote. Outros pacotes que pertencem à instalação de vários pacotes, que não contêm uma ação ForceReboot ou ScheduleReboot, podem ser instalados.

**[Windows Instalador 4.0](not-supported-in-windows-installer-4-0.md)e versões anteriores:[****](t-gly.md) Não há suporte para o processamento de transações de vários pacotes Windows instalações do Instalador. Essas versões do Windows Instalador não podem reverter a instalação de vários pacotes como uma única transação.

**Windows Server 2008 R2 com a [função Serviços de Área de Trabalho Remota](../termserv/terminal-services-portal.md) habilitada:** Sem suporte. Uma instalação de vários pacotes usando a [tabela MsiEmbeddedChainer](msiembeddedchainer-table.md) falhará [se](../termserv/terminal-services-portal.md) Serviços de Área de Trabalho Remota função estiver habilitada.

 

 
