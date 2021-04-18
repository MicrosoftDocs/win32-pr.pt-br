---
description: Neste exemplo de C \# , um formulário de papel foi examinado como um arquivo PNG (Portable Network Graphics) e especificado como a imagem de plano de fundo em tempo de execução para um controle InkPicture. O exemplo usa uma caixa de mensagem para exibir resultados de reconhecimento de manuscrito.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Exemplo de formulário de papel digitalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780686"
---
# <a name="scanned-paper-form-sample"></a><span data-ttu-id="afb08-104">Exemplo de formulário de papel digitalizado</span><span class="sxs-lookup"><span data-stu-id="afb08-104">Scanned Paper Form Sample</span></span>

<span data-ttu-id="afb08-105">Neste exemplo de C \# , um formulário de papel foi examinado como um arquivo PNG (Portable Network Graphics) e especificado como a imagem de plano de fundo em tempo de execução para um controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="afb08-105">In this C\# sample, a paper form has been scanned as a Portable Network Graphics (PNG) file and specified as the background image at run time for a [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span> <span data-ttu-id="afb08-106">O exemplo usa uma caixa de mensagem para exibir resultados de reconhecimento de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="afb08-106">The sample uses a message box to display handwriting recognition results.</span></span>

<span data-ttu-id="afb08-107">O exemplo inclui um arquivo linguagem XML (XML), Formdata.xml.</span><span class="sxs-lookup"><span data-stu-id="afb08-107">The sample includes an Extensible Markup Language (XML) file, Formdata.xml.</span></span> <span data-ttu-id="afb08-108">O arquivo XML contém o nome do arquivo PNG.</span><span class="sxs-lookup"><span data-stu-id="afb08-108">The XML file contains the name of the PNG file.</span></span> <span data-ttu-id="afb08-109">Ele também contém `FieldInfo` elementos que definem regiões retangulares no formulário em que um usuário pode inserir tinta.</span><span class="sxs-lookup"><span data-stu-id="afb08-109">It also contains `FieldInfo` elements that define rectangular regions on the form where a user can enter ink.</span></span> <span data-ttu-id="afb08-110">As informações no `FieldInfo` elemento são mostradas no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="afb08-110">The information in the `FieldInfo` element is shown in the following example:</span></span>


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



<span data-ttu-id="afb08-111">Os elementos esquerdo, superior, direito e inferior são definições de coordenadas de pixel para cada campo.</span><span class="sxs-lookup"><span data-stu-id="afb08-111">The Left, Top, Right, and Bottom elements are definitions of pixel coordinates for each field.</span></span>

<span data-ttu-id="afb08-112">O exemplo inicializa um novo [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) com os dados contidos no Formdata.xml:</span><span class="sxs-lookup"><span data-stu-id="afb08-112">The sample initializes a new [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) with the data contained in Formdata.xml:</span></span>


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



<span data-ttu-id="afb08-113">A imagem do formulário especificada em Formdata.xml é carregada como o plano de fundo do controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="afb08-113">The form image specified in Formdata.xml is loaded as the background of the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



<span data-ttu-id="afb08-114">A coleta de tinta é então habilitada para o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="afb08-114">Ink collection is then enabled for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a><span data-ttu-id="afb08-115">Manipuladores de eventos de menu</span><span class="sxs-lookup"><span data-stu-id="afb08-115">Menu Event Handlers</span></span>

<span data-ttu-id="afb08-116">O aplicativo inclui manipuladores de eventos de clique para todos os menus exibidos ao longo da parte superior do formulário.</span><span class="sxs-lookup"><span data-stu-id="afb08-116">The application includes click event handlers for all of the menus displayed along the top of the form.</span></span>

### <a name="recognize-menu-item"></a><span data-ttu-id="afb08-117">Reconhecer item de menu</span><span class="sxs-lookup"><span data-stu-id="afb08-117">Recognize Menu Item</span></span>

