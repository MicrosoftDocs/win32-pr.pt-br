---
title: Instalando e registrando manipuladores de protocolo (recursos Windows ambiente herdado)
description: A instalação de manipuladores de protocolo envolve copiar as DLL(s) para um local apropriado no diretório Arquivos de Programas e registrá-las.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f6cce4337c8b2c3faf47411f76165b11ed13ff00dfebd66ac5307d6ca6a68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716556"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>Instalando e registrando manipuladores de protocolo (recursos Windows ambiente herdado)

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search.](../search/-search-3x-wds-overview.md)

A instalação **de manipuladores de** protocolo envolve copiar as DLL(s) para um local apropriado no diretório Arquivos de Programas e registrá-las.

Esta seção contém os seguintes tópicos:

-   [Diretrizes de instalação](#installation-guidelines)
-   [Para registrar manipuladores de protocolo](#to-register-protocol-handlers)
-   [Para registrar extensões do Shell](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Diretrizes de instalação

Os manipuladores de protocolo devem implementar o autoregisto para instalação e devem seguir estas diretrizes:

-   O instalador deve usar o instalador EXE ou MSI.
-   As notas de versão devem ser fornecidas.
-   Uma **entrada Adicionar/Remover Programas** deve ser criada para cada complemento instalado.
-   O instalador deve assumir todas as configurações do Registro para o tipo de arquivo ou armazenamento específico que o complemento atual entende.
-   Se um complemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.
-   Se um novo complemento tiver substituído o complemento anterior, deverá haver a capacidade de restaurar a funcionalidade do complemento anterior e torná-la o complemento padrão para esse tipo de arquivo novamente.

## <a name="to-register-protocol-handlers"></a>Para registrar manipuladores de protocolo

Você precisa fazer 14 entradas no Registro para registrar o componente do manipulador de protocolo, em que:

-   *Ver \_ Ind \_ ProgID é* o ProgID independente de versão da implementação do manipulador de protocolo
-   *Ver \_ Dep \_ ProgID é* o ProgID dependente de versão da implementação do manipulador de protocolo
-   *CLSID \_ 1 é* a CLSID da implementação do manipulador de protocolo

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

4.  Registre o manipulador de protocolo com Windows Desktop Search:

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

Você precisa fazer duas entradas no Registro para registrar a extensão shell do manipulador de protocolo.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




