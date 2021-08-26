---
description: Este exemplo se baseia no exemplo Formulário de Declarações Automáticas integrando o objeto PenInputPanel. O exemplo está no diretório \# C PIPanel na pasta AutoClaims.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Exemplo de PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c464be52fd08c6c461ba094428a1868fbb51fb328e1a3c88a2d0949a6ae581e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934736"
---
# <a name="peninputpanel-sample"></a>Exemplo de PenInputPanel

Este exemplo se baseia no exemplo Formulário de Declarações Automáticas integrando o [objeto PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) O exemplo está no diretório \# C PIPanel na pasta AutoClaims.

> [!Note]  
> Este exemplo requer que o sistema esteja equipado com um dispositivo de caneta. Se você estiver usando apenas um mouse (ou outro dispositivo que aponta para HID (dispositivo de interface não humana), o [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) não será exibido.

 

Para obter mais informações sobre o exemplo de Formulário de Declarações Automáticas, consulte [Exemplo de formulário de declarações automáticas.](auto-claims-form-sample.md) Para obter mais informações sobre [o objeto PenInputPanel,](/previous-versions/aa514041(v=msdn.10)) consulte Programando o painel de entrada [usando a classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md).

No exemplo, o Formulário de Declarações Automáticas contém cinco campos nos quais o usuário é solicitado a colocar informações relevantes para a declaração: número da política, nome da casa, ano, marca e modelo do carro. Um [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) é anexado a cada campo de entrada para fornecer um meio fácil de inserir valores com uma caneta.

Há duas técnicas para anexar um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) aos campos de entrada no formulário. A primeira técnica é atribuir uma instância separada do objeto a cada campo de entrada em tempo de design. A segunda é criar uma única instância do objeto e, em seguida, anexar essa instância de objeto em tempo de executar a um campo quando receber o foco. Este exemplo demonstra as duas técnicas.

Há trocas envolvidas na decisão de qual técnica usar. A criação de uma instância exclusiva do objeto para cada campo de formulário requer um pouco mais de memória quando o formulário é carregado. No entanto, ele salva a dificuldade de lidar com eventos de foco para que os campos atribuam uma única instância ao campo atual em tempo de executar.

Como o [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tem suporte apenas em um tablet pc, o exemplo cria os objetos PenInputPanel dentro de um bloco de tratamento de exceção.

## <a name="one-object-per-field"></a>Um objeto por campo

O exemplo demonstra a primeira técnica (um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) por campo) atribuindo os campos de entrada para o número da política ( ) e o nome da pasta ( ) uma instância exclusiva do objeto `inkEdPolicyNumber` `inkEdName` PenInputPanel. Um construtor sobrecarregado para o objeto PenInputPanel pode usar o nome do controle de entrada como um argumento, associando os controles. As linhas a seguir do manipulador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário mostram isso:


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Um objeto por formulário

A segunda técnica também é mostrada no exemplo: uma única instância de um objeto [PenInputPanel,](/previous-versions/aa514041(v=msdn.10)) , é compartilhada entre os campos de entrada `pipShared` Year, Make e Model. O objeto compartilhado é criado usando o construtor padrão.


```C++
pipShared = new PenInputPanel();
```



Usar essa técnica requer que o formulário tenha apenas uma única instância do [objeto PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) Isso economiza memória, mas você deve adicionar código para manipular o evento quando um campo de entrada recebe o foco. Quando um controle que usa uma instância compartilhada de um objeto PenInputPanel obtém o foco, de definir a propriedade [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) do objeto PenInputPanel para esse controle. O código a seguir mostra um manipulador de eventos para os eventos dos campos Year, Make e `Enter` Model.


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



Certifique-se de definir todas as propriedades que precisam ser definidas quando o foco muda para um novo controle. Nos manipuladores de eventos anteriores, por exemplo, a [propriedade Factoid](/previous-versions/ms571978(v=vs.100)) é definida conforme apropriado.

## <a name="usability-considerations"></a>Considerações sobre usabilidade

Lembre-se das seguintes considerações de usabilidade ao usar [o objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) em seu aplicativo.

### <a name="positioning-the-peninputpanel"></a>Posicionando o PenInputPanel

Como os campos são colocados verticalmente no formulário neste exemplo, a interface do usuário [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para cada controle de entrada é posicionada ligeiramente à direita do controle de entrada para facilitar o uso. Isso impede que o PenInputPanel acoberte a próxima caixa de edição, facilitando o direcionamento para a próxima caixa de edição.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Selecionando o painel de entrada a ser exibido

Como os números de política geralmente são combinações de números, letras e outros caracteres, eles podem ser propensos a erros de reconhecimento. Portanto, o exemplo define o painel padrão exibido pelo objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para ser o teclado quando ele é anexado ao campo número da política.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



O comportamento padrão do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) é usar o painel selecionado pelo usuário por último.

### <a name="text-services-framework-correction-user-interface"></a>Estrutura de Serviços de Texto correção Interface do Usuário

Neste exemplo, todos os campos de entrada são [controles InkEdit.](/previous-versions/ms552265(v=vs.100)) Isso é significativo porque o controle InkEdit tem suporte integrado para o [Estrutura de Serviços de Texto](../tsf/text-services-framework.md) (TSF) e, portanto, é capaz de dar suporte à interface do usuário de correção no local para entrada recebida do objeto [PenInputPanel.](/previous-versions/aa514041(v=msdn.10))

O valor padrão para [EnableTsf](/previous-versions/ms569656(v=vs.100)) é **TRUE.** Isso faz com [que o objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tente iniciar o Estrutura de Serviços de Texto (TSF) no controle anexado. Se for bem-sucedida, a interface do usuário de correção será demonstrada no controle e permitirá o acesso a alternativas de reconhecimento. Chamar esse método com um **parâmetro FALSE** tenta desligar o TSF no controle anexado.

O [controle InkEdit](/previous-versions/ms552265(v=vs.100)) já fornece uma interface do usuário de correção, mas no exemplo [EnableTsf](/previous-versions/ms569656(v=vs.100)) é usado para habilitar [o PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a usar o contexto do reconhecedor de inserção TSF em vez da [**função SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) para enviar os resultados de reconhecimento de manuscrito para o controle. O resultado é que o texto pode ser inserido mesmo que o campo não tenha mais foco.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Fechando o formulário

No código gerado Windows Designer de Formulário, os controles [InkEdit](/previous-versions/ms552265(v=vs.100)) e [InkPicture](/previous-versions/aa514604(v=msdn.10)) são adicionados à lista de componentes do formulário quando o formulário é inicializado. Quando o formulário é fechado, os controles InkEdit e InkPicture são descartados, bem como os outros componentes do formulário, pelo método [Dispose do](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) formulário. O método Dispose do formulário também descarta os objetos [Ink](/previous-versions/aa515768(v=msdn.10)) criados para o formulário.

 

 
