---
description: As associações de arquivo definem como o Shell trata um tipo de arquivo no sistema.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Como funcionam as associações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169449"
---
# <a name="how-file-associations-work"></a><span data-ttu-id="6201b-103">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-103">How File Associations Work</span></span>

<span data-ttu-id="6201b-104">As associações de arquivo definem como o Shell trata um [tipo de arquivo](fa-file-types.md) no sistema.</span><span class="sxs-lookup"><span data-stu-id="6201b-104">File associations define how the Shell treats a [file type](fa-file-types.md) on the system.</span></span>

<span data-ttu-id="6201b-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6201b-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6201b-106">Sobre associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-106">About File Associations</span></span>](#about-file-associations)
-   [<span data-ttu-id="6201b-107">Quando você deve implementar ou modificar associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-107">When You Should Implement or Modify File Associations</span></span>](#when-you-should-implement-or-modify-file-associations)
-   [<span data-ttu-id="6201b-108">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-108">How File Associations Work</span></span>](#how-file-associations-work)
-   [<span data-ttu-id="6201b-109">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="6201b-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="6201b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6201b-110">Related topics</span></span>](#related-topics)

## <a name="about-file-associations"></a><span data-ttu-id="6201b-111">Sobre associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-111">About File Associations</span></span>

<span data-ttu-id="6201b-112">As associações de arquivo controlam a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="6201b-112">File associations control the following functionality:</span></span>

-   <span data-ttu-id="6201b-113">Qual aplicativo é iniciado quando um usuário clica duas vezes em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6201b-113">Which application launches when a user double-clicks a file.</span></span>
-   <span data-ttu-id="6201b-114">Qual ícone aparece para um arquivo por padrão.</span><span class="sxs-lookup"><span data-stu-id="6201b-114">Which icon appears for a file by default.</span></span>
-   <span data-ttu-id="6201b-115">Como o tipo de arquivo aparece quando exibido no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="6201b-115">How the file type appears when viewed in Windows Explorer.</span></span>
-   <span data-ttu-id="6201b-116">Quais comandos aparecem no menu de atalho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6201b-116">Which commands appear in a file's shortcut menu.</span></span>
-   <span data-ttu-id="6201b-117">Outros recursos de interface do usuário, como dicas de ferramenta, informações de bloco e o painel detalhes.</span><span class="sxs-lookup"><span data-stu-id="6201b-117">Other UI features, such as tooltips, tile info, and the details pane.</span></span>

<span data-ttu-id="6201b-118">Os desenvolvedores de aplicativos podem usar associações de arquivos para controlar como o Shell trata tipos de arquivo personalizados ou para associar um aplicativo a tipos de arquivo existentes.</span><span class="sxs-lookup"><span data-stu-id="6201b-118">Application developers can use file associations to control how the Shell treats custom file types, or to associate an application with existing file types.</span></span> <span data-ttu-id="6201b-119">Por exemplo, quando um aplicativo é instalado, o aplicativo pode verificar a presença de associações de arquivo existentes e criar ou substituir essas associações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6201b-119">For example, when an application is installed, the application can check for the presence of existing file associations, and either create or override those file associations.</span></span>

<span data-ttu-id="6201b-120">Os usuários podem controlar alguns aspectos das associações de arquivo para personalizar como o Shell trata um tipo de arquivo usando a interface do usuário **abrir com** ou editando o registro.</span><span class="sxs-lookup"><span data-stu-id="6201b-120">Users can control some aspects of file associations to customize how the Shell treats a file type either by using the **Open With** UI, or editing the registry.</span></span>

<span data-ttu-id="6201b-121">Na janela do Windows Explorer mostrada na captura de tela abaixo, o Shell exibe ícones diferentes para cada arquivo, com base no ícone associado ao tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6201b-121">In the Windows Explorer window shown in the screen shot below, the Shell displays different icons for each file, based on the icon associated with the file type.</span></span> <span data-ttu-id="6201b-122">Se o usuário clicar duas vezes na **imagem de bitmap de exemplo** de arquivo, o Shell iniciará o Paint e o usará para abrir o arquivo porque, nesse sistema, o Paint será associado a arquivos. bmp.</span><span class="sxs-lookup"><span data-stu-id="6201b-122">If the user double-clicks the file **Sample Bitmap Image**, the Shell launches Paint and uses it to open the file because on this system, Paint is associated with .bmp files.</span></span> <span data-ttu-id="6201b-123">As pessoas podem controlar essas ações usando associações de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6201b-123">People can control these actions using file associations.</span></span>

![ilustração de como as associações de arquivo funcionam na prática](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a><span data-ttu-id="6201b-125">Quando você deve implementar ou modificar associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-125">When You Should Implement or Modify File Associations</span></span>

<span data-ttu-id="6201b-126">Os aplicativos podem usar arquivos para várias finalidades: alguns arquivos são usados exclusivamente pelo aplicativo e, normalmente, não são acessados por usuários, enquanto outros arquivos são criados pelo usuário e são frequentemente abertos, pesquisados e exibidos no Shell.</span><span class="sxs-lookup"><span data-stu-id="6201b-126">Applications can use files for various purposes: some files are used exclusively by the application, and are not typically accessed by users, while other files are created by the user and are often opened, searched for, and viewed from the Shell.</span></span>

<span data-ttu-id="6201b-127">A menos que o tipo de arquivo personalizado seja usado exclusivamente pelo aplicativo, você deve implementar associações de arquivo para ele.</span><span class="sxs-lookup"><span data-stu-id="6201b-127">Unless your custom file type is used exclusively by the application, you should implement file associations for it.</span></span> <span data-ttu-id="6201b-128">Como regra geral, implemente as associações de arquivo para o tipo de arquivo personalizado se você espera que o usuário interaja diretamente com esses arquivos de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="6201b-128">As a general rule, implement file associations for your custom file type if you expect the user to interact directly with these files in any way.</span></span> <span data-ttu-id="6201b-129">Isso inclui o uso do Shell para procurar e abrir os arquivos, pesquisar o conteúdo ou as propriedades dos arquivos e visualizar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="6201b-129">That includes using the Shell to browse and open the files, searching the content or properties of the files, and previewing the files.</span></span>

<span data-ttu-id="6201b-130">Se seu aplicativo estiver manipulando um tipo de arquivo existente, não modifique a associação de arquivo, a menos que você queira modificar a maneira como o Shell manipula todos os arquivos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="6201b-130">If your application is handling an existing file type, do not modify the file association unless you want to modify the way the Shell handles all files of this type.</span></span>

## <a name="how-file-associations-work"></a><span data-ttu-id="6201b-131">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-131">How File Associations Work</span></span>

<span data-ttu-id="6201b-132">Os arquivos são expostos no Shell como itens de Shell.</span><span class="sxs-lookup"><span data-stu-id="6201b-132">Files are exposed in the Shell as Shell items.</span></span> <span data-ttu-id="6201b-133">Para controlar as associações de arquivos, os desenvolvedores de aplicativos podem registrar um mapeamento entre o tipo de arquivo e os manipuladores (objetos COM que fornecem funcionalidade para os itens de shell do tipo de arquivo).</span><span class="sxs-lookup"><span data-stu-id="6201b-133">To control file associations, application developers can register a mapping between the file type and the handlers (COM objects that provide functionality for the file type's Shell items).</span></span> <span data-ttu-id="6201b-134">Quando o Shell precisa consultar as associações de arquivo de um tipo de arquivo, ele cria uma matriz de chaves do registro contendo as associações para o tipo de arquivo e verifica essas chaves para que as associações de arquivo apropriadas sejam usadas.</span><span class="sxs-lookup"><span data-stu-id="6201b-134">When the Shell needs to query for the file associations of a file type, it creates an array of registry keys containing the associations for the file type, and checks these keys for the appropriate file associations to use.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6201b-135">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="6201b-135">Additional Resources</span></span>

-   <span data-ttu-id="6201b-136">Para obter um plano de fundo conceitual sobre associações de arquivo, consulte [visão geral de verbos e associações de arquivo](fa-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="6201b-136">For conceptual background on file associations, see [Overview of Verbs and File Associations](fa-verbs.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6201b-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6201b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6201b-138">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6201b-138">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="6201b-139">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-139">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="6201b-140">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="6201b-140">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="6201b-141">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-141">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="6201b-142">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="6201b-142">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="6201b-143">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="6201b-143">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="6201b-144">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="6201b-144">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="6201b-145">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="6201b-145">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



