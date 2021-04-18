---
description: Este exemplo baseia-se no exemplo de formulário de declarações automáticas integrando o objeto PenInputPanel. O exemplo está no diretório C \# PIPanel na pasta Autodeclarations.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Exemplo de PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781227"
---
# <a name="peninputpanel-sample"></a><span data-ttu-id="57fd7-104">Exemplo de PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="57fd7-104">PenInputPanel Sample</span></span>

<span data-ttu-id="57fd7-105">Este exemplo baseia-se no exemplo de formulário de declarações automáticas integrando o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="57fd7-105">This sample builds on the Auto Claims Form sample by integrating the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="57fd7-106">O exemplo está no diretório C \# PIPanel na pasta Autodeclarations.</span><span class="sxs-lookup"><span data-stu-id="57fd7-106">The sample is in the C\# PIPanel directory in the AutoClaims folder.</span></span>

> [!Note]  
> <span data-ttu-id="57fd7-107">Este exemplo requer que o sistema esteja equipado com um dispositivo de caneta.</span><span class="sxs-lookup"><span data-stu-id="57fd7-107">This sample requires that your system is equipped with a pen device.</span></span> <span data-ttu-id="57fd7-108">Se você estiver usando apenas um mouse (ou outro dispositivo de interface não-humana (HID)), o [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) não aparecerá.</span><span class="sxs-lookup"><span data-stu-id="57fd7-108">If you are using just a mouse (or other non-human interface device (HID) pointing device) the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) does not appear.</span></span>

 

<span data-ttu-id="57fd7-109">Para obter mais informações sobre o exemplo de formulário de declarações automáticas, consulte [exemplo de formulário de declarações automática](auto-claims-form-sample.md).</span><span class="sxs-lookup"><span data-stu-id="57fd7-109">For more information about the Auto Claims Form sample, see [Auto Claims Form Sample](auto-claims-form-sample.md).</span></span> <span data-ttu-id="57fd7-110">Para obter mais informações sobre o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , consulte [programando o painel de entrada usando a classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md).</span><span class="sxs-lookup"><span data-stu-id="57fd7-110">For more information about the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, see [Programming the Input Panel Using the PenInputPanel Class](programming-the-input-panel-using-the-peninputpanel-class.md).</span></span>

<span data-ttu-id="57fd7-111">No exemplo, o formulário de declarações automáticas contém cinco campos nos quais o usuário é solicitado a colocar as informações relevantes para a declaração: número da política, nome segurado, ano, marca e modelo do carro.</span><span class="sxs-lookup"><span data-stu-id="57fd7-111">In the sample, the Auto Claims Form contains five fields into which the user is asked to put information relevant to the claim: policy number, insured name, the year, make, and model of the car.</span></span> <span data-ttu-id="57fd7-112">Um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) é anexado a cada campo de entrada para fornecer um meio fácil de inserir valores com uma caneta.</span><span class="sxs-lookup"><span data-stu-id="57fd7-112">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is attached to each input field to provide an easy means for entering values with a pen.</span></span>

<span data-ttu-id="57fd7-113">Há duas técnicas para anexar um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) aos campos de entrada no formulário.</span><span class="sxs-lookup"><span data-stu-id="57fd7-113">There are two techniques for attaching a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to the input fields on your form.</span></span> <span data-ttu-id="57fd7-114">A primeira técnica é atribuir uma instância separada do objeto a cada campo de entrada em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="57fd7-114">The first technique is to assign a separate instance of the object to each input field at design time.</span></span> <span data-ttu-id="57fd7-115">A segunda é criar uma única instância do objeto e, em seguida, anexar essa instância de objeto em tempo de execução a um campo quando receber o foco.</span><span class="sxs-lookup"><span data-stu-id="57fd7-115">The second is to create a single instance of the object and then attach that object instance at run time to a field when it receives focus.</span></span> <span data-ttu-id="57fd7-116">Este exemplo demonstra as duas técnicas.</span><span class="sxs-lookup"><span data-stu-id="57fd7-116">This sample demonstrates both techniques.</span></span>

