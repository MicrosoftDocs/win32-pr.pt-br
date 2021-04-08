---
description: Módulos TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Módulos TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010803"
---
# <a name="topoedit-modules"></a>Módulos TopoEdit

A ferramenta TopoEdit é fornecida com o SDK do Windows para Windows Server 2008 e posterior. A ferramenta requer o Windows Vista ou posterior.

Os módulos TopoEdit estão localizados na pasta bin do SDK. Esses módulos são:

-   TopoEdit.exe — executável do aplicativo
-   TEDUTIL.dll — DLL de extensão

A instalação do SDK registra a DLL. No entanto, se isso falhar, em um prompt de comando, execute o seguinte.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



O código-fonte para TopoEdit também é fornecido como um exemplo na SDK do Windows. Ele está localizado no seguinte diretório:

<samples root>\\Multimídia \\ Media Foundation \\ TopoEdit

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução ao TopoEdit](introduction-to-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



