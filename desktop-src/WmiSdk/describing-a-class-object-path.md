---
description: Um caminho de objeto de classe descreve o local de uma classe dentro de um namespace.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Descrevendo um caminho de objeto de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6801d91c4236a7892d7db121dc02c73d93640b7dbc4969c86db55a8789b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244396"
---
# <a name="describing-a-class-object-path"></a>Descrevendo um caminho de objeto de classe

Um caminho de objeto de classe descreve o local de uma classe dentro de um namespace.

Você pode usar os seguintes métodos para especificar um caminho de objeto:

-   Um caminho de objeto completo para uma classe anexa o nome da classe a um caminho de namespace.

    O exemplo a seguir mostra o local da classe [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no \\ \\ namespace raiz cimv2 no servidor chamado Admin.

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   Um caminho de objeto relativo representa uma classe que reside no namespace atual. Um caminho de objeto relativo para uma classe contém apenas o nome da classe.

    O exemplo a seguir mostra o caminho relativo para a [**classe \_ LogicalDisk do Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)

    ``` syntax
    Win32_LogicalDisk
    ```

Quando você consulta um nome de classe, mas não especifica nenhuma instância, o WMI retorna a definição de classe. O procedimento a seguir descreve como recuperar uma definição de classe no VBScript.

**Para recuperar uma definição de classe no VBScript**

-   Você pode usar a conexão moniker com uma consulta ou [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx). Você também pode usar [**SWbemServices.Get.**](swbemservices-get.md)

    O exemplo a seguir mostra como usar [GetObject para](/previous-versions//kdccchxa(v=vs.85)) obter uma definição de classe.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    O exemplo a seguir mostra como consultar uma definição de classe.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

Você pode recuperar uma definição de classe em C++ especificando apenas o nome da classe e nenhum caminho para uma instância específica. O procedimento a seguir descreve como recuperar uma definição de classe em C++.

**Para recuperar uma definição de classe em C++**

-   Faça uma chamada para as funções [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices::GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

    O exemplo a seguir mostra como chamar a [**função IWbemServices::GetObject.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    O exemplo de código anterior requer que a \# instrução include a seguir seja compilada corretamente.

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
