---
description: Módulos TopEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Módulos TopEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc95848a533ba67599c114917ebe502f42a4fe859df9c1ac6bf5acfc40bb393c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057711"
---
# <a name="topoedit-modules"></a>Módulos TopEdit

A ferramenta TopoEdit é fornecida com o SDK Windows para Windows Server 2008 e posterior. A ferramenta requer Windows Vista ou posterior.

Os módulos TopoEdit estão localizados na pasta Bin do SDK. Estes módulos são:

-   TopoEdit.exe— Executável do aplicativo
-   TEDUTIL.dll— DLL de extensão

A instalação do SDK registra a DLL. No entanto, se isso falhar, em um prompt de comando, execute o seguinte.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



O código-fonte para TopEdit também é fornecido como um exemplo no SDK do Windows. Ele está localizado no seguinte diretório:

<samples root>\\Multimídia \\ Media Foundation \\ TopoEdit

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução ao TopoEdit](introduction-to-topoedit.md)
</dt> <dt>

[TopEdit](topoedit.md)
</dt> </dl>

 

 



