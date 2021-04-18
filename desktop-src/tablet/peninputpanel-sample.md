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
# <a name="peninputpanel-sample"></a>Exemplo de PenInputPanel

Este exemplo baseia-se no exemplo de formulário de declarações automáticas integrando o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . O exemplo está no diretório C \# PIPanel na pasta Autodeclarations.

> [!Note]  
> Este exemplo requer que o sistema esteja equipado com um dispositivo de caneta. Se você estiver usando apenas um mouse (ou outro dispositivo de interface não-humana (HID)), o [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) não aparecerá.

 

Para obter mais informações sobre o exemplo de formulário de declarações automáticas, consulte [exemplo de formulário de declarações automática](auto-claims-form-sample.md). Para obter mais informações sobre o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , consulte [programando o painel de entrada usando a classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md).

No exemplo, o formulário de declarações automáticas contém cinco campos nos quais o usuário é solicitado a colocar as informações relevantes para a declaração: número da política, nome segurado, ano, marca e modelo do carro. Um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) é anexado a cada campo de entrada para fornecer um meio fácil de inserir valores com uma caneta.

Há duas técnicas para anexar um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) aos campos de entrada no formulário. A primeira técnica é atribuir uma instância separada do objeto a cada campo de entrada em tempo de design. A segunda é criar uma única instância do objeto e, em seguida, anexar essa instância de objeto em tempo de execução a um campo quando receber o foco. Este exemplo demonstra as duas técnicas.

Há compensações envolvidas na decisão de qual técnica usar. A criação de uma instância exclusiva do objeto para cada campo de formulário requer um pouco mais de memória quando o formulário é carregado. No entanto, ele economiza ter que lidar com eventos de foco para os campos atribuir uma única instância ao campo atual em tempo de execução.

Como o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tem suporte apenas em um Tablet PC, o exemplo cria os objetos PenInputPanel dentro de um bloco de tratamento de exceção.

## <a name="one-object-per-field"></a>Um objeto por campo

O exemplo demonstra a primeira técnica (um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) por campo) atribuindo os campos de entrada para número de política ( `inkEdPolicyNumber` ) e nome segurado ( `inkEdName` ) uma instância exclusiva do objeto PenInputPanel. Um construtor sobrecarregado para o objeto PenInputPanel pode pegar o nome do controle de entrada como um argumento, associando assim os controles. As linhas a seguir do manipulador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário mostram:


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Um objeto por formulário

A segunda técnica também é mostrada no exemplo: uma única instância de um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , `pipShared` , é compartilhada entre os campos de entrada year, Make e Model. O objeto compartilhado é criado usando o construtor padrão.


```C++
pipShared = new PenInputPanel();
```



Usar essa técnica requer que seu formulário tenha apenas uma única instância do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . Isso economiza memória, mas você deve adicionar código para manipular o evento quando um campo de entrada recebe o foco. Quando um controle que usa uma instância compartilhada de um objeto PenInputPanel Obtém foco, defina a propriedade [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) do objeto PenInputPanel para esse controle. O código a seguir mostra um manipulador de eventos para os eventos year, Make e Model Fields `Enter` .


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



Certifique-se de definir as propriedades que precisam ser definidas quando o foco é alterado para um novo controle. Nos manipuladores de eventos anteriores, por exemplo, a propriedade [factoname](/previous-versions/ms571978(v=vs.100)) é definida conforme apropriado.

## <a name="usability-considerations"></a>Considerações sobre usabilidade

Tenha em mente as seguintes considerações de usabilidade ao usar o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) em seu aplicativo.

### <a name="positioning-the-peninputpanel"></a>Posicionando o PenInputPanel

Como os campos são dispostos verticalmente no formulário neste exemplo, a interface do usuário [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para cada controle de entrada está posicionada ligeiramente à direita do controle de entrada para facilitar o uso. Isso impede que o PenInputPanel cubra a próxima caixa de edição, facilitando o direcionamento da próxima caixa de edição.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Selecionando o painel de entrada para exibição

Como os números de política geralmente são combinações de números, letras e outros caracteres, eles podem estar sujeitos a erros de reconhecimento. Portanto, o exemplo define o painel padrão exibido pelo objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) como o teclado quando ele é anexado ao campo de número da política.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



O comportamento padrão do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) é usar o painel que o usuário selecionou por último.

### <a name="text-services-framework-correction-user-interface"></a>Interface do usuário de correção da estrutura de serviços de texto

Neste exemplo, todos os campos de entrada são controles [InkEdit](/previous-versions/ms552265(v=vs.100)) . Isso é significativo porque o controle InkEdit tem suporte interno para a TSF ( [estrutura de serviços de texto](../tsf/text-services-framework.md) ) e, portanto, é capaz de dar suporte à interface do usuário de correção in-loco para entrada recebida do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .

O valor padrão para [EnableTsf](/previous-versions/ms569656(v=vs.100)) é **true**. Isso faz com que o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tente iniciar a TSF (estrutura de serviços de texto) no controle anexado. Se for bem-sucedida, a interface do usuário de correção mostrará no controle e permitirá o acesso a alternativas de reconhecimento. Chamar esse método com um parâmetro **false** tenta desligar o TSF no controle anexado.

O controle [InkEdit](/previous-versions/ms552265(v=vs.100)) já fornece uma interface do usuário de correção, mas no exemplo [EnableTsf](/previous-versions/ms569656(v=vs.100)) é usado para permitir que o [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) use o contexto de reconhecedor de inserção do TSF em vez da função [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) para enviar os resultados de reconhecimento de manuscrito para o controle. O resultado é que o texto pode ser inserido mesmo que o campo não tenha mais foco.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Fechando o formulário

No código gerado pelo Windows Form Designer, os controles [InkEdit](/previous-versions/ms552265(v=vs.100)) e [InkPicture](/previous-versions/aa514604(v=msdn.10)) são adicionados à lista de componentes do formulário quando o formulário é inicializado. Quando o formulário é fechado, os controles InkEdit e InkPicture são descartados, bem como os outros componentes do formulário, pelo método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário. O método Dispose do formulário também descarta os objetos de [tinta](/previous-versions/aa515768(v=msdn.10)) criados para o formulário.

 

 
