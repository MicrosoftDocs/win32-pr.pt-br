---
description: Um ícone personalizado deve ser atribuído a um tipo de arquivo para fornecer uma indicação visual ao usuário desse tipo de arquivo ou ao aplicativo ao qual o tipo de arquivo está associado.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Como atribuir um ícone personalizado a um tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967917"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a><span data-ttu-id="f8ee0-103">Como atribuir um ícone personalizado a um tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="f8ee0-103">How to Assign a Custom Icon to a File Type</span></span>

<span data-ttu-id="f8ee0-104">Quando nenhum ícone padrão personalizado é atribuído a um tipo de arquivo, a área de trabalho e o Windows Explorer exibem todos os arquivos desse tipo com um ícone padrão genérico.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-104">When no custom default icon is assigned to a file type, the desktop and Windows Explorer display all files of that type with a generic default icon.</span></span> <span data-ttu-id="f8ee0-105">Por exemplo, a captura de tela a seguir mostra esse ícone padrão usado com o arquivo MyDocs4. MYP.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-105">For example, the following screen shot shows this default icon used with the MyDocs4.myp file.</span></span>

![captura de tela do ícone padrão](images/icon.png)

<span data-ttu-id="f8ee0-107">Embora todos os arquivos exibidos nesta captura de tela sejam arquivos de texto simples, somente MyDocs4. MYP exibe o ícone padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-107">While all the files displayed in this screen shot are simple text files, only MyDocs4.myp displays the Windows default icon.</span></span> <span data-ttu-id="f8ee0-108">Isso ocorre porque a extensão. txt é um tipo de arquivo registrado que tem um ícone padrão personalizado.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-108">This is because the .txt extension is a registered file type that has a custom default icon.</span></span>

<span data-ttu-id="f8ee0-109">A captura de tela a seguir mostra um ícone personalizado que foi atribuído ao tipo de arquivo. MYP.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-109">The following screen shot shows a custom icon that has been assigned to the .myp file type.</span></span>

![captura de tela do ícone personalizado para arquivos. MYP](images/context4.png)

> [!Note]  
> <span data-ttu-id="f8ee0-111">Os ícones também podem ser atribuídos de acordo com uma base específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-111">Icons can also be assigned on an application-specific basis.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="f8ee0-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="f8ee0-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="f8ee0-113">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="f8ee0-113">Step 1:</span></span>

<span data-ttu-id="f8ee0-114">Crie uma subchave chamada **DefaultIcon** em um dos dois locais a seguir:</span><span class="sxs-lookup"><span data-stu-id="f8ee0-114">Create a subkey named **DefaultIcon** in one of the following two locations:</span></span>

-   <span data-ttu-id="f8ee0-115">Para uma atribuição de tipo de arquivo, **HKEY \_ classes \_ raiz** \\ *. Extension*</span><span class="sxs-lookup"><span data-stu-id="f8ee0-115">For a file-type assignment, **HKEY\_CLASSES\_ROOT**\\ *.extension*</span></span>
-   <span data-ttu-id="f8ee0-116">Para uma atribuição de aplicativo, **HKEY \_ classes \_ raiz** \\ *ProgID*</span><span class="sxs-lookup"><span data-stu-id="f8ee0-116">For an application assignment, **HKEY\_CLASSES\_ROOT**\\*ProgID*</span></span>

### <a name="step-2"></a><span data-ttu-id="f8ee0-117">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="f8ee0-117">Step 2:</span></span>

<span data-ttu-id="f8ee0-118">Atribua a subchave **DefaultIcon** a um valor padrão do tipo **reg \_ sz** que especifica o caminho totalmente qualificado para o arquivo que contém o ícone.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-118">Assign the **DefaultIcon** subkey a default value of type **REG\_SZ** that specifies the fully qualified path for the file that contains the icon.</span></span>

### <a name="step-3"></a><span data-ttu-id="f8ee0-119">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="f8ee0-119">Step 3:</span></span>

<span data-ttu-id="f8ee0-120">Chame a função [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para notificar o Shell para atualizar seu cache de ícone.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-120">Call the [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) function to notify the Shell to update its icon cache.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ee0-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8ee0-121">Remarks</span></span>

<span data-ttu-id="f8ee0-122">O exemplo a seguir mostra uma exibição detalhada das entradas do registro que são necessárias para uma atribuição de ícone de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-122">The following example shows a detailed view of the registry entries that are required for a file-type icon assignment.</span></span> <span data-ttu-id="f8ee0-123">A extensão de nome de arquivo é associada a um aplicativo, mas a atribuição de ícone é a própria extensão de nome de arquivo para que o aplicativo associado não dite o ícone padrão.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-123">The file name extension is associated with an application, but the icon assignment is to the file name extension itself so that the associated application does not dictate the default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="f8ee0-124">O exemplo a seguir mostra uma exibição detalhada das entradas do registro que são necessárias para uma atribuição de ícone de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-124">The following example shows a detailed view of the registry entries that are required for an application icon assignment.</span></span> <span data-ttu-id="f8ee0-125">A extensão de nome de arquivo. MYP é associada primeiro ao aplicativo myprogram. 1.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-125">The .myp file name extension is first associated with the MyProgram.1 application.</span></span> <span data-ttu-id="f8ee0-126">A subchave myprogram. 1 ProgID é então atribuída ao ícone padrão personalizado.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-126">The MyProgram.1 ProgID subkey is then assigned the custom default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="f8ee0-127">Qualquer arquivo que contenha um ícone é aceitável, incluindo arquivos. ico,. exe e. dll.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-127">Any file that contains an icon is acceptable, including .ico, .exe, and .dll files.</span></span> <span data-ttu-id="f8ee0-128">Se houver mais de um ícone no arquivo, o caminho deverá ser seguido por uma vírgula e, em seguida, o índice do ícone.</span><span class="sxs-lookup"><span data-stu-id="f8ee0-128">If there is more than one icon in the file, the path should be followed by a comma, and then the index of the icon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8ee0-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8ee0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8ee0-130">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="f8ee0-130">File Types</span></span>](fa-file-types.md)
</dt> </dl>

 

 



