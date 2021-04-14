---
description: Os binários do Windows Server 2003 com Service Pack 1 (SP1) são compatíveis com o Windows Vista e o Windows Server 2008. No entanto, os binários de versões anteriores do Windows devem ser recompilados.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Portando aplicativos de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505746"
---
# <a name="porting-backup-applications"></a>Portando aplicativos de backup

Os binários do Windows Server 2003 com Service Pack 1 (SP1) são compatíveis com o Windows Vista e o Windows Server 2008. No entanto, os binários de versões anteriores do Windows devem ser recompilados.

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>Portando aplicativos de backup do Windows XP para o Windows Vista

Várias interfaces VSS foram alteradas desde o Windows XP. No mínimo, os aplicativos do Windows XP devem ser recompilados usando arquivos de cabeçalho e bibliotecas do SDK do VSS 7,2 ou do SDK do Windows Vista ou do Windows Server 2008.

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>Portando aplicativos de backup do Windows Server 2003 SP1 para o Windows Vista

Os binários do Windows Server 2003 com SP1 são compatíveis com o Windows Vista e o Windows Server 2008. No entanto, a maioria dos aplicativos de backup do Windows Server 2003 com SP1 deve ser atualizada para considerar novos recursos, que são descritos nas seções a seguir.

## <a name="compiling-backup-applications-for-windows-vista"></a>Compilando aplicativos de backup para o Windows Vista

Os aplicativos que usam interfaces disponíveis no Windows Server 2003 podem ser compilados usando arquivos de cabeçalho e bibliotecas fornecidas no SDK do VSS 7,2. Para usar novas interfaces, os aplicativos devem ser recompilados usando os arquivos de cabeçalho e as bibliotecas incluídas no SDK do Windows Vista.

> [!Note]  
> Os binários compilados usando o Windows Vista ou o Windows Server 2008 não são compatíveis com o Windows Server 2003 com SP1 ou versões anteriores do Windows.

 

 

 



