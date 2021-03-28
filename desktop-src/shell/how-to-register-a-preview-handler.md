---
description: Este tópico explica como registrar um Gerenciador de visualização associado a um determinado tipo de dados.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Como registrar um Gerenciador de visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967892"
---
# <a name="how-to-register-a-preview-handler"></a><span data-ttu-id="fe33c-103">Como registrar um Gerenciador de visualização</span><span class="sxs-lookup"><span data-stu-id="fe33c-103">How to Register a Preview Handler</span></span>

<span data-ttu-id="fe33c-104">Este tópico explica como registrar um Gerenciador de visualização associado a um determinado tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fe33c-104">This topic explains how to register a preview handler associated with a given data type.</span></span> <span data-ttu-id="fe33c-105">Para fins de ilustração, os exemplos neste tópico usam um tipo de arquivo. xyz.</span><span class="sxs-lookup"><span data-stu-id="fe33c-105">For the purposes of illustration, examples in this topic use a .xyz file type.</span></span> <span data-ttu-id="fe33c-106">O registro de um Gerenciador de visualização é um registro padrão baseado em associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fe33c-106">Registration of a preview handler is a standard file association-based registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="fe33c-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="fe33c-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="fe33c-108">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="fe33c-108">Step 1:</span></span>

<span data-ttu-id="fe33c-109">Primeiro, uma extensão de nome de arquivo é associada a um ProgID.</span><span class="sxs-lookup"><span data-stu-id="fe33c-109">First, a file name extension is associated with a ProgID.</span></span> <span data-ttu-id="fe33c-110">A entrada a seguir associa a subchave ProgID **xyzfile** com a extensão de nome de arquivo. xyz.</span><span class="sxs-lookup"><span data-stu-id="fe33c-110">The following entry associates the **xyzfile** ProgID subkey with the .xyz file name extension.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

