---
description: Mostra como usar as interfaces VSS para criar um provedor de hardware VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Ferramenta VssSampleProvider e exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd84288f6dc878c103f639aa0c015a3e5e95bde
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884417"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Ferramenta VssSampleProvider e exemplo

Mostra como usar as [interfaces](volume-shadow-copy-api-interfaces.md) VSS para criar um provedor de hardware VSS.

> [!Note]  
> A ferramenta VssSampleProvider e o exemplo estão incluídos no SDK (Software Development Kit) do Microsoft Windows. Você pode baixar o SDK Windows do [Windows SDK (Software Development Kit) para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).

 

Na instalação do SDK do Windows, a ferramenta VssSampleProvider pode ser encontrada em (para Windows de `%Program Files(x86)%\Windows Kits\8.1\bin\x64` 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para 32 bits Windows).

> [!Note]  
> Os provedores de hardware só têm suporte em sistemas operacionais Windows Server. Em um Windows do cliente, você pode compilar o exemplo VssSampleProvider, mas não pode registrá-lo como um provedor de hardware.

 

A ferramenta VssSampleProvider consiste nos seguintes arquivos:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

O exemplo vssSampleProvider inclui os seguintes scripts de instalação e desinstalação:

-   Install-sampleprovider.cmd
-   Uninstall-sampleprovider.cmd
-   Registrar \_app.vbs

**Para instalar e usar o exemplo VssSampleProvider**

1.  Navegue até o diretório `Program Files (x86)\Windows Kits\8.0\bin\`. Esse diretório contém virtualstoragevss.sys e vstorcontrol.exe.
2.  Abra uma janela do prompt de comando no diretório especificado.
3.  Para instalar o driver de armazenamento virtual, na janela do prompt de comando, digite o seguinte comando:

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  Para instalar o provedor de exemplo do VSS, na janela do prompt de comando, digite o seguinte comando:

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  Para criar um LUN virtual, faça o seguinte.

    1.  Na janela de prompt de comando, digite o seguinte comando:

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        Esse comando cria um LUN virtual cujo identificador de armazenamento é o Provedor **HW de Exemplo do VSS.** Para criar LUNs virtuais adicionais, repita esta etapa.

        O provedor de exemplo do VSS reconhecerá um LUN somente se o Provedor HW de Exemplo do **VSS** for parte do identificador de armazenamento. Para obter mais informações sobre o identificador de armazenamento, consulte a postagem no blog a seguir.

        [LUN – Ressíncrono com Diskshadow e Virtual Armazenamento](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  Na janela do prompt de comando, use diskpart.exe formatar o disco virtual e atribuir uma letra da unidade a ele.

        Aqui está um script de exemplo a ser executado no prompt de comando diskpart.

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  Para executar o provedor de exemplo, na janela do prompt de comando, digite o seguinte comando:

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    *&lt; drive &gt;* representa a letra da unidade do LUN virtual.

7.  Para desinstalar o provedor de exemplo vss, na janela do prompt de comando, digite o seguinte comando:

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Para desinstalar o driver de armazenamento virtual, na janela do prompt de comando, digite o seguinte comando:

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



