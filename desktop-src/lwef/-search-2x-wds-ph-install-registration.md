---
title: Instalando e Registrando manipuladores de protocolo (recursos de ambiente herdados do Windows)
description: A instalação de manipuladores de protocolo envolve copiar as DLLs para um local apropriado no diretório arquivos de programas e registrá-las.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294737"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>Instalando e Registrando manipuladores de protocolo (recursos de ambiente herdados do Windows)

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

A instalação de **manipuladores de protocolo** envolve copiar as DLLs para um local apropriado no diretório arquivos de programas e registrá-las.

Esta seção contém os seguintes tópicos:

-   [Diretrizes de instalação](#installation-guidelines)
-   [Para registrar manipuladores de protocolo](#to-register-protocol-handlers)
-   [Para registrar extensões do Shell](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Diretrizes de instalação

Os manipuladores de protocolo devem implementar o auto-registro para instalação e devem seguir estas diretrizes:

-   O instalador deve usar o EXE ou o instalador MSI.
-   As notas de versão devem ser fornecidas.
-   Uma entrada **Adicionar/remover programas** deve ser criada para cada suplemento instalado.
-   O instalador deve assumir todas as configurações do registro para o tipo de arquivo específico ou o armazenamento que o suplemento atual compreende.
-   Se um suplemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.
-   Se um suplemento mais recente tiver substituído o suplemento anterior, deverá haver a capacidade de restaurar a funcionalidade do suplemento anterior e torná-lo o suplemento padrão para esse tipo de arquivo novamente.

## <a name="to-register-protocol-handlers"></a>Para registrar manipuladores de protocolo

Você precisa fazer quatorze entradas no registro para registrar o componente de manipulador de protocolo, em que:

-   *Ver \_ A \_ ProgID do IND* é o ProgID independente da versão da implementação do manipulador de protocolo
-   *Ver \_ \_ProgID DEP* é o ProgID dependente da versão da implementação do manipulador de protocolo
-   *CLSID \_ 1* é o CLSID da implementação do manipulador de protocolo

1.  Registre o ProgID independente de versão com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  Registre o ProgID dependente de versão com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  Registre o CLSID do manipulador de protocolo com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  Registre o manipulador de protocolo no Windows Desktop Search:

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a>Para registrar extensões do Shell

Você precisa fazer duas entradas no registro para registrar a extensão do shell do manipulador de protocolo.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