<span data-ttu-id="57fd7-117">Há compensações envolvidas na decisão de qual técnica usar.</span><span class="sxs-lookup"><span data-stu-id="57fd7-117">There are tradeoffs involved in deciding which technique to use.</span></span> <span data-ttu-id="57fd7-118">A criação de uma instância exclusiva do objeto para cada campo de formulário requer um pouco mais de memória quando o formulário é carregado.</span><span class="sxs-lookup"><span data-stu-id="57fd7-118">Creating a unique instance of the object for each form field requires slightly more memory when the form is loaded.</span></span> <span data-ttu-id="57fd7-119">No entanto, ele economiza ter que lidar com eventos de foco para os campos atribuir uma única instância ao campo atual em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="57fd7-119">However, it saves having to handle focus events for the fields to assign a single instance to the current field at run time.</span></span>

<span data-ttu-id="57fd7-120">Como o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tem suporte apenas em um Tablet PC, o exemplo cria os objetos PenInputPanel dentro de um bloco de tratamento de exceção.</span><span class="sxs-lookup"><span data-stu-id="57fd7-120">Because the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is supported only on a Tablet PC, the sample creates the PenInputPanel objects within an exception-handling block.</span></span>

## <a name="one-object-per-field"></a><span data-ttu-id="57fd7-121">Um objeto por campo</span><span class="sxs-lookup"><span data-stu-id="57fd7-121">One Object per Field</span></span>

