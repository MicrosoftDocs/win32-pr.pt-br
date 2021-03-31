---
title: Instalação do manipulador de arquivos e fluxos
description: Instalação do manipulador de arquivos e fluxos
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636934"
---
# <a name="file-and-stream-handler-installation"></a><span data-ttu-id="3746a-103">Instalação do manipulador de arquivos e fluxos</span><span class="sxs-lookup"><span data-stu-id="3746a-103">File and Stream Handler Installation</span></span>

<span data-ttu-id="3746a-104">A biblioteca AVIFile usa manipuladores de fluxo e arquivo instalados para ler e gravar arquivos AVI e fluxos.</span><span class="sxs-lookup"><span data-stu-id="3746a-104">The AVIFile library uses installed stream and file handlers for reading and writing AVI files and streams.</span></span> <span data-ttu-id="3746a-105">Um manipulador é instalado quando ele reside no diretório de sistema do Windows e o registro contém as seguintes informações necessárias para descrever e identificar um manipulador:</span><span class="sxs-lookup"><span data-stu-id="3746a-105">A handler is installed when it resides in the Windows SYSTEM directory and the registry contains the following information needed to describe and identify a handler:</span></span>

-   <span data-ttu-id="3746a-106">O identificador de classe de 16 bytes para o manipulador</span><span class="sxs-lookup"><span data-stu-id="3746a-106">The 16-byte class identifier for the handler</span></span>
-   <span data-ttu-id="3746a-107">Uma breve descrição do manipulador</span><span class="sxs-lookup"><span data-stu-id="3746a-107">A brief description of the handler</span></span>
-   <span data-ttu-id="3746a-108">O nome do arquivo que contém o manipulador</span><span class="sxs-lookup"><span data-stu-id="3746a-108">The name of the file containing the handler</span></span>
-   <span data-ttu-id="3746a-109">A extensão de arquivo que um manipulador de arquivo pode processar</span><span class="sxs-lookup"><span data-stu-id="3746a-109">The file extension that a file handler can process</span></span>
-   <span data-ttu-id="3746a-110">Acesso a arquivos e outras propriedades associadas a um manipulador de arquivos</span><span class="sxs-lookup"><span data-stu-id="3746a-110">File-access and other properties associated with a file handler</span></span>
-   <span data-ttu-id="3746a-111">Códigos de quatro caracteres identificando os tipos de fluxo que um manipulador de fluxo pode processar</span><span class="sxs-lookup"><span data-stu-id="3746a-111">Four-character codes identifying stream types that a stream handler can process</span></span>

<span data-ttu-id="3746a-112">A biblioteca AVIFile consulta o registro de manipuladores que são externos a um aplicativo ao abrir arquivos e acessar fluxos.</span><span class="sxs-lookup"><span data-stu-id="3746a-112">The AVIFile library queries the registry for handlers that are external to an application when opening files and accessing streams.</span></span> <span data-ttu-id="3746a-113">O resultado de uma consulta bem-sucedida retorna o FileName de um manipulador que pode processar o arquivo ou o tipo de fluxo especificado na consulta.</span><span class="sxs-lookup"><span data-stu-id="3746a-113">The result of a successful query returns the filename of a handler that can process the file or stream type specified in the query.</span></span> <span data-ttu-id="3746a-114">O registro lista cada manipulador criando três entradas que têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="3746a-114">The registry lists each handler by creating three entries that have the following form:</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



<span data-ttu-id="3746a-115">Essas entradas consistem nas seguintes partes.</span><span class="sxs-lookup"><span data-stu-id="3746a-115">These entries consist of the following parts.</span></span>



