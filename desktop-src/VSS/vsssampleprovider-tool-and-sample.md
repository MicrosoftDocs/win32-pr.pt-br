---
description: Mostra como usar as interfaces VSS para criar um provedor de hardware VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Ferramenta VssSampleProvider e exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763408"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Ferramenta VssSampleProvider e exemplo

Mostra como usar as [interfaces](volume-shadow-copy-api-interfaces.md) VSS para criar um provedor de hardware VSS.

> [!Note]  
> A ferramenta VssSampleProvider e o exemplo estão incluídos no SDK (Software Development Kit) do Microsoft Windows. Você pode baixar o SDK do Windows do [SDK (Software Development Kit) do Windows para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).

 

Na instalação do SDK do Windows, a ferramenta VssSampleProvider pode ser encontrada em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para o Windows de 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para o windows de 32 bits).

> [!Note]  
> Os provedores de hardware só têm suporte em sistemas operacionais Windows Server. Em um sistema operacional cliente Windows, você pode compilar o exemplo VssSampleProvider, mas não pode registrá-lo como um provedor de hardware.

 

A ferramenta VssSampleProvider consiste nos seguintes arquivos:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

O exemplo de VssSampleProvider inclui os seguintes scripts de instalação e desinstalação:

-   Install-SampleProvider. cmd
-   Uninstall-SampleProvider. cmd
-   Registrar \_app.vbs

**Para instalar e usar o exemplo de VssSampleProvider**

1.  Navegue até o diretório `Program Files (x86)\Windows Kits\8.0\bin\`. Esse diretório contém virtualstoragevss.sys e vstorcontrol.exe.
2.  Abra uma janela de prompt de comando no diretório especificado.
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

        

        Este comando cria um LUN virtual cujo identificador de armazenamento é um **provedor de HW de exemplo VSS**. Para criar LUNs virtuais adicionais, repita essa etapa.

        O provedor de exemplo do VSS reconhece um LUN somente se o **provedor de HW de exemplo do VSS** faz parte do identificador de armazenamento. Para obter mais informações sobre o identificador de armazenamento, consulte a seguinte postagem no blog.

        [LUN-ressincronização com o DiskShadow e o armazenamento virtual](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  Na janela do prompt de comando, use diskpart.exe para formatar o disco virtual e atribuir uma letra da unidade a ele.

        Aqui está um script de exemplo a ser executado no prompt de comando do DiskPart.

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

    

    *<drive>* representa a letra da unidade do LUN virtual.

7.  Para desinstalar o provedor de exemplo do VSS, na janela do prompt de comando, digite o seguinte comando:

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Para desinstalar o driver de armazenamento virtual, na janela do prompt de comando, digite o seguinte comando:

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