<span data-ttu-id="afb08-118">O manipulador de eventos de clique do menu reconhecer desabilita a coleta de tinta para o controle e verifica se há um reconhecedor de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="afb08-118">The Recognize menu click event handler disables ink collection for the control and checks for a handwriting recognizer.</span></span> <span data-ttu-id="afb08-119">Se nenhum reconhecedor estiver instalado, uma caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="afb08-119">If no recognizer is installed, a dialog box is displayed.</span></span> <span data-ttu-id="afb08-120">Um usuário deve clicar na opção de menu tinta ou caneta para reabilitar o controle para entrada à tinta.</span><span class="sxs-lookup"><span data-stu-id="afb08-120">A user must then click the Ink or Pen menu option to re-enable the control for ink input.</span></span>

<span data-ttu-id="afb08-121">Se um reconhecedor estiver instalado, a `Recognize` função recuperará os dados XML que especificam coordenadas de pixel para cada campo de formulário.</span><span class="sxs-lookup"><span data-stu-id="afb08-121">If a recognizer is installed, the `Recognize` function retrieves the XML data that specifies pixel coordinates for each form field.</span></span> <span data-ttu-id="afb08-122">As coordenadas são convertidas em coordenadas de espaço à tinta e um retângulo é definido para cada campo de formulário.</span><span class="sxs-lookup"><span data-stu-id="afb08-122">The coordinates are converted to ink space coordinates, and a rectangle is defined for each form field.</span></span> <span data-ttu-id="afb08-123">Depois que os retângulos são definidos, a função localiza os traços que interseccionam e ficam dentro de cada retângulo.</span><span class="sxs-lookup"><span data-stu-id="afb08-123">After rectangles are defined, the function finds the strokes that intersect and lie within each rectangle.</span></span> <span data-ttu-id="afb08-124">Por fim, ele executa o reconhecimento na tinta e exibe os resultados em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="afb08-124">Finally, it performs recognition on the ink and displays the results in a message box.</span></span>

### <a name="ink-menu-item"></a><span data-ttu-id="afb08-125">Item de menu de tinta</span><span class="sxs-lookup"><span data-stu-id="afb08-125">Ink Menu Item</span></span>

<span data-ttu-id="afb08-126">O manipulador de eventos de clique do menu de tinta habilita o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="afb08-126">The Ink menu click event handler enables the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span>

### <a name="pen-menu-item"></a><span data-ttu-id="afb08-127">Item de menu da caneta</span><span class="sxs-lookup"><span data-stu-id="afb08-127">Pen Menu Item</span></span>

<span data-ttu-id="afb08-128">O manipulador de eventos de clique no menu de caneta executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="afb08-128">The Pen menu click event handler performs the following tasks:</span></span>

