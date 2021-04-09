---
description: Depois que a cópia de sombra for concluída, o mecanismo mais importante para obter acesso aos dados de arquivo que ele contém é por meio do uso do objeto de dispositivo da cópia de sombra.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Acesso do solicitante aos dados copiados de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091429"
---
# <a name="requester-access-to-shadow-copied-data"></a><span data-ttu-id="9f4fe-103">Acesso do solicitante aos dados copiados de sombra</span><span class="sxs-lookup"><span data-stu-id="9f4fe-103">Requester Access to Shadow Copied Data</span></span>

<span data-ttu-id="9f4fe-104">Depois que a cópia de sombra for concluída, o mecanismo mais importante para obter acesso aos dados de arquivo que ele contém é por meio do uso do [*objeto de dispositivo*](vssgloss-d.md)da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-104">Once the shadow copy has completed, the most important mechanism for getting access to the file data it contains is through the use of the shadow copy's [*device object*](vssgloss-d.md).</span></span>

<span data-ttu-id="9f4fe-105">O membro **m \_ pwszSnapshotDeviceObject** de uma estrutura de [**\_ \_ prop instantâneo do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) é uma cadeia de caracteres que contém um objeto de dispositivo de volume copiado por sombra.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-105">The **m\_pwszSnapshotDeviceObject** member of a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure is a string containing a shadow-copied volume's device object.</span></span> <span data-ttu-id="9f4fe-106">Um solicitante pode obter um objeto de **\_ \_ prop snapshot do VSS** do volume copiado por sombra se ele souber **a \_ ID do VSS** do volume (GUID de identificação) e passá-lo para [**IVssBackupComponents:: getinstantâneoproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="9f4fe-106">A requester can obtain a shadow-copied volume's **VSS\_SNAPSHOT\_PROP** object if it knows the volume's **VSS\_ID** (identifying GUID) and passes it to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="9f4fe-107">Um solicitante também pode obter informações de propriedade de cópia de sombra usando o membro **obj. snap** da estrutura de [**\_ \_ prop do objeto VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que é uma estrutura de [**\_ \_ prop instantâneo do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtida usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para iterar na lista de objetos retornados por uma chamada para [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="9f4fe-107">A requester can also obtain shadow copy property information by using the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) structure (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

<span data-ttu-id="9f4fe-108">O objeto de dispositivo deve ser interpretado como a raiz de um volume copiado por sombra.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-108">The device object should be interpreted as the root of a shadow-copied volume.</span></span> <span data-ttu-id="9f4fe-109">Por esse motivo, o objeto de dispositivo não contém nenhuma barra invertida (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="9f4fe-109">For this reason, the device object contains no backslash ("\\").</span></span>

<span data-ttu-id="9f4fe-110">Os caminhos no volume copiado de sombra são obtidos pela substituição da raiz do caminho original pelo objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-110">Paths on the shadow copied volume are obtained by replacing the root of the original path with the device object.</span></span> <span data-ttu-id="9f4fe-111">Por exemplo, dado um caminho no volume original de "C: \\ Database \\ \* . mdb" e uma instância [**de \_ \_ prop de instantâneo do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) de snapProp, você obteria o caminho no volume de sombra copiado concatenando snapPropm \_ pwszShadow copyDeviceObject, " \\ " e " \\ Database \\ \* . mdb".</span><span class="sxs-lookup"><span data-stu-id="9f4fe-111">For example, given a path on the original volume of "C:\\DATABASE\\\*.mdb" and a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) instance of snapProp, you would obtain the path on the shadow copied volume by concatenating snapPropm\_pwszShadow copyDeviceObject, "\\", and "\\DATABASE\\\*.mdb".</span></span>

<span data-ttu-id="9f4fe-112">Os conjuntos de arquivos do VSS podem ter caracteres curinga em seus descritores de arquivo, portanto, obter uma lista completa dos arquivos em uma cópia de sombra gerenciada por um componente pode exigir o uso de métodos como **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-112">The VSS file sets might have wildcard characters in their file descriptors, so obtaining a full list of the files on a shadow copy managed by a component might require the use of methods such as **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>

 

 