| <span data-ttu-id="3746a-116">Parte</span><span class="sxs-lookup"><span data-stu-id="3746a-116">Part</span></span>                                   | <span data-ttu-id="3746a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3746a-117">Description</span></span>                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3746a-118">\_raiz de classes hKey \_</span><span class="sxs-lookup"><span data-stu-id="3746a-118">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="3746a-119">Identifica a entrada raiz do registro.</span><span class="sxs-lookup"><span data-stu-id="3746a-119">Identifies the root entry of the registry.</span></span>                                                                                                                                               |
| <span data-ttu-id="3746a-120">Clsid</span><span class="sxs-lookup"><span data-stu-id="3746a-120">Clsid</span></span>                                  | <span data-ttu-id="3746a-121">Identifica essa entrada como um identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="3746a-121">Identifies this entry as a class identifier.</span></span>                                                                                                                                             |
| <span data-ttu-id="3746a-122">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="3746a-122">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="3746a-123">Especifica um identificador de interface (IID) ou identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="3746a-123">Specifies an interface identifier (IID) or class identifier.</span></span> <span data-ttu-id="3746a-124">Esse valor é um identificador exclusivo de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="3746a-124">This value is a unique 16-byte identifier.</span></span> <span data-ttu-id="3746a-125">(O identificador também pode ser referido como um GUID ou um UUID em outros manuais.)</span><span class="sxs-lookup"><span data-stu-id="3746a-125">(The identifier might also be referred to as a GUID or a UUID in other manuals.)</span></span> |
| <span data-ttu-id="3746a-126">Leitor/gravador de arquivo Wave</span><span class="sxs-lookup"><span data-stu-id="3746a-126">Wave File reader/writer</span></span>                | <span data-ttu-id="3746a-127">Especifica uma cadeia de caracteres para descrever o manipulador.</span><span class="sxs-lookup"><span data-stu-id="3746a-127">Specifies a string to describe the handler.</span></span> <span data-ttu-id="3746a-128">Essa cadeia de caracteres pode ser exibida em caixas de diálogo para selecionar manipuladores de fluxo e arquivo.</span><span class="sxs-lookup"><span data-stu-id="3746a-128">This string can be displayed in dialog boxes for selecting stream and file handlers.</span></span>                                                         |
| <span data-ttu-id="3746a-129">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="3746a-129">InProcServer32</span></span>                         | <span data-ttu-id="3746a-130">Especifica o arquivo (neste exemplo, WAVEFILE.DLL) que pode ser carregado para lidar com essa classe.</span><span class="sxs-lookup"><span data-stu-id="3746a-130">Specifies the file (in this example, WAVEFILE.DLL) that can be loaded to handle this class.</span></span>                                                                                              |
| <span data-ttu-id="3746a-131">AVIFile</span><span class="sxs-lookup"><span data-stu-id="3746a-131">AVIFile</span></span>                                | <span data-ttu-id="3746a-132">Especifica as propriedades de um manipulador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3746a-132">Specifies the properties of a file handler.</span></span> <span data-ttu-id="3746a-133">Neste exemplo, o manipulador pode ler e gravar em um arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="3746a-133">In this example, the handler can read and write to an AVI file.</span></span>                                                                              |



 

<span data-ttu-id="3746a-134">Um manipulador de arquivos pode ter uma ou mais de suas propriedades armazenadas no registro.</span><span class="sxs-lookup"><span data-stu-id="3746a-134">A file handler can have one or more of its properties stored in the registry.</span></span> <span data-ttu-id="3746a-135">As constantes a seguir identificam as propriedades atualmente associadas a um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3746a-135">The following constants identify the properties currently associated with a file.</span></span>



