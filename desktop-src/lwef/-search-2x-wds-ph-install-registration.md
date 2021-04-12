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
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a><span data-ttu-id="cab47-103">Instalando e Registrando manipuladores de protocolo (recursos de ambiente herdados do Windows)</span><span class="sxs-lookup"><span data-stu-id="cab47-103">Installing and Registering Protocol Handlers (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="cab47-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cab47-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cab47-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="cab47-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="cab47-106">A instalação de **manipuladores de protocolo** envolve copiar as DLLs para um local apropriado no diretório arquivos de programas e registrá-las.</span><span class="sxs-lookup"><span data-stu-id="cab47-106">Installing **protocol handlers** involves copying the DLL(s) to an appropriate location in the Program Files directory and registering them.</span></span>

<span data-ttu-id="cab47-107">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="cab47-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="cab47-108">Diretrizes de instalação</span><span class="sxs-lookup"><span data-stu-id="cab47-108">Installation Guidelines</span></span>](#installation-guidelines)
-   [<span data-ttu-id="cab47-109">Para registrar manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="cab47-109">To Register Protocol Handlers</span></span>](#to-register-protocol-handlers)
-   [<span data-ttu-id="cab47-110">Para registrar extensões do Shell</span><span class="sxs-lookup"><span data-stu-id="cab47-110">To Register Shell Extensions</span></span>](#to-register-shell-extensions)

## <a name="installation-guidelines"></a><span data-ttu-id="cab47-111">Diretrizes de instalação</span><span class="sxs-lookup"><span data-stu-id="cab47-111">Installation Guidelines</span></span>

<span data-ttu-id="cab47-112">Os manipuladores de protocolo devem implementar o auto-registro para instalação e devem seguir estas diretrizes:</span><span class="sxs-lookup"><span data-stu-id="cab47-112">Protocol handlers should implement self-registration for installation and should follow these guidelines:</span></span>

-   <span data-ttu-id="cab47-113">O instalador deve usar o EXE ou o instalador MSI.</span><span class="sxs-lookup"><span data-stu-id="cab47-113">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="cab47-114">As notas de versão devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="cab47-114">Release notes must be provided.</span></span>
-   <span data-ttu-id="cab47-115">Uma entrada **Adicionar/remover programas** deve ser criada para cada suplemento instalado.</span><span class="sxs-lookup"><span data-stu-id="cab47-115">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="cab47-116">O instalador deve assumir todas as configurações do registro para o tipo de arquivo específico ou o armazenamento que o suplemento atual compreende.</span><span class="sxs-lookup"><span data-stu-id="cab47-116">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="cab47-117">Se um suplemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.</span><span class="sxs-lookup"><span data-stu-id="cab47-117">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="cab47-118">Se um suplemento mais recente tiver substituído o suplemento anterior, deverá haver a capacidade de restaurar a funcionalidade do suplemento anterior e torná-lo o suplemento padrão para esse tipo de arquivo novamente.</span><span class="sxs-lookup"><span data-stu-id="cab47-118">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>

## <a name="to-register-protocol-handlers"></a><span data-ttu-id="cab47-119">Para registrar manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="cab47-119">To Register Protocol Handlers</span></span>

<span data-ttu-id="cab47-120">Você precisa fazer quatorze entradas no registro para registrar o componente de manipulador de protocolo, em que:</span><span class="sxs-lookup"><span data-stu-id="cab47-120">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="cab47-121">*Ver \_ A \_ ProgID do IND* é o ProgID independente da versão da implementação do manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="cab47-121">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="cab47-122">*Ver \_ \_ProgID DEP* é o ProgID dependente da versão da implementação do manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="cab47-122">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="cab47-123">*CLSID \_ 1* é o CLSID da implementação do manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="cab47-123">*CLSID\_1* is the CLSID of the protocol handler implementation</span></span>

1.  <span data-ttu-id="cab47-124">Registre o ProgID independente de versão com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="cab47-124">Register the version independent ProgID with the following keys and values:</span></span>

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

2.  <span data-ttu-id="cab47-125">Registre o ProgID dependente de versão com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="cab47-125">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="cab47-126">Registre o CLSID do manipulador de protocolo com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="cab47-126">Register the protocol handler's CLSID with the following keys and values:</span></span>

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

4.  <span data-ttu-id="cab47-127">Registre o manipulador de protocolo no Windows Desktop Search:</span><span class="sxs-lookup"><span data-stu-id="cab47-127">Register the protocol handler with Windows Desktop Search:</span></span>

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

## <a name="to-register-shell-extensions"></a><span data-ttu-id="cab47-128">Para registrar extensões do Shell</span><span class="sxs-lookup"><span data-stu-id="cab47-128">To Register Shell Extensions</span></span>

<span data-ttu-id="cab47-129">Você precisa fazer duas entradas no registro para registrar a extensão do shell do manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="cab47-129">You need to make two entries in the registry to register the protocol handler's Shell extension.</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




