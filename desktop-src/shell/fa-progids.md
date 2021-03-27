---
description: O Shell usa uma subchave do registro ProgID (identificador programático) para associar um tipo de arquivo a um aplicativo e controlar o comportamento da associação.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificadores programáticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988740"
---
# <a name="programmatic-identifiers"></a><span data-ttu-id="148c1-103">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="148c1-103">Programmatic Identifiers</span></span>

<span data-ttu-id="148c1-104">O Shell usa uma subchave do registro ProgID (identificador programático) para associar um tipo de arquivo a um aplicativo e controlar o comportamento da associação.</span><span class="sxs-lookup"><span data-stu-id="148c1-104">The Shell uses a programmatic identifier (ProgID) registry subkey to associate a file type with an application, and to control the behavior of the association.</span></span> <span data-ttu-id="148c1-105">As entradas de ProgID usadas para associações de arquivo estão localizadas na **\_ \_ raiz de classes hKey** no registro.</span><span class="sxs-lookup"><span data-stu-id="148c1-105">The ProgID entries used for file associations are located under **HKEY\_CLASSES\_ROOT** in the registry.</span></span>

<span data-ttu-id="148c1-106">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="148c1-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="148c1-107">Elementos de identificador programático usados por associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="148c1-107">Programmatic Identifier Elements Used by File Associations</span></span>](#programmatic-identifier-elements-used-by-file-associations)
-   [<span data-ttu-id="148c1-108">Usando identificadores programáticos com versão</span><span class="sxs-lookup"><span data-stu-id="148c1-108">Using Versioned Programmatic Identifiers</span></span>](#using-versioned-programmatic-identifiers)
-   [<span data-ttu-id="148c1-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="148c1-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="148c1-110">Para obter informações adicionais, leia [como registrar um tipo de arquivo para um novo aplicativo](how-to-register-a-file-type-for-a-new-application.md)</span><span class="sxs-lookup"><span data-stu-id="148c1-110">For additional information, read [How To Register a File Type for a New Application](how-to-register-a-file-type-for-a-new-application.md)</span></span>

## <a name="programmatic-identifier-elements-used-by-file-associations"></a><span data-ttu-id="148c1-111">Elementos de identificador programático usados por associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="148c1-111">Programmatic Identifier Elements Used by File Associations</span></span>

<span data-ttu-id="148c1-112">O formato apropriado de um nome de chave ProgID é \[ *fornecedor ou aplicativo* \] . \[ Do *componente* \] . \[ *Versão* \] , separada por pontos e sem espaços, como em Word.Document. 6.</span><span class="sxs-lookup"><span data-stu-id="148c1-112">The proper format of a ProgID key name is \[*Vendor or Application*\].\[*Component*\].\[*Version*\], separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="148c1-113">A parte da *versão* é opcional, mas altamente recomendável.</span><span class="sxs-lookup"><span data-stu-id="148c1-113">The *Version* portion is optional but strongly recommended.</span></span> <span data-ttu-id="148c1-114">Para obter mais informações, consulte [usando identificadores programáticos com versão](#using-versioned-programmatic-identifiers).</span><span class="sxs-lookup"><span data-stu-id="148c1-114">For more information, see [Using Versioned Programmatic Identifiers](#using-versioned-programmatic-identifiers).</span></span>

<span data-ttu-id="148c1-115">Uma subchave ProgID deve incluir os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="148c1-115">A ProgID subkey should include the following elements.</span></span> <span data-ttu-id="148c1-116">Observe que alguns dados de cadeia de caracteres nesta chave exigem formatação específica.</span><span class="sxs-lookup"><span data-stu-id="148c1-116">Note that some string data in this key requires specific formatting.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="148c1-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="148c1-117">Element</span></span></th>
<th><span data-ttu-id="148c1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="148c1-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="148c1-119"><strong>Os</strong></span><span class="sxs-lookup"><span data-stu-id="148c1-119"><strong>(Default)</strong></span></span></td>
<td><span data-ttu-id="148c1-120">Defina a entrada padrão da subchave ProgID para um nome amigável para esse ProgID, adequado para exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="148c1-120">Set the default entry of the ProgID subkey to a friendly name for that ProgID, suitable to display to the user.</span></span> <span data-ttu-id="148c1-121">O uso dessa entrada para manter o nome amigável é preterido pela entrada FriendlyTypeName em sistemas que executam o Windows 2000 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="148c1-121">The use of this entry to hold the friendly name is deprecated by the FriendlyTypeName entry on systems running Windows 2000 or later.</span></span> <span data-ttu-id="148c1-122">No entanto, você deve definir esse valor para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="148c1-122">However, you should set this value for backward compatibility.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="148c1-123"><strong>AllowSilentDefaultTakeOver</strong> (introduzido no Windows 8)</span><span class="sxs-lookup"><span data-stu-id="148c1-123"><strong>AllowSilentDefaultTakeOver</strong> (introduced in Windows 8)</span></span></td>
<td><span data-ttu-id="148c1-124">Defina essa entrada opcional para sinalizar que o Windows deve ignorar esse ProgID ao determinar um manipulador padrão para um tipo de arquivo público.</span><span class="sxs-lookup"><span data-stu-id="148c1-124">Set this optional entry to signal that Windows should ignore this ProgID when determining a default handler for a public file type.</span></span> <span data-ttu-id="148c1-125">Independentemente de esse valor ser definido, o ProgID continua a aparecer no menu de atalho OpenWith e na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="148c1-125">Regardless of whether this value is set, the ProgID continues to appear in the OpenWith shortcut menu and dialog.</span></span> <span data-ttu-id="148c1-126">Esse é um valor REG_NONE.</span><span class="sxs-lookup"><span data-stu-id="148c1-126">This is a REG_NONE value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="148c1-127"><strong>AppUserModelID</strong> (introduzido no Windows 7)</span><span class="sxs-lookup"><span data-stu-id="148c1-127"><strong>AppUserModelID</strong> (introduced in Windows 7)</span></span></td>
<td><span data-ttu-id="148c1-128">Defina essa entrada opcional para a ID do modelo de usuário do aplicativo explícito do aplicativo (AppUserModelID) se o aplicativo usar um AppUserModelID explícito e usar as listas de saltos <strong>recentes</strong> ou <strong>frequentes</strong> automaticamente geradas pelo sistema ou fornecer uma lista de atalhos personalizada.</span><span class="sxs-lookup"><span data-stu-id="148c1-128">Set this optional entry to the application's explicit Application User Model ID (AppUserModelID) if the application uses an explicit AppUserModelID and uses either the system's automatically generated <strong>Recent</strong> or <strong>Frequent</strong> Jump Lists or provides a custom Jump List.</span></span> <span data-ttu-id="148c1-129">Se um aplicativo usar um AppUserModelID explícito e não definir esse valor, os itens não serão exibidos nas listas de atalhos desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="148c1-129">If an application uses an explicit AppUserModelID and does not set this value, items will not appear in that application's Jump Lists.</span></span> <span data-ttu-id="148c1-130">Esta é uma cadeia de caracteres REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="148c1-130">This is a REG_SZ string.</span></span> <span data-ttu-id="148c1-131">Para obter mais informações, consulte <a href="appids.md">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</a>.</span><span class="sxs-lookup"><span data-stu-id="148c1-131">For more information, see <a href="appids.md">Application User Model IDs (AppUserModelIDs)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="148c1-132"><strong>EditFlags</strong></span><span class="sxs-lookup"><span data-stu-id="148c1-132"><strong>EditFlags</strong></span></span></td>
<td><span data-ttu-id="148c1-133">Defina essa entrada opcional usando sinalizadores da enumeração <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="148c1-133">Set this optional entry using flags from the <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> enumeration.</span></span> <span data-ttu-id="148c1-134">A entrada EditFlags controla alguns aspectos da manipulação do Shell dos tipos de arquivo vinculados a esse ProgID.</span><span class="sxs-lookup"><span data-stu-id="148c1-134">The EditFlags entry controls some aspects of the Shell's handling of the file types linked to this ProgID.</span></span> <span data-ttu-id="148c1-135">Você também pode usar a entrada EditFlags para limitar o quanto o usuário pode modificar determinados aspectos desses tipos de arquivo usando a folha de propriedades de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="148c1-135">You can also use the EditFlags entry to limit how much the user can modify certain aspects of these file types using a file's property sheet.</span></span> <span data-ttu-id="148c1-136">Os valores de <strong>FILETYPEATTRIBUTEFLAGS</strong> usados para EditFlags são valores binários projetados de forma que você possa combinar vários atributos em um único valor em uma operação OR de bits.</span><span class="sxs-lookup"><span data-stu-id="148c1-136">The <strong>FILETYPEATTRIBUTEFLAGS</strong> values used for EditFlags are binary values designed so that you can combine multiple attributes into a single value in a bitwise OR operation.</span></span> <span data-ttu-id="148c1-137">Este é um valor REG_DWORD ou REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="148c1-137">This is a REG_DWORD or REG_BINARY value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="148c1-138"><strong>FriendlyTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="148c1-138"><strong>FriendlyTypeName</strong></span></span></td>
<td><span data-ttu-id="148c1-139">Defina essa entrada como um nome amigável para o ProgID, adequado para exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="148c1-139">Set this entry to a friendly name for the ProgID, suitable to display to the user.</span></span> <span data-ttu-id="148c1-140">Para consistência, essa cadeia de caracteres deve conter os mesmos dados que a entrada padrão para essa chave de ProgID.</span><span class="sxs-lookup"><span data-stu-id="148c1-140">For consistency, this string should contain the same data as the Default entry for this ProgID key.</span></span> <span data-ttu-id="148c1-141">Essa entrada pode ser uma cadeia de caracteres REG_SZ ou REG_EXPAND_SZ, mas deve ser formatada como uma cadeia de caracteres indireta (um nome de arquivo totalmente qualificado e um valor de recurso precedido pelo símbolo @), por exemplo <em>@% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="148c1-141">This entry can be either a REG_SZ or REG_EXPAND_SZ string, but it must be formatted as an indirect string (a fully qualified file name and resource value preceded by the @ symbol), for instance <em>@%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="148c1-142"><strong>InfoTip</strong></span><span class="sxs-lookup"><span data-stu-id="148c1-142"><strong>InfoTip</strong></span></span></td>
<td><span data-ttu-id="148c1-143">Defina essa entrada como uma breve mensagem de ajuda que o Shell exibe para este ProgID.</span><span class="sxs-lookup"><span data-stu-id="148c1-143">Set this entry to a brief help message that the Shell displays for this ProgID.</span></span> <span data-ttu-id="148c1-144">A entrada InfoTip é exibida em uma caixa de diálogo do mouse sobre.</span><span class="sxs-lookup"><span data-stu-id="148c1-144">The InfoTip entry displays in a mouse-over dialog box.</span></span> <span data-ttu-id="148c1-145">Esse valor pode ser uma cadeia de caracteres REG_SZ ou REG_EXPAND_SZ, mas, como FriendlyTypeName, deve ser formatado como uma cadeia de caracteres indireta.</span><span class="sxs-lookup"><span data-stu-id="148c1-145">This value can be either a REG_SZ or REG_EXPAND_SZ string but, like FriendlyTypeName, it must be formatted as an indirect string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="148c1-146"><strong>CurVer</strong></span><span class="sxs-lookup"><span data-stu-id="148c1-146"><strong>CurVer</strong></span></span></td>
<td><span data-ttu-id="148c1-147">Defina a entrada (padrão) dessa subchave para a versão mais atual deste ProgID.</span><span class="sxs-lookup"><span data-stu-id="148c1-147">Set the (Default) entry of this subkey to the most current version of this ProgID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="148c1-148">A menos que você tenha versões de aplicativo lado a lado, ou seja, várias versões instaladas no mesmo sistema, você deve evitar usar a <strong>curva</strong>.</span><span class="sxs-lookup"><span data-stu-id="148c1-148">Unless you have side-by-side application versions, that is, multiple versions installed on the same system, you should avoid using <strong>CurVer</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="148c1-149"><strong>DefaultIcon</strong>.</span><span class="sxs-lookup"><span data-stu-id="148c1-149"><strong>DefaultIcon</strong>.</span></span></td>
<td><span data-ttu-id="148c1-150">Defina a entrada (padrão) dessa subchave para o ícone padrão que você deseja exibir para os tipos de arquivo associados a este ProgID.</span><span class="sxs-lookup"><span data-stu-id="148c1-150">Set the (Default) entry of this subkey to the default icon that you want to display for file types associated with this ProgID.</span></span> <span data-ttu-id="148c1-151">Esse valor pode ser uma cadeia de caracteres REG_SZ ou REG_EXPAND_SZ, mas deve ser fornecido como um nome de arquivo totalmente qualificado com seu valor de recurso de atendente, por exemplo <em>% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="148c1-151">This value can be either a REG_SZ or REG_EXPAND_SZ string, but it must be provided as a fully qualified file name with its attendant resource value, for instance <em>%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="148c1-152">O exemplo de chave do registro a seguir ilustra um nó de chave ProgID de associação de arquivo:</span><span class="sxs-lookup"><span data-stu-id="148c1-152">The following registry key example illustrates a file association ProgID key node:</span></span>

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a><span data-ttu-id="148c1-153">Usando identificadores programáticos com versão</span><span class="sxs-lookup"><span data-stu-id="148c1-153">Using Versioned Programmatic Identifiers</span></span>

<span data-ttu-id="148c1-154">Um ProgID com versão é aquele cuja versão é indicada em seu nome.</span><span class="sxs-lookup"><span data-stu-id="148c1-154">A versioned ProgID is one whose version is indicated in its name.</span></span> <span data-ttu-id="148c1-155">Normalmente, você faz isso adicionando um ponto e o número de versão ao nome.</span><span class="sxs-lookup"><span data-stu-id="148c1-155">You typically do this by adding a period and the version number to the name.</span></span> <span data-ttu-id="148c1-156">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="148c1-156">For example:</span></span>

-   <span data-ttu-id="148c1-157">Word.Document. 6</span><span class="sxs-lookup"><span data-stu-id="148c1-157">Word.Document.6</span></span>
-   <span data-ttu-id="148c1-158">Word.Document. 8</span><span class="sxs-lookup"><span data-stu-id="148c1-158">Word.Document.8</span></span>

<span data-ttu-id="148c1-159">Essas são ProgIDs com versão, com as versões 6 e 8, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="148c1-159">These are versioned ProgIDs, with versions 6 and 8 respectively.</span></span> <span data-ttu-id="148c1-160">Se você tiver um aplicativo lado a lado, ou seja, um que dê suporte a várias versões do seu aplicativo instalado ao mesmo tempo, use ProgIDs e versões independentes de versão.</span><span class="sxs-lookup"><span data-stu-id="148c1-160">If you have a side-by-side application, that is, one that supports multiple versions of your application installed at the same time, then use CurVer and Version Independent ProgIDs.</span></span> <span data-ttu-id="148c1-161">Caso contrário, ProgIDs e versões independentes de versão devem ser evitadas, pois elas resultarão em ineficiência.</span><span class="sxs-lookup"><span data-stu-id="148c1-161">Otherwise, CurVer and Version Independent ProgIDs should be avoided because they will lead to inefficiency.</span></span>

## <a name="related-topics"></a><span data-ttu-id="148c1-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="148c1-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="148c1-163">Como registrar um tipo de arquivo para um novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="148c1-163">How To Register a File Type for a New Application</span></span>](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[<span data-ttu-id="148c1-164">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="148c1-164">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="148c1-165">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="148c1-165">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="148c1-166">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="148c1-166">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="148c1-167">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="148c1-167">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="148c1-168">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="148c1-168">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="148c1-169">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="148c1-169">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="148c1-170">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="148c1-170">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="148c1-171">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="148c1-171">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 