<span data-ttu-id="57fd7-122">O exemplo demonstra a primeira técnica (um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) por campo) atribuindo os campos de entrada para número de política ( `inkEdPolicyNumber` ) e nome segurado ( `inkEdName` ) uma instância exclusiva do objeto PenInputPanel.</span><span class="sxs-lookup"><span data-stu-id="57fd7-122">The sample demonstrates the first technique (one [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object per field) by assigning the input fields for policy number (`inkEdPolicyNumber`) and insured name (`inkEdName`) a unique instance of the PenInputPanel object.</span></span> <span data-ttu-id="57fd7-123">Um construtor sobrecarregado para o objeto PenInputPanel pode pegar o nome do controle de entrada como um argumento, associando assim os controles.</span><span class="sxs-lookup"><span data-stu-id="57fd7-123">An overloaded constructor for the PenInputPanel object can take the name of the input control as an argument, thus associating the controls.</span></span> <span data-ttu-id="57fd7-124">As linhas a seguir do manipulador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário mostram:</span><span class="sxs-lookup"><span data-stu-id="57fd7-124">The following lines from the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler shows this:</span></span>


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a><span data-ttu-id="57fd7-125">Um objeto por formulário</span><span class="sxs-lookup"><span data-stu-id="57fd7-125">One Object per Form</span></span>

<span data-ttu-id="57fd7-126">A segunda técnica também é mostrada no exemplo: uma única instância de um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , `pipShared` , é compartilhada entre os campos de entrada year, Make e Model.</span><span class="sxs-lookup"><span data-stu-id="57fd7-126">The second technique is also shown in the sample: a single instance of a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, `pipShared`, is shared between the Year, Make, and Model input fields.</span></span> <span data-ttu-id="57fd7-127">O objeto compartilhado é criado usando o construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="57fd7-127">The shared object is created by using the default constructor.</span></span>


```C++
pipShared = new PenInputPanel();
```



<span data-ttu-id="57fd7-128">Usar essa técnica requer que seu formulário tenha apenas uma única instância do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="57fd7-128">Using this technique requires that your form have only a single instance of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="57fd7-129">Isso economiza memória, mas você deve adicionar código para manipular o evento quando um campo de entrada recebe o foco.</span><span class="sxs-lookup"><span data-stu-id="57fd7-129">This saves memory, but you must add code to handle the event when an input field receives focus.</span></span> <span data-ttu-id="57fd7-130">Quando um controle que usa uma instância compartilhada de um objeto PenInputPanel Obtém foco, defina a propriedade [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) do objeto PenInputPanel para esse controle.</span><span class="sxs-lookup"><span data-stu-id="57fd7-130">When a control that uses a shared instance of a PenInputPanel object gets focus, set the PenInputPanel object's [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) property to that control.</span></span> <span data-ttu-id="57fd7-131">O código a seguir mostra um manipulador de eventos para os eventos year, Make e Model Fields `Enter` .</span><span class="sxs-lookup"><span data-stu-id="57fd7-131">The following code shows an event handler for the Year, Make, and Model fields' `Enter` events.</span></span>


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



<span data-ttu-id="57fd7-132">Certifique-se de definir as propriedades que precisam ser definidas quando o foco é alterado para um novo controle.</span><span class="sxs-lookup"><span data-stu-id="57fd7-132">Be sure to set any properties that need to be set when focus changes to a new control.</span></span> <span data-ttu-id="57fd7-133">Nos manipuladores de eventos anteriores, por exemplo, a propriedade [factoname](/previous-versions/ms571978(v=vs.100)) é definida conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="57fd7-133">In the previous event handlers, for example, the [Factoid](/previous-versions/ms571978(v=vs.100)) property is set as appropriate.</span></span>

## <a name="usability-considerations"></a><span data-ttu-id="57fd7-134">Considerações sobre usabilidade</span><span class="sxs-lookup"><span data-stu-id="57fd7-134">Usability Considerations</span></span>

<span data-ttu-id="57fd7-135">Tenha em mente as seguintes considerações de usabilidade ao usar o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57fd7-135">Keep the following usability considerations in mind when using the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object in your application.</span></span>

### <a name="positioning-the-peninputpanel"></a><span data-ttu-id="57fd7-136">Posicionando o PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="57fd7-136">Positioning the PenInputPanel</span></span>

<span data-ttu-id="57fd7-137">Como os campos são dispostos verticalmente no formulário neste exemplo, a interface do usuário [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para cada controle de entrada está posicionada ligeiramente à direita do controle de entrada para facilitar o uso.</span><span class="sxs-lookup"><span data-stu-id="57fd7-137">Because the fields are laid out vertically on the form in this sample, the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) user interface for each input control is positioned slightly to the right of the input control to make it easier to use.</span></span> <span data-ttu-id="57fd7-138">Isso impede que o PenInputPanel cubra a próxima caixa de edição, facilitando o direcionamento da próxima caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="57fd7-138">This prevents the PenInputPanel from covering up the next edit box, making it easier to target the next edit box.</span></span>


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a><span data-ttu-id="57fd7-139">Selecionando o painel de entrada para exibição</span><span class="sxs-lookup"><span data-stu-id="57fd7-139">Selecting Input Panel to Display</span></span>

<span data-ttu-id="57fd7-140">Como os números de política geralmente são combinações de números, letras e outros caracteres, eles podem estar sujeitos a erros de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="57fd7-140">Because policy numbers are often combinations of numbers, letters, and other characters, they can be prone to recognition errors.</span></span> <span data-ttu-id="57fd7-141">Portanto, o exemplo define o painel padrão exibido pelo objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) como o teclado quando ele é anexado ao campo de número da política.</span><span class="sxs-lookup"><span data-stu-id="57fd7-141">Therefore, the sample sets the default panel displayed by the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to be the keyboard when it is attached to the policy number field.</span></span>


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



<span data-ttu-id="57fd7-142">O comportamento padrão do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) é usar o painel que o usuário selecionou por último.</span><span class="sxs-lookup"><span data-stu-id="57fd7-142">The default behavior of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is to use the panel the user selected last.</span></span>

### <a name="text-services-framework-correction-user-interface"></a><span data-ttu-id="57fd7-143">Interface do usuário de correção da estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="57fd7-143">Text Services Framework Correction User Interface</span></span>

