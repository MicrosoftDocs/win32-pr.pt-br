---
description: Este tópico explica como criar novos tipos de arquivo e como associar seu aplicativo ao tipo de arquivo e a outros tipos de arquivo bem definidos.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967948"
---
# <a name="file-types"></a><span data-ttu-id="fc822-103">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-103">File Types</span></span>

<span data-ttu-id="fc822-104">Este tópico explica como criar novos tipos de arquivo e como associar seu aplicativo ao tipo de arquivo e a outros tipos de arquivo bem definidos.</span><span class="sxs-lookup"><span data-stu-id="fc822-104">This topic explains how to create new file types and how to associate your app with your file type and other well-defined file types.</span></span> <span data-ttu-id="fc822-105">Arquivos com uma extensão de nome de arquivo comum compartilhada (. doc,. html e assim por diante) são do mesmo *tipo*.</span><span class="sxs-lookup"><span data-stu-id="fc822-105">Files with a shared common file name extension (.doc, .html, and so on) are of the same *type*.</span></span> <span data-ttu-id="fc822-106">Por exemplo, se você criar um novo editor de texto, poderá usar o tipo de arquivo. txt existente.</span><span class="sxs-lookup"><span data-stu-id="fc822-106">For example, if you create a new text editor, then you can use the existing .txt file type.</span></span> <span data-ttu-id="fc822-107">Em outros casos, talvez seja necessário criar um novo tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc822-107">In other cases, you might need to create a new file type.</span></span>

