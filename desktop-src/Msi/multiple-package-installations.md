---
description: Windows Installer pode instalar vários pacotes usando o processamento de transações.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Instalações do Multiple-Package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fa30893f353d6661a7f77fe23fe55b4c9b22c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782330"
---
# <a name="multiple-package-installations"></a>Instalações do Multiple-Package

Windows Installer pode instalar vários pacotes usando o [*processamento de transações*](t-gly.md). Essa funcionalidade está disponível a partir do Windows Installer 4,5. O instalador instalará todos os pacotes que pertencem a uma transação de vários pacotes ou nenhum dos pacotes. Se todos os pacotes na transação não puderem ser instalados com êxito ou se o usuário cancelar a instalação, o Windows Installer poderá reverter as alterações e restaurar o computador ao seu estado original.

Um pacote de instalação de vários pacotes pode conter uma [tabela MsiEmbeddedChainer](msiembeddedchainer-table.md) que faz referência a uma função definida pelo usuário que usa as funções [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)e [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) .

A [tabela MsiPackageCertificate](msipackagecertificate-table.md) lista os certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem uma instalação de vários pacotes. Você pode usar essa tabela para reduzir o número de vezes que a instalação de vários pacotes exibe um prompt de [*controle de conta de usuário*](u-gly.md) (UAC) que requer uma resposta por um administrador.

As funções Windows Installer a seguir podem fazer alterações no computador do usuário quando o Windows Installer instala, repara, atualiza ou remove aplicativos. A partir do Windows Installer 4,5, o instalador pode reverter as alterações feitas por essas funções durante o [*processamento de transações*](t-gly.md) de uma instalação de vários pacotes:

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

Haverá uma exceção se o Windows Installer encontrar um pacote que pertence a uma instalação de vários pacotes que contém uma ação [ForceReboot](forcereboot-action.md) ou [ScheduleReboot](schedulereboot-action.md) . Nesse caso, Windows Installer não instala apenas esse pacote. Outros pacotes que pertencem à instalação de vários pacotes, que não contêm uma ação ForceReboot ou ScheduleReboot, podem ser instalados.

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md): * * não há suporte para o [*processamento de transações*](t-gly.md) de vários pacotes Windows Installer instalações. Essas versões do Windows Installer não podem reverter a instalação de vários pacotes como uma única transação.

**Windows Server 2008 R2 com a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) habilitada:** Sem suporte. Uma instalação de vários pacotes usando a [tabela MsiEmbeddedChainer](msiembeddedchainer-table.md) falhará se a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) estiver habilitada.

 

 