<span data-ttu-id="57fd7-144">Neste exemplo, todos os campos de entrada são controles [InkEdit](/previous-versions/ms552265(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="57fd7-144">In this sample all of the input fields are [InkEdit](/previous-versions/ms552265(v=vs.100)) controls.</span></span> <span data-ttu-id="57fd7-145">Isso é significativo porque o controle InkEdit tem suporte interno para a TSF ( [estrutura de serviços de texto](../tsf/text-services-framework.md) ) e, portanto, é capaz de dar suporte à interface do usuário de correção in-loco para entrada recebida do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="57fd7-145">This is significant because the InkEdit control has built-in support for the [Text Services Framework](../tsf/text-services-framework.md) (TSF) and is thus capable of supporting the in-place correction user interface for input received from the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span>

<span data-ttu-id="57fd7-146">O valor padrão para [EnableTsf](/previous-versions/ms569656(v=vs.100)) é **true**.</span><span class="sxs-lookup"><span data-stu-id="57fd7-146">The default value for [EnableTsf](/previous-versions/ms569656(v=vs.100)) is **TRUE**.</span></span> <span data-ttu-id="57fd7-147">Isso faz com que o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tente iniciar a TSF (estrutura de serviços de texto) no controle anexado.</span><span class="sxs-lookup"><span data-stu-id="57fd7-147">This causes the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to attempt to start the Text Services Framework (TSF) on the attached control.</span></span> <span data-ttu-id="57fd7-148">Se for bem-sucedida, a interface do usuário de correção mostrará no controle e permitirá o acesso a alternativas de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="57fd7-148">If successful, the correction user interface shows in the control, and it allows access to recognition alternates.</span></span> <span data-ttu-id="57fd7-149">Chamar esse método com um parâmetro **false** tenta desligar o TSF no controle anexado.</span><span class="sxs-lookup"><span data-stu-id="57fd7-149">Calling this method with a **FALSE** parameter attempts to shut down TSF on the attached control.</span></span>

<span data-ttu-id="57fd7-150">O controle [InkEdit](/previous-versions/ms552265(v=vs.100)) já fornece uma interface do usuário de correção, mas no exemplo [EnableTsf](/previous-versions/ms569656(v=vs.100)) é usado para permitir que o [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) use o contexto de reconhecedor de inserção do TSF em vez da função [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) para enviar os resultados de reconhecimento de manuscrito para o controle.</span><span class="sxs-lookup"><span data-stu-id="57fd7-150">The [InkEdit](/previous-versions/ms552265(v=vs.100)) control already provides a correction user interface, but in the sample [EnableTsf](/previous-versions/ms569656(v=vs.100)) is used to enable the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) to use the TSF insertion recognizer context rather than the [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) function to send the handwriting recognition results into the control.</span></span> <span data-ttu-id="57fd7-151">O resultado é que o texto pode ser inserido mesmo que o campo não tenha mais foco.</span><span class="sxs-lookup"><span data-stu-id="57fd7-151">The result is that text can be inserted even if the field no longer has focus.</span></span>


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a><span data-ttu-id="57fd7-152">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="57fd7-152">Closing the Form</span></span>

<span data-ttu-id="57fd7-153">No código gerado pelo Windows Form Designer, os controles [InkEdit](/previous-versions/ms552265(v=vs.100)) e [InkPicture](/previous-versions/aa514604(v=msdn.10)) são adicionados à lista de componentes do formulário quando o formulário é inicializado.</span><span class="sxs-lookup"><span data-stu-id="57fd7-153">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms552265(v=vs.100)) and [InkPicture](/previous-versions/aa514604(v=msdn.10)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="57fd7-154">Quando o formulário é fechado, os controles InkEdit e InkPicture são descartados, bem como os outros componentes do formulário, pelo método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário.</span><span class="sxs-lookup"><span data-stu-id="57fd7-154">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span> <span data-ttu-id="57fd7-155">O método Dispose do formulário também descarta os objetos de [tinta](/previous-versions/aa515768(v=msdn.10)) criados para o formulário.</span><span class="sxs-lookup"><span data-stu-id="57fd7-155">The form's Dispose method also disposes the [Ink](/previous-versions/aa515768(v=msdn.10)) objects that are created for the form.</span></span>

 

 