| <span data-ttu-id="3746a-136">Constante</span><span class="sxs-lookup"><span data-stu-id="3746a-136">Constant</span></span>                        | <span data-ttu-id="3746a-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="3746a-137">Description</span></span>                                                          |
|---------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="3746a-138">AVIFILEHANDLER \_ CANACCEPTNONRGB</span><span class="sxs-lookup"><span data-stu-id="3746a-138">AVIFILEHANDLER\_CANACCEPTNONRGB</span></span> | <span data-ttu-id="3746a-139">Indica que um manipulador de arquivo pode processar dados de imagem diferentes de RGB.</span><span class="sxs-lookup"><span data-stu-id="3746a-139">Indicates that a file handler can process image data other than RGB.</span></span> |
| <span data-ttu-id="3746a-140">AVIFILEHANDLER \_ CANread</span><span class="sxs-lookup"><span data-stu-id="3746a-140">AVIFILEHANDLER\_CANREAD</span></span>         | <span data-ttu-id="3746a-141">Indica que um manipulador de arquivo pode abrir um arquivo com acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="3746a-141">Indicates that a file handler can open a file with read access.</span></span>      |
| <span data-ttu-id="3746a-142">AVIFILEHANDLER \_ CANWRITE</span><span class="sxs-lookup"><span data-stu-id="3746a-142">AVIFILEHANDLER\_CANWRITE</span></span>        | <span data-ttu-id="3746a-143">Indica que um manipulador de arquivo pode abrir um arquivo com acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="3746a-143">Indicates that a file handler can open a file with write access.</span></span>     |



 

<span data-ttu-id="3746a-144">Ao criar um manipulador de arquivo ou fluxo, você pode obter um novo identificador executando UUIDGEN.EXE.</span><span class="sxs-lookup"><span data-stu-id="3746a-144">When creating a file or stream handler, you can obtain a new identifier by running UUIDGEN.EXE.</span></span> <span data-ttu-id="3746a-145">Sempre use UUIDGEN.EXE para criar um novo identificador.</span><span class="sxs-lookup"><span data-stu-id="3746a-145">Always use UUIDGEN.EXE to create a new identifier.</span></span> <span data-ttu-id="3746a-146">O número hexadecimal de 16 bytes criado por esse executável identificará exclusivamente seu manipulador.</span><span class="sxs-lookup"><span data-stu-id="3746a-146">The 16-byte hexadecimal number created by this executable will uniquely identify your handler.</span></span>

<span data-ttu-id="3746a-147">A biblioteca AVIFile usa entradas adicionais no registro para identificar um identificador de classe com base na extensão de arquivo que um manipulador de arquivo pode processar ou um código de quatro caracteres que um arquivo ou manipulador de fluxo pode processar.</span><span class="sxs-lookup"><span data-stu-id="3746a-147">The AVIFile library uses additional entries in the registry to identify a class identifier based on the file extension that a file handler can process or a four-character code that a file or stream handler can process.</span></span> <span data-ttu-id="3746a-148">Por exemplo, as entradas a seguir associam um identificador de classe à extensão de arquivo. WAV e o código de quatro caracteres "WAVE":</span><span class="sxs-lookup"><span data-stu-id="3746a-148">For example, the following entries associate a class identifier with the file extension .WAV and the four-character code "WAVE":</span></span>


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



<span data-ttu-id="3746a-149">Essas entradas consistem nas seguintes partes.</span><span class="sxs-lookup"><span data-stu-id="3746a-149">These entries consist of the following parts.</span></span>



