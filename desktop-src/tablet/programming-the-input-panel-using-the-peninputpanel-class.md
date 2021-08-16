---
description: Descrição do uso do objeto PenInputPanel para programar o Painel de Entrada do Tablet pc no nível do sistema.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programando o painel de entrada usando a classe PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d430b002fb967652aea046919ec7341a984f420f756fd936e8c68dbfce8c055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449376"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>Programando o painel de entrada usando a classe PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) foi substituído por [Microsoft.Ink.TextInput.](/previous-versions/ms581554(v=vs.100)) Consulte Programando [o Painel de Entrada de Texto](programming-the-text-input-panel.md).\]

Descrição do uso [**do objeto PenInputPanel**](peninputpanel-class.md) para programar o Painel de Entrada do Tablet pc no nível do sistema.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Painel de entrada versus o objeto PenInputPanel

No Microsoft Windows XP Tablet PC Edition versão 1.0, o Painel de Entrada do tablet no nível do sistema fornece um mecanismo universal para realizar a entrada de texto na plataforma Windows, mas não fornece acesso programático. No SDK (Software Development Kit) do Windows XP Tablet PC Edition versão 1.5 e posterior, o objeto [**PenInputPanel**](peninputpanel-class.md) permite integrar ferramentas de entrada de texto diretamente aos seus aplicativos e fornecer um nível de controle não disponível anteriormente. A partir do Windows XP Tablet PC Edition 2005, o Painel de Entrada no nível do sistema foi atualizado para incluir a funcionalidade de entrada in-loque fornecidas pelo objeto **PenInputPanel** e muito mais.

O gráfico a seguir mostra o Painel de Entrada exibido sobre o [exemplo de Exemplo de Formulário de Declarações](auto-claims-form-sample.md) Automáticas.

![painel de entrada exibido em um formulário usado para declarações de automóveis](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

O Painel de Entrada é o responsável pelo [**PenInputPanel,**](peninputpanel-class.md) fornecendo a mesma funcionalidade de entrada in-loco para qualquer aplicativo em execução no Windows XP Tablet PC Edition 2005 ou posterior sem a necessidade de código adicional. Este artigo sobre como usar o **objeto PenInputPanel** é fornecido para compatibilidade com backward. Os aplicativos que já utilizam o objeto **PenInputPanel** funcionarão da mesma forma, exceto que o Painel de Entrada será exibido em vez do **PenInputPanel** quando o aplicativo for executado no Windows XP Tablet PC Edition 2005 ou posterior.

Se você estiver desenvolvendo um novo aplicativo para o Tablet PC e quiser ter uma solução de entrada de usuário in-locar, o Painel de Entrada o fornece automaticamente no Windows XP Tablet PC Edition 2005 ou posterior. Não é necessário insinuar o [**objeto PenInputPanel.**](peninputpanel-class.md)

## <a name="disabling-the-input-panel"></a>Desabilitando o painel de entrada

Pode haver casos em que você deseja desabilitar o Painel de Entrada. Há duas maneiras de fazer isso. Você pode fazer isso programaticamente ou definindo uma entrada do Registro que desabilita o Painel de Entrada para todo o aplicativo.

### <a name="disabling-input-panel-programmatically"></a>Desabilitando o painel de entrada programaticamente

Para desabilitar o Painel de Entrada programaticamente, insinue [**o PenInputPanel**](peninputpanel-class.md) e de definido sua propriedade [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) como **False.**


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



Para desabilitar o Painel de Entrada para vários controles em um único aplicativo, insinue um objeto [**PenInputPanel**](peninputpanel-class.md) para cada controle e de definir a propriedade [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)como **False** para cada um ou insinue um único **PenInputPanel** e mova-o do controle para controle conforme o foco de entrada muda. Para obter mais informações sobre essas duas técnicas, consulte o tópico [Exemplo de PenInputPanel.](peninputpanel-sample.md)

### <a name="disabling-input-panel-through-the-registry"></a>Desabilitando o painel de entrada por meio do Registro

Você pode definir uma entrada do Registro para desabilitar o Painel de Entrada para todo o aplicativo. No entanto, isso também o desabilitará  para caixas de  diálogo comuns, como a caixa de diálogo Abrir Arquivo, a caixa de diálogo Imprimir e a caixa **de** diálogo Salvar Arquivo . Isso pode tornar a experiência do usuário em seu aplicativo inconsistente com outros aplicativos de Tablet PC.

Definir a chave do Registro como zero impede que a interface do usuário do Painel de Entrada `DisableInPlace` apareça em um aplicativo. Você deve colocar `DisableInPlace` a chave do Registro em `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` . Em seguida, adicione um novo valor de Registro usando o caminho completo do aplicativo no qual você deseja desabilitar o Painel de Entrada. A seguinte entrada de registro de exemplo desabilita o Painel de Entrada em um aplicativo chamado MyApp:

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Se você ainda vir um problema em seu aplicativo depois de desabilitar a interface do usuário do Painel de Entrada, talvez seja necessário desabilitar a estrutura subjacente, que consulta seu aplicativo para o local do atromento. Por exemplo, o Painel de Entrada pode expor um bug no código de acompanhamento de aplicação. Desligar a consulta de acompanhamento do sinal de adoção também impede que a interface do usuário do Painel de Entrada seja exibida. Para desabilitar a estrutura, de definir `EnableCaretTracking` a chave do Registro como zero. Localize essa chave em `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> As ferramentas de acessibilidade e a tecnologia de fala Windows XP também usam essa estrutura, portanto, desabilitar a consulta também desabilita esses recursos em seu aplicativo.

 

## <a name="the-input-panel-and-web-pages"></a>O painel de entrada e as páginas da Web

Para usar uma API em uma página da Web, ela deve funcionar em um ambiente de confiança parcial. Todos [**os membros da classe PenInputPanel**](peninputpanel-class.md) exigem confiança total, exceto o seguinte:

-   [Construtores PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (somente código gerenciado)
-   [Método Dispose](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (somente código gerenciado)
-   [Propriedade AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (somente código gerenciado)
-   [**Propriedade AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Essas APIs funcionam em um ambiente de confiança parcial, como uma página da Web, permitindo que você inicie um objeto [**PenInputPanel,**](peninputpanel-class.md) anexe-o a um controle e desabilite o Painel de Entrada para esse controle. Para obter mais informações, consulte Programando o painel de entrada usando a classe PenInputPanel e [Ink na Web.](ink-on-the-web.md)

## <a name="the-peninputpanel-object"></a>O objeto PenInputPanel

O restante deste tópico descreve como usar o objeto [**PenInputPanel**](peninputpanel-class.md) em seus aplicativos habilitados para Tablet PC. Mais especificamente, este tópico refere-se ao objeto **PenInputPanel** ao discutir o objeto de programação, o painel de entrada de caneta ao se referir ao elemento de interface do usuário e o Painel de Entrada do COMPUTADOR (ou Painel de Entrada) ao fazer referência ao painel de entrada global normalmente encontrado no lado da tela do tablet.

As seções a seguir descrevem o [**objeto PenInputPanel**](peninputpanel-class.md) e a interface do usuário.

-   [Sobre o painel de entrada](about-the-input-panel.md)
-   [Inciando a classe PenInputPanel](instantiating-the-peninputpanel-class.md)
-   [Suporte a factoid](factoid-support.md)
-   [Estrutura de Serviços de Texto](text-services-framework.md)
-   [Práticas recomendadas](best-practices.md)

 

 
