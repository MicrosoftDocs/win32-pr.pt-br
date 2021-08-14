---
description: Descrição do uso do objeto PenInputPanel para programar o painel de entrada do Tablet PC no nível do sistema.
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

\[[**PenInputPanel**](peninputpanel-class.md) foi substituído por [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)). Consulte [programando o painel de entrada de texto](programming-the-text-input-panel.md).\]

Descrição do uso do objeto [**PenInputPanel**](peninputpanel-class.md) para programar o painel de entrada do Tablet PC no nível do sistema.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Painel de entrada versus o objeto PenInputPanel

no Microsoft Windows XP tablet PC Edition versão 1,0, o painel de entrada do Tablet pc no nível do sistema fornece um mecanismo universal para realizar a entrada de texto na plataforma Windows, mas não fornece acesso programático. no Windows XP Tablet PC Edition Software Development Kit (SDK) versão 1,5 e posterior, o objeto [**PenInputPanel**](peninputpanel-class.md) permite que você integre ferramentas de entrada de texto diretamente em seus aplicativos e forneça um nível de controle que não estava disponível anteriormente. a partir do Windows XP Tablet PC Edition 2005, o painel de entrada no nível do sistema foi atualizado para incluir a funcionalidade de entrada in-loco fornecida pelo objeto **PenInputPanel** e muito mais.

O gráfico a seguir mostra o painel de entrada exibido sobre a amostra de [exemplo de formulário de declarações automática](auto-claims-form-sample.md) .

![painel de entrada exibido em um formulário usado para declarações de automóvel](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

o painel de entrada substitui o [**PenInputPanel**](peninputpanel-class.md) fornecendo a mesma funcionalidade de entrada in-loco para qualquer aplicativo executado em Windows XP Tablet PC Edition 2005 ou posterior sem a necessidade de código adicional. Este artigo sobre como usar o objeto **PenInputPanel** é fornecido para compatibilidade com versões anteriores. os aplicativos que já utilizam o objeto **PenInputPanel** funcionarão da mesma forma, exceto que o painel de entrada será exibido em vez do **PenInputPanel** quando o aplicativo for executado no Windows XP Tablet PC Edition 2005 ou posterior.

se você estiver desenvolvendo um novo aplicativo para o Tablet PC e quiser ter uma solução de entrada do usuário in-loco, o painel de entrada fornecerá isso automaticamente no Windows XP Tablet PC Edition 2005 ou posterior. Não é necessário criar uma instância do objeto [**PenInputPanel**](peninputpanel-class.md) .

## <a name="disabling-the-input-panel"></a>Desabilitando o painel de entrada

Pode haver casos em que você deseja desabilitar o painel de entrada. Há duas maneiras de fazer isso. Você pode fazer isso programaticamente ou definindo uma entrada de registro que desabilita o painel de entrada para todo o aplicativo.

### <a name="disabling-input-panel-programmatically"></a>Desabilitando o painel de entrada programaticamente

Para desabilitar o painel de entrada programaticamente, instancie o [**PenInputPanel**](peninputpanel-class.md) e defina sua propriedade [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) como **false**.


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



Para desabilitar o painel de entrada para vários controles em um único aplicativo, crie uma instância de um objeto [**PenInputPanel**](peninputpanel-class.md) para cada controle e defina a propriedade [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)como **false** para cada uma ou instancie um único **PenInputPanel** e mova-o de Control para Control como o foco de entrada é alterado. Para obter mais informações sobre essas duas técnicas, consulte o tópico de [exemplo PenInputPanel](peninputpanel-sample.md) .

### <a name="disabling-input-panel-through-the-registry"></a>Desabilitando o painel de entrada por meio do registro

Você pode definir uma entrada de registro para desabilitar o painel de entrada para todo o aplicativo. No entanto, isso também o desabilitará para caixas de diálogo comuns, como a caixa de diálogo **Abrir arquivo** , a caixa de diálogo **Imprimir** e a caixa de diálogo **salvar arquivo** . Isso pode tornar a experiência do usuário em seu aplicativo inconsistente com outros aplicativos do Tablet PC.

Definir a `DisableInPlace` chave do registro como zero impede que a interface do usuário do painel de entrada seja exibida em um aplicativo. Você deve posicionar a `DisableInPlace` chave do registro em `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` . Em seguida, adicione um novo valor de registro usando o caminho completo do aplicativo no qual você deseja desabilitar o painel de entrada. A seguinte entrada de registro de exemplo desabilita o painel de entrada em um aplicativo chamado MyApp:

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Se você ainda vir um problema em seu aplicativo depois de desabilitar a interface do usuário do painel de entrada, pode ser necessário desabilitar a estrutura subjacente, que consulta seu aplicativo para o local do cursor. Por exemplo, o painel de entrada pode expor um bug no código de rastreamento de cursor do seu aplicativo. Desativar a consulta de rastreamento de cursor também impede que a interface do usuário do painel de entrada apareça. Para desabilitar a estrutura, defina a `EnableCaretTracking` chave do registro como zero. Localize essa chave em `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> ferramentas de acessibilidade e tecnologia de fala no Windows XP também usam essa estrutura, portanto, desabilitar a consulta também desabilita esses recursos em seu aplicativo.

 

## <a name="the-input-panel-and-web-pages"></a>O painel de entrada e as páginas da Web

Para usar uma API em uma página da Web, ela deve funcionar em um ambiente de confiança parcial. Todos os membros da classe [**PenInputPanel**](peninputpanel-class.md) exigem confiança total, exceto o seguinte:

-   [Construtores PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (somente código gerenciado)
-   [Método Dispose](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (somente código gerenciado)
-   [Propriedade AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (somente código gerenciado)
-   [**Propriedade de automostrar**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Essas APIs funcionam em um ambiente de confiança parcial, como uma página da Web, permitindo que você instancie um objeto [**PenInputPanel**](peninputpanel-class.md) , anexe-o a um controle e desabilite o painel de entrada para esse controle. Para obter mais informações, consulte Programando o painel de entrada usando a classe PenInputPanel e a [tinta na Web](ink-on-the-web.md).

## <a name="the-peninputpanel-object"></a>O objeto PenInputPanel

O restante deste tópico descreve como usar o objeto [**PenInputPanel**](peninputpanel-class.md) em seus aplicativos habilitados para Tablet PC. Mais especificamente, este tópico refere-se ao objeto **PenInputPanel** ao discutir o objeto de programação, o painel de entrada da caneta ao se referir ao elemento da interface do usuário e ao painel de entrada do PC (ou painel de entrada) ao se referir ao painel de entrada global normalmente encontrado no lado da tela do Tablet PC.

As seções a seguir descrevem o objeto [**PenInputPanel**](peninputpanel-class.md) e a interface do usuário.

-   [Sobre o painel de entrada](about-the-input-panel.md)
-   [Instanciando a classe PenInputPanel](instantiating-the-peninputpanel-class.md)
-   [Suporte ao factor](factoid-support.md)
-   [Estrutura de serviços de texto](text-services-framework.md)
-   [Práticas recomendadas](best-practices.md)

 

 