| <span data-ttu-id="3746a-150">Parte</span><span class="sxs-lookup"><span data-stu-id="3746a-150">Part</span></span>                                   | <span data-ttu-id="3746a-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="3746a-151">Description</span></span>                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3746a-152">\_raiz de classes hKey \_</span><span class="sxs-lookup"><span data-stu-id="3746a-152">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="3746a-153">Identifica a entrada raiz do registro.</span><span class="sxs-lookup"><span data-stu-id="3746a-153">Identifies the root entry of the registry.</span></span>                                                        |
| <span data-ttu-id="3746a-154">AVIFile</span><span class="sxs-lookup"><span data-stu-id="3746a-154">AVIFile</span></span>                                | <span data-ttu-id="3746a-155">Identifica essa entrada como uma entrada usada pelo AVIFile.</span><span class="sxs-lookup"><span data-stu-id="3746a-155">Identifies this entry as an entry used by AVIFile.</span></span>                                                |
| <span data-ttu-id="3746a-156">Extensões do</span><span class="sxs-lookup"><span data-stu-id="3746a-156">Extensions</span></span>                             | <span data-ttu-id="3746a-157">Especifica a extensão de arquivo (neste exemplo,. WAV) que um manipulador de arquivo pode processar.</span><span class="sxs-lookup"><span data-stu-id="3746a-157">Specifies the file extension (in this example, .WAV) that a file handler can process.</span></span>             |
| <span data-ttu-id="3746a-158">RIFFHandlers</span><span class="sxs-lookup"><span data-stu-id="3746a-158">RIFFHandlers</span></span>                           | <span data-ttu-id="3746a-159">Especifica o código de quatro caracteres (neste exemplo, "WAVE") que um arquivo ou manipulador de fluxo pode processar.</span><span class="sxs-lookup"><span data-stu-id="3746a-159">Specifies the four-character code (in this example, "WAVE") a file or stream handler can process.</span></span> |
| <span data-ttu-id="3746a-160">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="3746a-160">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="3746a-161">Especifica um identificador de interface (IID) ou identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="3746a-161">Specifies an interface identifier (IID) or class identifier.</span></span>                                      |



 

<span data-ttu-id="3746a-162">Se você distribuir o fluxo ou o manipulador de arquivos sem um aplicativo de instalação para instalá-lo no sistema do usuário, deverá incluir um. O arquivo REG para que o usuário possa instalar o manipulador.</span><span class="sxs-lookup"><span data-stu-id="3746a-162">If you distribute your stream or file handler without a setup application to install it in the user's system, you must include a .REG file so the user can install the handler.</span></span> <span data-ttu-id="3746a-163">O usuário usará o editor do registro para criar entradas de registro para o seu manipulador de fluxo ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="3746a-163">The user will use the registry editor to create registry entries for your stream or file handler.</span></span>

<span data-ttu-id="3746a-164">O exemplo a seguir mostra o conteúdo de um típico. Arquivo REG.</span><span class="sxs-lookup"><span data-stu-id="3746a-164">The following example shows the contents of a typical .REG file.</span></span> <span data-ttu-id="3746a-165">A primeira entrada no exemplo a seguir é a cadeia de caracteres descritiva para o manipulador.</span><span class="sxs-lookup"><span data-stu-id="3746a-165">The first entry in the following example is the descriptive string for the handler.</span></span> <span data-ttu-id="3746a-166">A segunda entrada identifica o arquivo que contém o manipulador.</span><span class="sxs-lookup"><span data-stu-id="3746a-166">The second entry identifies the file containing the handler.</span></span> <span data-ttu-id="3746a-167">A terceira entrada identifica as propriedades do manipulador de arquivo (nesse caso, acesso somente leitura aos arquivos).</span><span class="sxs-lookup"><span data-stu-id="3746a-167">The third entry identifies the properties of the file handler (in this case, read-only access to files).</span></span> <span data-ttu-id="3746a-168">A quarta entrada associa o tipo de arquivo que o manipulador processa (nesse caso, arquivos com um. Extensão de nome de arquivo JPG) com o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="3746a-168">The fourth entry associates the type of file the handler processes (in this case, files with a .JPG filename extension) with the class identifier.</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



<span data-ttu-id="3746a-169">Ao criar esse arquivo, salve-o com um. REG Extension para identificá-lo como um arquivo de atualização para o registro.</span><span class="sxs-lookup"><span data-stu-id="3746a-169">When creating this file, save it with a .REG extension to identify it as an update file for the registry.</span></span> <span data-ttu-id="3746a-170">Além disso, substitua um IID exclusivo pelo código de 16 bytes usado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="3746a-170">Also, substitute a unique IID for the 16-byte code used in the example.</span></span>

 

 




