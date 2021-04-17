---
description: O COM (Component Object Model) é um padrão binário para escrever software de componente em um ambiente de computação distribuído.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Fazendo backup e restaurando o banco de dados de registro de classe COM+ em VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784979"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a><span data-ttu-id="839b4-103">Fazendo backup e restaurando o banco de dados de registro de classe COM+ em VSS</span><span class="sxs-lookup"><span data-stu-id="839b4-103">Backing Up and Restoring the COM+ Class Registration Database Under VSS</span></span>

<span data-ttu-id="839b4-104">O COM (Component Object Model) é um padrão binário para escrever software de componente em um ambiente de computação distribuído.</span><span class="sxs-lookup"><span data-stu-id="839b4-104">The Component Object Model (COM) is a binary standard for writing component software in a distributed computing environment.</span></span>

<span data-ttu-id="839b4-105">A implementação original do Win32 identificadores de componente armazenados (GUIDs) e outro Estado COM no registro sob **HKEY \_ classes \_ raiz \\ CLSID**.</span><span class="sxs-lookup"><span data-stu-id="839b4-105">The original Win32 implementation stored component identifiers (GUIDs) and other COM state in the registry under **HKEY\_CLASSES\_ROOT\\CLSID**.</span></span>

<span data-ttu-id="839b4-106">A geração atual do Component Object Model, COM+, oferece um banco de dados independente do registro para armazenar informações de registro do componente: o banco de dados de registro da classe COM+.</span><span class="sxs-lookup"><span data-stu-id="839b4-106">The current generation of the Component Object Model, COM+, offers a registry-independent database for storing component registration information: the COM+ Class Registration Database.</span></span>

<span data-ttu-id="839b4-107">O banco de dados de registro de classe COM+ dá suporte a um gravador VSS, que permite que os solicitantes cofrentem o banco de dados de registro usando os dados armazenados em um volume copiado por sombra.</span><span class="sxs-lookup"><span data-stu-id="839b4-107">The COM+ Class Registration Database supports a VSS writer, which allows requesters to back up the registration database using data stored on a shadow-copied volume.</span></span>

<span data-ttu-id="839b4-108">Para restaurar o banco de dados de registro do COM+, um solicitante deve chamar o método [ICOMAdminCatalog:: RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="839b4-108">To restore the COM+ Registration Database, a requester must call the [ICOMAdminCatalog::RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="839b4-109">Para obter mais informações sobre o gravador de banco de dados de registro do COM+, consulte [gravadores VSS in-box](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="839b4-109">For more information about the COM+ Registration Database writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
