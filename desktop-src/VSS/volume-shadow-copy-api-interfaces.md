---
description: A API Serviço de Cópias de Sombra de Volume (VSS) fornece interfaces COM e C++ para dar suporte à criação de solicitantes e autores.
ms.assetid: 3a0c60df-666c-4e33-a54c-7fa5ddbfde13
title: Interfaces da API de Cópia de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8820566e952a43f56e45c49e925aab2375c0ea3994015717e6c4bc345f0c7f78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121549"
---
# <a name="volume-shadow-copy-api-interfaces"></a>Interfaces da API de Cópia de Sombra de Volume

A API Serviço de Cópias de Sombra de Volume (VSS) fornece interfaces COM e C++ para dar suporte à criação de solicitantes e autores.

## <a name="vss-requester-specific-interfaces"></a>VSS Requester-Specific Interfaces

-   [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   [**IVssBackupComponentsEx**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex)
-   [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
-   [**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)
-   [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
-   [**IVssExamineWriterMetadataEx**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex)
-   [**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)
-   [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
-   [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)

## <a name="vss-writer-specific-interfaces"></a>VSS Writer-Specific Interfaces

-   [**IVssCreateExpressWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)
-   [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
-   [**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)
-   [**IVssExpressWriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)
-   [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

## <a name="vss-hardware-provider-specific-interfaces"></a>VSS Hardware Provider-Specific Interfaces

-   [**IVssAdmin**](/windows/desktop/api/VsAdmin/nn-vsadmin-ivssadmin)
-   [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider)
-   [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)
-   [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset)
-   [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications)

## <a name="vss-software-provider-specific-interfaces"></a>VSS Software Provider-Specific Interfaces

-   [**IVssSoftwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsssoftwaresnapshotprovider)

## <a name="vss-shared-interfaces"></a>Interfaces compartilhadas do VSS

-   [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)
-   [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
-   [**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)
-   [**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)
-   [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject)
-   [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)
-   [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

## <a name="vss-management-interfaces"></a>Interfaces de gerenciamento do VSS

-   [**IVssDifferentialSoftwareSnapshotMgmt**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt)
-   [**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)
-   [**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)
-   [**IVssEnumMgmtObject**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssenummgmtobject)
-   [**IVssSnapshotMgmt**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt)
-   [**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 