-   <span data-ttu-id="afb08-129">Desabilita a coleta de tinta para o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) (que é necessário antes de alterar a propriedade [EditingMode](/previous-versions/ms582189(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="afb08-129">Disables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control (which is necessary before changing the [EditingMode](/previous-versions/ms582189(v=vs.100)) property).</span></span>
-   <span data-ttu-id="afb08-130">Define a propriedade [EditingMode](/previous-versions/ms582189(v=vs.100)) para coletar tinta.</span><span class="sxs-lookup"><span data-stu-id="afb08-130">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to collect ink.</span></span>
-   <span data-ttu-id="afb08-131">Habilita novamente a coleta de tinta para o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) e alterna os menus de caneta, seleção e borracha para indicar o modo ativo.</span><span class="sxs-lookup"><span data-stu-id="afb08-131">Re-enables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control and toggles the Pen, Select, and Eraser menus to indicate the active mode.</span></span>

### <a name="edit-menu-item"></a><span data-ttu-id="afb08-132">Editar item de menu</span><span class="sxs-lookup"><span data-stu-id="afb08-132">Edit Menu Item</span></span>

<span data-ttu-id="afb08-133">O menu Editar manipulador de eventos de clique é semelhante ao manipulador de eventos de menu de caneta.</span><span class="sxs-lookup"><span data-stu-id="afb08-133">The Edit menu click event handler is similar to the Pen menu event handler.</span></span> <span data-ttu-id="afb08-134">Ele executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="afb08-134">It performs the following tasks:</span></span>

-   <span data-ttu-id="afb08-135">Desabilita a coleta de tinta.</span><span class="sxs-lookup"><span data-stu-id="afb08-135">Disables ink collection.</span></span>
-   <span data-ttu-id="afb08-136">Define a propriedade [EditingMode](/previous-versions/ms582189(v=vs.100)) a ser **selecionada**, o que permite que o usuário execute a seleção de tinta.</span><span class="sxs-lookup"><span data-stu-id="afb08-136">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to **Select**, which enables the user to perform ink selection.</span></span>
-   <span data-ttu-id="afb08-137">Habilita novamente a coleta de tinta e alterna os menus de caneta, de edição e de borracha para indicar o modo ativo.</span><span class="sxs-lookup"><span data-stu-id="afb08-137">Re-enables ink collection and toggles the Pen, Edit, and Eraser menus to indicate the active mode.</span></span>

### <a name="eraser-menu-item"></a><span data-ttu-id="afb08-138">Item de menu de borracha</span><span class="sxs-lookup"><span data-stu-id="afb08-138">Eraser Menu Item</span></span>

<span data-ttu-id="afb08-139">O menu de borracha clique no [manipulador de eventos](/previous-versions/ms582189(v=vs.100)) define o controle [inkpicturemode](/previous-versions/aa514604(v=msdn.10)) para **excluir**, que permite que um usuário apague a tinta.</span><span class="sxs-lookup"><span data-stu-id="afb08-139">The Eraser menu click event handler sets the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control [EditingMode](/previous-versions/ms582189(v=vs.100)) to **Delete**, which enables a user to erase ink.</span></span> <span data-ttu-id="afb08-140">Ele também alterna os itens de menu caneta, editar e borracha.</span><span class="sxs-lookup"><span data-stu-id="afb08-140">It also toggles the Pen, Edit, and Eraser menu items.</span></span>

### <a name="clear-menu-item"></a><span data-ttu-id="afb08-141">Limpar item de menu</span><span class="sxs-lookup"><span data-stu-id="afb08-141">Clear Menu Item</span></span>

<span data-ttu-id="afb08-142">O manipulador de eventos de clique de menu Limpar exclui a coleção de [traços](/previous-versions/ms552701(v=vs.100)) atuais para o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) , apagando, assim, toda a tinta no formulário.</span><span class="sxs-lookup"><span data-stu-id="afb08-142">The Clear menu click event handler deletes the current [Strokes](/previous-versions/ms552701(v=vs.100)) collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control, thereby erasing all of the ink on the form.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="afb08-143">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="afb08-143">Closing the Form</span></span>

<span data-ttu-id="afb08-144">No código gerado pelo Windows Form Designer, o controle [InkPicture](/previous-versions/aa514604(v=msdn.10)) é adicionado à lista de componentes do formulário quando o formulário é inicializado.</span><span class="sxs-lookup"><span data-stu-id="afb08-144">In the Windows Form Designer generated code, the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="afb08-145">Quando o formulário é fechado, o controle InkPicture é Descartado, bem como os outros componentes do formulário, pelo método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário.</span><span class="sxs-lookup"><span data-stu-id="afb08-145">When the form closes, the InkPicture control is disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afb08-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="afb08-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afb08-147">Controle InkEdit</span><span class="sxs-lookup"><span data-stu-id="afb08-147">InkEdit Control</span></span>](inkedit-control.md)
</dt> <dt>

[<span data-ttu-id="afb08-148">Controle InkPicture</span><span class="sxs-lookup"><span data-stu-id="afb08-148">InkPicture Control</span></span>](inkpicture-control.md)
</dt> </dl>

 

 