<span data-ttu-id="fc822-108">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fc822-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="fc822-109">Tipos de arquivos públicos e privados</span><span class="sxs-lookup"><span data-stu-id="fc822-109">Public and Private File Types</span></span>](#public-and-private-file-types)
-   [<span data-ttu-id="fc822-110">Registrando um tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-110">Registering a File Type</span></span>](#registering-a-file-type)
    -   [<span data-ttu-id="fc822-111">Definindo subchaves opcionais e atributos de extensão de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-111">Setting Optional Subkeys and File Type Extension Attributes</span></span>](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [<span data-ttu-id="fc822-112">Excluindo informações do registro durante a desinstalação</span><span class="sxs-lookup"><span data-stu-id="fc822-112">Deleting Registry Information During Uninstallation</span></span>](#deleting-registry-information-during-uninstallation)
-   [<span data-ttu-id="fc822-113">Tipos de arquivo que dão suporte a metadados abertos</span><span class="sxs-lookup"><span data-stu-id="fc822-113">File Types That Support Open Metadata</span></span>](#file-types-that-support-open-metadata)
-   [<span data-ttu-id="fc822-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc822-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="fc822-115">Informações adicionais podem ser encontradas nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="fc822-115">Additional information can be found on the following topics:</span></span>

-   [<span data-ttu-id="fc822-116">Como escolher uma extensão de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-116">How To Choose a File Type Extension</span></span>](how-to-choose-a-file-type-extension.md)
-   [<span data-ttu-id="fc822-117">Como definir atributos de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-117">How To Define File Type Attributes</span></span>](./how-to-define-file-type-attributes.md)
-   [<span data-ttu-id="fc822-118">Como incluir um aplicativo na caixa de diálogo abrir com</span><span class="sxs-lookup"><span data-stu-id="fc822-118">How To Include an Application on the Open with Dialog Box</span></span>](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [<span data-ttu-id="fc822-119">Como excluir um aplicativo da caixa de diálogo abrir com para tipos de arquivo não associados</span><span class="sxs-lookup"><span data-stu-id="fc822-119">How To Exclude an Application from the Open with Dialog Box for Unassociated File Types</span></span>](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a><span data-ttu-id="fc822-120">Tipos de arquivos públicos e privados</span><span class="sxs-lookup"><span data-stu-id="fc822-120">Public and Private File Types</span></span>

<span data-ttu-id="fc822-121">Os tipos de arquivo públicos também são conhecidos como tipos populares ou contenciosos porque os aplicativos concorrentes podem querer ser associados a esses tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc822-121">Public file types are also known as popular or contentious types because competing applications might want to be associated with these file types.</span></span> <span data-ttu-id="fc822-122">As características dos tipos de arquivo públicos incluem:</span><span class="sxs-lookup"><span data-stu-id="fc822-122">Characteristics of public file types include:</span></span>

-   <span data-ttu-id="fc822-123">Normalmente, eles são definidos por órgãos de padrões e/ou são promovidos por suas organizações de definição como formatos de intercâmbio.</span><span class="sxs-lookup"><span data-stu-id="fc822-123">They are typically defined by standards bodies, and/or are promoted by their defining organizations as interchange formats.</span></span>
-   <span data-ttu-id="fc822-124">Muitas vezes, eles são trocados entre computadores e usuários para fins diferentes.</span><span class="sxs-lookup"><span data-stu-id="fc822-124">They are often exchanged between computers and users for diverse purposes.</span></span>
-   <span data-ttu-id="fc822-125">Eles precisam ter suporte em várias plataformas diferentes.</span><span class="sxs-lookup"><span data-stu-id="fc822-125">They need to be supported on many different platforms.</span></span>
-   <span data-ttu-id="fc822-126">É provável que os aplicativos de vários fornecedores os manipulem.</span><span class="sxs-lookup"><span data-stu-id="fc822-126">Applications from multiple vendors are likely to handle them.</span></span>

<span data-ttu-id="fc822-127">Alguns exemplos de tipos de arquivo que são considerados públicos são os tipos de arquivo de imagem. png,. gif,. jpg e. bmp, e os tipos de áudio. wav,. mp3 e. au.</span><span class="sxs-lookup"><span data-stu-id="fc822-127">Some examples of file types that are considered public are the image file types .png, .gif, .jpg, and .bmp, and the audio types .wav, .mp3, and .au.</span></span>

<span data-ttu-id="fc822-128">Ao contrário dos tipos de arquivos públicos, os tipos de arquivos privados ou proprietários normalmente têm um formato que é implementado e compreendido por apenas um aplicativo ou fornecedor.</span><span class="sxs-lookup"><span data-stu-id="fc822-128">Unlike public file types, private or proprietary file types typically have a format that is implemented and understood by only one application or vendor.</span></span> <span data-ttu-id="fc822-129">Como resultado, os tipos de arquivo privados normalmente não são propensos a conflitos entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fc822-129">As a result, private file types are typically not prone to conflicts between applications.</span></span> <span data-ttu-id="fc822-130">Alguns tipos de arquivo podem ser iniciados como tipos de arquivo privados, mas posteriormente se tornam tipos de arquivo públicos.</span><span class="sxs-lookup"><span data-stu-id="fc822-130">Some file types can start as private file types but later become public file types.</span></span>

> [!Note]  
> <span data-ttu-id="fc822-131">O Windows não diferencia os tipos de arquivo público e privado.</span><span class="sxs-lookup"><span data-stu-id="fc822-131">Windows does not differentiate between public and private file types.</span></span> <span data-ttu-id="fc822-132">A distinção é relevante apenas para tomar decisões sobre a escolha do registro de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc822-132">The distinction is relevant only in making decisions about your choice of file type registration.</span></span>

 

## <a name="registering-a-file-type"></a><span data-ttu-id="fc822-133">Registrando um tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-133">Registering a File Type</span></span>

<span data-ttu-id="fc822-134">Para associar o tipo de arquivo a um aplicativo existente, localize a ProgID do aplicativo no registro.</span><span class="sxs-lookup"><span data-stu-id="fc822-134">To associate the file type with an existing application, locate the application ProgID in the registry.</span></span> <span data-ttu-id="fc822-135">Para associar o tipo de arquivo a um novo aplicativo, defina um ProgID para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc822-135">To associate the file type with a new application, define a ProgID for your application.</span></span> <span data-ttu-id="fc822-136">Para obter informações sobre como definir um novo ProgID, consulte [identificadores programáticos](fa-progids.md).</span><span class="sxs-lookup"><span data-stu-id="fc822-136">For information about defining a new ProgID, see [Programmatic Identifiers](fa-progids.md).</span></span>

<span data-ttu-id="fc822-137">As subchaves de extensão de nome de arquivo têm o seguinte formato geral: ProgID de *extensão* = .</span><span class="sxs-lookup"><span data-stu-id="fc822-137">File name extension subkeys have the following general form: *extension*=*ProgID*.</span></span> <span data-ttu-id="fc822-138">As subchaves de extensão de nome de arquivo são armazenadas na subárvore **\_ \_ raiz de classes hKey** .</span><span class="sxs-lookup"><span data-stu-id="fc822-138">File name extension subkeys are stored in the **HKEY\_CLASSES\_ROOT** subtree.</span></span>

<span data-ttu-id="fc822-139">É importante incluir o ponto à esquerda (.) ao criar subchaves de tipo de arquivo no registro.</span><span class="sxs-lookup"><span data-stu-id="fc822-139">It is important to include the leading period (.) when creating file type subkeys in the registry.</span></span> <span data-ttu-id="fc822-140">Por exemplo, se você quiser um tipo de arquivo com a extensão curta. MYP e a extensão longa. MYP-arquivo a ser aberto com um aplicativo chamado myprogram, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="fc822-140">For example, if you want a file type with the short extension .myp and the long extension .myp-file to be opened with an application called MyProgram, use the following syntax:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

<span data-ttu-id="fc822-141">Conforme demonstrado no exemplo anterior, se você também registrar uma extensão de nome de arquivo curto (. MYP), deverá criar uma subchave para a extensão longa (. MYP-File) também.</span><span class="sxs-lookup"><span data-stu-id="fc822-141">As demonstrated in the preceding example, if you also register a short file name extension (.myp), you should create a subkey for the long extension (.myp-file) as well.</span></span> <span data-ttu-id="fc822-142">Para obter mais informações, consulte [manipuladores de tipo de arquivo](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="fc822-142">For more information, see [File Type Handlers](fa-file-extensions.md).</span></span>

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a><span data-ttu-id="fc822-143">Definindo subchaves opcionais e atributos de extensão de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-143">Setting Optional Subkeys and File Type Extension Attributes</span></span>

<span data-ttu-id="fc822-144">As entradas de extensão de tipo de arquivo no registro têm várias subchaves e atributos opcionais.</span><span class="sxs-lookup"><span data-stu-id="fc822-144">File type extension entries in the registry have several optional subkeys and attributes.</span></span>

<span data-ttu-id="fc822-145">As entradas de extensão de tipo de arquivo usadas por associações de arquivo são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc822-145">The file type extension entries that are used by file associations are described in the following table.</span></span> <span data-ttu-id="fc822-146">Todos os valores são do tipo **reg \_ sz** .</span><span class="sxs-lookup"><span data-stu-id="fc822-146">All values are of the **REG\_SZ** type.</span></span>



| <span data-ttu-id="fc822-147">Entrada de registro</span><span class="sxs-lookup"><span data-stu-id="fc822-147">Registry entry</span></span>  | <span data-ttu-id="fc822-148">Ação</span><span class="sxs-lookup"><span data-stu-id="fc822-148">Action</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc822-149">Padrão</span><span class="sxs-lookup"><span data-stu-id="fc822-149">Default</span></span>         | <span data-ttu-id="fc822-150">Defina o valor padrão da subchave de extensão para o ProgID ao qual ela está vinculada.</span><span class="sxs-lookup"><span data-stu-id="fc822-150">Set the default value of the extension subkey to the ProgID to which it is linked.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fc822-151">Tipo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="fc822-151">Content Type</span></span>    | <span data-ttu-id="fc822-152">Defina o valor do tipo de conteúdo como o tipo de conteúdo MIME do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc822-152">Set the Content Type value to the file type's MIME content type.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="fc822-153">OpenWithList</span><span class="sxs-lookup"><span data-stu-id="fc822-153">OpenWithList</span></span>    | <span data-ttu-id="fc822-154">Não use.</span><span class="sxs-lookup"><span data-stu-id="fc822-154">Do not use.</span></span> <span data-ttu-id="fc822-155">Essa subchave contém uma ou mais subchaves de aplicativo para aplicativos que aparecem na entrada da caixa de diálogo **abrir com** para o tipo de arquivo e destina-se apenas a aplicativos. exe em sistemas operacionais anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc822-155">This subkey contains one or more application subkeys for applications that appear in the **Open with** dialog box entry for the file type and is intended only for .exe applications on operating systems prior to Windows XP.</span></span> <span data-ttu-id="fc822-156">Use OpenWithProgIds em vez disso.</span><span class="sxs-lookup"><span data-stu-id="fc822-156">Use OpenWithProgIds instead.</span></span>                                                            |
| <span data-ttu-id="fc822-157">OpenWithProgIds</span><span class="sxs-lookup"><span data-stu-id="fc822-157">OpenWithProgIds</span></span> | <span data-ttu-id="fc822-158">Essa subchave contém uma lista de ProgIDs alternativos para esse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc822-158">This subkey contains a list of alternate ProgIDs for this file type.</span></span> <span data-ttu-id="fc822-159">Os programas para esses ProgIDs aparecem no menu **abrir com** e estão disponíveis como aplicativos padrão da Windows Store para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc822-159">The programs for these ProgIDs appear in the **Open with** menu and are available as default Windows Store apps for the file type.</span></span> <span data-ttu-id="fc822-160">Sempre que um aplicativo assumir esse tipo de arquivo alterando o valor padrão, ele também deverá adicionar uma entrada a essa lista.</span><span class="sxs-lookup"><span data-stu-id="fc822-160">Whenever an application takes over this file type by changing the default value, it should also add an entry to this list.</span></span> |
| <span data-ttu-id="fc822-161">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="fc822-161">PerceivedType</span></span>   | <span data-ttu-id="fc822-162">Defina o valor percebido como o percebido ao qual o arquivo pertence, se houver.</span><span class="sxs-lookup"><span data-stu-id="fc822-162">Set the PerceivedType value to the PerceivedType to which the file belongs, if any.</span></span> <span data-ttu-id="fc822-163">Essa cadeia de caracteres não é usada pelas versões do Windows anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc822-163">This string is not used by Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="fc822-164">Para obter mais informações, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="fc822-164">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>                                                                           |



 

<span data-ttu-id="fc822-165">A forma geral de uma subchave de extensão de nome de arquivo é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="fc822-165">The general form of a file name extension subkey is as follows.</span></span> <span data-ttu-id="fc822-166">Todos os tipos de entrada são do tipo **reg \_ sz** .</span><span class="sxs-lookup"><span data-stu-id="fc822-166">All entry types are of the **REG\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

<span data-ttu-id="fc822-167">Considerações importantes sobre tipos de arquivo incluem:</span><span class="sxs-lookup"><span data-stu-id="fc822-167">Important considerations about file types include:</span></span>

-   <span data-ttu-id="fc822-168">A subárvore **\_ \_ raiz de classes hKey** é uma exibição formada pela mesclagem do **HKEY \_ Current \_ User** \\ **software** \\ **classes** e o **HKEY \_ local \_ Machine** \\ **software** \\ **classes**</span><span class="sxs-lookup"><span data-stu-id="fc822-168">The **HKEY\_CLASSES\_ROOT** subtree is a view formed by merging **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** and **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes**</span></span>
-   <span data-ttu-id="fc822-169">Em geral, **a \_ \_ raiz de classes hKey** deve ser lida, mas não gravada.</span><span class="sxs-lookup"><span data-stu-id="fc822-169">In general, **HKEY\_CLASSES\_ROOT** is intended to be read from but not written to.</span></span> <span data-ttu-id="fc822-170">Para obter mais informações, consulte o artigo [ \_ \_ raiz de classes hKey](../sysinfo/hkey-classes-root-key.md) .</span><span class="sxs-lookup"><span data-stu-id="fc822-170">For more information, see the [HKEY\_CLASSES\_ROOT](../sysinfo/hkey-classes-root-key.md) article.</span></span>
-   <span data-ttu-id="fc822-171">Para registrar um tipo de arquivo globalmente em um computador específico, crie uma entrada para o tipo de arquivo na subchave **HKEY \_ local \_ Machine** \\ **software** \\ **classes** .</span><span class="sxs-lookup"><span data-stu-id="fc822-171">To register a file type globally on a particular computer, create an entry for the file type in the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="fc822-172">Para tornar um registro de tipo de arquivo visível somente para o usuário atual, crie uma entrada para o tipo de arquivo na subchave **HKEY \_ Current \_ User** \\ **software** \\ **classes** .</span><span class="sxs-lookup"><span data-stu-id="fc822-172">To make a file type registration visible to the current user only, create an entry for the file type in the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="fc822-173">Um aplicativo pode fornecer sua própria implementação de um verbo, como Open ou Play, conforme mostrado no exemplo de registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc822-173">An application can provide its own implementation of a verb, such as open or play, as shown in the following registry example.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    <span data-ttu-id="fc822-174">Subchaves da subchave Verb incluem a linha de comando e o método Drop target: **Command** e **DropTarget**.</span><span class="sxs-lookup"><span data-stu-id="fc822-174">Subkeys of the verb subkey include the command line and the drop target method: **command** and **DropTarget**.</span></span>

-   <span data-ttu-id="fc822-175">Quando você cria ou altera uma associação de arquivo, é importante notificar o sistema de que você fez uma alteração.</span><span class="sxs-lookup"><span data-stu-id="fc822-175">When you create or change a file association, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="fc822-176">Faça isso chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) e especificando o evento **SHCNE \_ assocchanged** .</span><span class="sxs-lookup"><span data-stu-id="fc822-176">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) and specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="fc822-177">Se você não chamar **SHChangeNotify**, a alteração poderá não ser reconhecida até que o sistema seja reinicializado.</span><span class="sxs-lookup"><span data-stu-id="fc822-177">If you do not call **SHChangeNotify**, the change may not be recognized until after the system is rebooted.</span></span>
-   <span data-ttu-id="fc822-178">Para recuperar informações de registro sobre uma associação de arquivo, use a interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="fc822-178">To retrieve registry information regarding a file association, use the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface.</span></span> <span data-ttu-id="fc822-179">Para ver um cenário que ilustra esse procedimento, consulte [exemplo de associação de arquivo](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="fc822-179">For a scenario that illustrates this procedure, see [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

> [!Note]  
> <span data-ttu-id="fc822-180">As subchaves de registro de **aplicativos** e **caminhos de aplicativo** são usadas para registrar e controlar o comportamento do sistema em nome dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fc822-180">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="fc822-181">Para obter informações mais detalhadas sobre essa funcionalidade, consulte [registro de aplicativo](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="fc822-181">For more detailed information about this functionality, see [Application Registration](app-registration.md).</span></span>

 

### <a name="deleting-registry-information-during-uninstallation"></a><span data-ttu-id="fc822-182">Excluindo informações do registro durante a desinstalação</span><span class="sxs-lookup"><span data-stu-id="fc822-182">Deleting Registry Information During Uninstallation</span></span>

<span data-ttu-id="fc822-183">Ao desinstalar um aplicativo, os ProgIDs e a maioria das outras informações de registro associadas a esse aplicativo devem ser excluídos como parte da desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fc822-183">When uninstalling an application, the ProgIDs and most other registry information associated with that application should be deleted as part of the uninstallation.</span></span> <span data-ttu-id="fc822-184">No entanto, os aplicativos que assumiram a propriedade de um tipo de arquivo (definindo o valor padrão da subchave **HKEY \_ classes \_ raiz**. Extension do tipo de arquivo \\  para o ProgID do aplicativo) não devem tentar remover esse valor ao desinstalar o.</span><span class="sxs-lookup"><span data-stu-id="fc822-184">However, applications that have taken ownership of a file type (by setting the Default value of the file type's **HKEY\_CLASSES\_ROOT**\\ *.extension* subkey to the ProgID of the application) should not attempt to remove that value when uninstalling.</span></span> <span data-ttu-id="fc822-185">Deixar os dados em vigor para o valor padrão evita a dificuldade de determinar se outro aplicativo assumiu a propriedade do tipo de arquivo e substituiu o valor padrão após a instalação do aplicativo original.</span><span class="sxs-lookup"><span data-stu-id="fc822-185">Leaving the data in place for the Default value avoids the difficulty of determining whether another application has taken ownership of the file type and overwritten the Default value after the original application was installed.</span></span> <span data-ttu-id="fc822-186">O Windows respeita o valor padrão somente se o ProgID encontrado há um ProgID registrado.</span><span class="sxs-lookup"><span data-stu-id="fc822-186">Windows respects the Default value only if the ProgID found there is a registered ProgID.</span></span> <span data-ttu-id="fc822-187">Se o ProgID tiver o registro cancelado, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="fc822-187">If the ProgID is unregistered, it is ignored.</span></span>

<span data-ttu-id="fc822-188">Observe que outras informações de propriedade de tipo de arquivo são armazenadas na subárvore **\_ atual do \_ usuário do hKey** e também são usadas somente quando o aplicativo ao qual ele faz referência é registrado.</span><span class="sxs-lookup"><span data-stu-id="fc822-188">Note that other file-type ownership information is stored in the **HKEY\_CURRENT\_USER** subtree and also is used only when the application that it references is registered.</span></span> <span data-ttu-id="fc822-189">Portanto, esses dados não precisam ser removidos durante a desinstalação de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc822-189">Therefore, this data does not need to be removed when uninstalling an application.</span></span>

<span data-ttu-id="fc822-190">Por exemplo, o seguinte mostra o estado do registro antes de um aplicativo ser desinstalado:</span><span class="sxs-lookup"><span data-stu-id="fc822-190">As an example, the following shows the state of the registry before an application is uninstalled:</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

<span data-ttu-id="fc822-191">O seguinte mostra o estado dessas mesmas entradas de registro depois que o aplicativo é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="fc822-191">The following shows the state of those same registry entries after the application has been uninstalled.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a><span data-ttu-id="fc822-192">Tipos de arquivo que dão suporte a metadados abertos</span><span class="sxs-lookup"><span data-stu-id="fc822-192">File Types That Support Open Metadata</span></span>

<span data-ttu-id="fc822-193">No Windows 7 e posterior, os seguintes tipos de arquivo dão suporte a metadados abertos.</span><span class="sxs-lookup"><span data-stu-id="fc822-193">In Windows 7 and later, the following file types support open metadata.</span></span>



| <span data-ttu-id="fc822-194">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-194">File type</span></span>                                                               | <span data-ttu-id="fc822-195">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-195">File name extensions</span></span>                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fc822-196">Documentos do Office 2007</span><span class="sxs-lookup"><span data-stu-id="fc822-196">Office 2007 Documents</span></span>                                                   | <span data-ttu-id="fc822-197">. docx,. xlsx,. pptx</span><span class="sxs-lookup"><span data-stu-id="fc822-197">.docx, .xlsx, .pptx</span></span>                                           |
| <span data-ttu-id="fc822-198">Documentos do Office 97-2003</span><span class="sxs-lookup"><span data-stu-id="fc822-198">Office 97-2003 Documents</span></span>                                                | <span data-ttu-id="fc822-199">. doc,. xls,. ppt</span><span class="sxs-lookup"><span data-stu-id="fc822-199">.doc, .xls, .ppt</span></span>                                              |
| <span data-ttu-id="fc822-200">Pesquisa Salva</span><span class="sxs-lookup"><span data-stu-id="fc822-200">Saved Search</span></span>                                                            | <span data-ttu-id="fc822-201">. Search-MS</span><span class="sxs-lookup"><span data-stu-id="fc822-201">.search-ms</span></span>                                                    |
| <span data-ttu-id="fc822-202">Formatos baseados no Windows Media (ASF (Advanced Streaming Format))</span><span class="sxs-lookup"><span data-stu-id="fc822-202">Windows Media-based formats (Advanced Streaming Format (ASF) container)</span></span> | <span data-ttu-id="fc822-203">. wmv,. WMA</span><span class="sxs-lookup"><span data-stu-id="fc822-203">.wmv, .wma</span></span>                                                    |
| <span data-ttu-id="fc822-204">MP4 (manipulador de propriedade)</span><span class="sxs-lookup"><span data-stu-id="fc822-204">MP4 (property handler)</span></span>                                                  | <span data-ttu-id="fc822-205">. MP4,. M4A,. m4v,. MP4V,. M4P,. M4B,. 3GP,. 3GPP,. 3GP2,. mov</span><span class="sxs-lookup"><span data-stu-id="fc822-205">.mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fc822-206">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc822-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc822-207">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="fc822-207">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="fc822-208">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-208">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="fc822-209">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="fc822-209">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="fc822-210">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-210">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="fc822-211">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc822-211">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="fc822-212">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="fc822-212">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="fc822-213">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="fc822-213">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="fc822-214">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="fc822-214">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