<span data-ttu-id="fe33c-111">A subchave ProgID do **xyzfile** é armazenada com os outros ProgIDs, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="fe33c-111">The **xyzfile** ProgID subkey is stored with the other ProgIDs as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
```

<span data-ttu-id="fe33c-112">Cada subchave ProgID do Gerenciador de visualização contém uma subchave chamada **shellex** que contém uma subchave *sempre* chamada **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span><span class="sxs-lookup"><span data-stu-id="fe33c-112">Each preview handler ProgID subkey contains a subkey named **shellex** that contains a subkey *always* named **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span></span> <span data-ttu-id="fe33c-113">A presença dessa subchave informa ao sistema que o manipulador é um Gerenciador de visualização.</span><span class="sxs-lookup"><span data-stu-id="fe33c-113">The presence of that subkey tells the system that the handler is a preview handler.</span></span>

<span data-ttu-id="fe33c-114">O valor padrão da subchave **{8895b1c6-b41f-4c1c-a562-0d564250836f}** é o identificador de classe (CLSID) do seu manipulador.</span><span class="sxs-lookup"><span data-stu-id="fe33c-114">The default value of the **{8895b1c6-b41f-4c1c-a562-0d564250836f}** subkey is the class identifier (CLSID) of your handler.</span></span> <span data-ttu-id="fe33c-115">Um exemplo da subchave ProgID **xyzfile** é mostrado aqui, associando um manipulador de CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span><span class="sxs-lookup"><span data-stu-id="fe33c-115">An example of the **xyzfile** ProgID subkey is shown here, associating a handler of CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a><span data-ttu-id="fe33c-116">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="fe33c-116">Step 2:</span></span>

<span data-ttu-id="fe33c-117">Em seguida, adicione a subchave sob **CLSID** para o seu Gerenciador de visualização.</span><span class="sxs-lookup"><span data-stu-id="fe33c-117">Next, add the subkey under **CLSID** for your preview handler.</span></span> <span data-ttu-id="fe33c-118">Um exemplo é mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="fe33c-118">An example is shown here.</span></span> <span data-ttu-id="fe33c-119">Segue uma explicação das entradas individuais.</span><span class="sxs-lookup"><span data-stu-id="fe33c-119">An explanation of individual entries follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

<span data-ttu-id="fe33c-120">O valor padrão para sua subchave (aqui, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) não é obrigatório ou usado.</span><span class="sxs-lookup"><span data-stu-id="fe33c-120">The default value for your subkey (here, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) is not required or used.</span></span> <span data-ttu-id="fe33c-121">No entanto, configurá-lo como uma cadeia de caracteres não-localada pode ajudá-lo a depurar problemas de registro.</span><span class="sxs-lookup"><span data-stu-id="fe33c-121">However, setting it to a nonlocalized string can help you to debug registration issues.</span></span>

<span data-ttu-id="fe33c-122">O sinal de subtração (-101) no recurso. dll na entrada DisplayName existe por motivos herdados.</span><span class="sxs-lookup"><span data-stu-id="fe33c-122">The minus sign (-101) in the .dll resource in the DisplayName entry exists for legacy reasons.</span></span> <span data-ttu-id="fe33c-123">A entrada de ícone, por outro lado, não requer um sinal de subtração.</span><span class="sxs-lookup"><span data-stu-id="fe33c-123">The Icon entry, on the other hand, does not require a minus sign.</span></span>

<span data-ttu-id="fe33c-124">O valor de AppID fornece uma referência à AppID do aplicativo associado à extensão de nome de arquivo (armazenada sob a ID do grupo de **classe de hKey \_ \_ raiz** \\ .</span><span class="sxs-lookup"><span data-stu-id="fe33c-124">The AppID value gives a reference to the AppID of the application associated with the file name extension (stored under **HKEY\_CLASSES\_ROOT**\\**APPID**.</span></span> <span data-ttu-id="fe33c-125">O valor usado aqui — {6d2b5079-2f0b-48dd-ab7f-97cec514d30b} — é a ID da Prevhost.exe host substituto.</span><span class="sxs-lookup"><span data-stu-id="fe33c-125">The value used here—{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}—is the ID of the Prevhost.exe surrogate host.</span></span> <span data-ttu-id="fe33c-126">os gerenciadores de visualização de 32 bits devem usar **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} quando instalados em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fe33c-126">32-bit preview handlers should use **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} when installed on 64-bit operating systems.</span></span>

<span data-ttu-id="fe33c-127">As entradas na subchave **InprocServer32** incluem uma referência de volta à subchave ProgID da extensão de nome de arquivo, bem como uma entrada para um [VersionIndependentProgId](../com/versionindependentprogid.md).</span><span class="sxs-lookup"><span data-stu-id="fe33c-127">The entries under the **InprocServer32** subkey include a reference back to the file name extension's ProgID subkey as well as an entry for a [VersionIndependentProgID](../com/versionindependentprogid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="fe33c-128">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="fe33c-128">Step 3:</span></span>

<span data-ttu-id="fe33c-129">Por fim, o Gerenciador de visualização deve ser adicionado à lista de todos os gerenciadores de visualização.</span><span class="sxs-lookup"><span data-stu-id="fe33c-129">Finally, the preview handler must be added to the list of all preview handlers.</span></span> <span data-ttu-id="fe33c-130">Essa lista é usada como uma otimização pelo sistema para enumerar todos os gerenciadores de visualização registrados para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="fe33c-130">This list is used as an optimization by the system to enumerate all registered preview handlers for display purposes.</span></span> <span data-ttu-id="fe33c-131">Novamente, o valor padrão não é necessário, ele simplesmente ajuda no processo de depuração.</span><span class="sxs-lookup"><span data-stu-id="fe33c-131">Again, the default value is not required, it simply aids in the debugging process.</span></span>

> [!Note]  
> <span data-ttu-id="fe33c-132">No Windows 7, se o aplicativo estiver instalado para todos os usuários do computador, use HKEY \_ local \_ Machine; se para apenas um usuário, use hKey \_ Current \_ User.</span><span class="sxs-lookup"><span data-stu-id="fe33c-132">In Windows 7, if the application is installed for all users of the computer, use HKEY\_LOCAL\_MACHINE; if for only one user, use HKEY\_CURRENT\_USER.</span></span>

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a><span data-ttu-id="fe33c-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe33c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe33c-134">Gerenciadores de visualização e host de visualização do Shell</span><span class="sxs-lookup"><span data-stu-id="fe33c-134">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="fe33c-135">Criando gerenciadores de visualização</span><span class="sxs-lookup"><span data-stu-id="fe33c-135">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="fe33c-136">Diretrizes do Gerenciador de visualização</span><span class="sxs-lookup"><span data-stu-id="fe33c-136">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
