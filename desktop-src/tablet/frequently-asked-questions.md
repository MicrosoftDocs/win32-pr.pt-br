---
description: Veja a seguir as perguntas frequentes sobre o desenvolvimento para os componentes da plataforma Tablet PC instalados pelo SDK do Windows Vista.
ms.assetid: eb349493-a2b2-4b58-bcbc-ee09953c8dc8
title: Perguntas frequentes (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722c00fa5aaf2b43494484fc015fa8b3e4c7826
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104369010"
---
# <a name="frequently-asked-questions-about-developing-for-the-tablet-pc-platform"></a>Perguntas frequentes sobre o desenvolvimento para a plataforma Tablet PC

Veja a seguir as perguntas frequentes sobre o desenvolvimento para os componentes da plataforma Tablet PC instalados pelo SDK do Windows Vista.

## <a name="q-can-i-use-the-ink-apis-or-controls-in-a-web-page"></a>Q. Posso usar as APIs de tinta ou os controles em uma página da Web?

a. Sim. A biblioteca gerenciada do Tablet PC dá suporte a ambientes parcialmente confiáveis, ou seja, a execução de assemblies gerenciados de páginas da Web.

Também há suporte para a implantação de navegador de aplicativos que usam Windows Presentation Foundation.

## <a name="q-do-i-need-a-tablet-pc-to-develop-tablet-pc-applications"></a>Q. É necessário um Tablet PC para desenvolver aplicativos para Tablet PC?

a. Não, os componentes da plataforma Tablet PC instalados pelo SDK do Windows incluem as extensões e os utilitários necessários para desenvolver software para o Tablet PC em um computador desktop ou laptop. Você pode usar um mouse ou Tablet externo para entrada de caneta e manuscrito.

Os componentes da plataforma do Tablet PC instalados pelo SDK do Windows podem ser instalados no Windows XP Professional ou no Windows Server 2003, mas há menos funcionalidades disponíveis para seus aplicativos. Nessas plataformas, seu aplicativo pode coletar tinta com os objetos [**InkCollector**](inkcollector-class.md) e [**InkOverlay**](inkoverlay-class.md) e pode ser testado e depurado.

Além disso, os controles [InkEdit](inkedit-control-reference.md) e [InkPicture](inkpicture-control-reference.md) podem coletar tinta nesses sistemas operacionais somente se os componentes da plataforma Tablet PC tiverem sido instalados do SDK do Windows (ou uma versão mais antiga do kit de desenvolvimento do Tablet PC); Eles não coletam tinta em aplicativos que são redistribuídos para computadores não tablets sem os componentes da plataforma instalados.

## <a name="q-do-i-need-to-run-a-special-version-of-windows-to-do-handwriting-recognition"></a>Q. É necessário executar uma versão especial do Windows para fazer o reconhecimento de manuscrito?

a. Não. Embora apenas o Windows XP Tablet PC Edition e determinadas versões do Windows Vista incluam reconhecedores de manuscrito, você pode baixar o [pacote do reconhecedor do Windows XP Tablet PC Edition 2005]( https://www.microsoft.com/downloads/details.aspx?FamilyId=080184DD-5E92-4464-B907-10762E9F918B&amp;displaylang=en) e instalá-lo no Windows XP Professional ou no windows Server 2003 apenas para fins de desenvolvimento. Você não pode redistribuir os reconhecedores com seu aplicativo.

## <a name="q-what-is-the-difference-between-windows-vista-and-tablet-pc-technology"></a>Q. Qual é a diferença entre a tecnologia Windows Vista e Tablet PC?

a. Os Tablet PCs executam o sistema operacional Windows Vista, apresentando toda a funcionalidade do Windows Vista, além de recursos adicionais específicos do Tablet PC. Esses recursos de tecnologia do Tablet PC permitem que os usuários executem aplicativos Windows e Windows usando uma caneta, anotando documentos e criando documentos manuscritos usando tinta digital. A tecnologia do Tablet PC está disponível na maioria das versões do Windows Vista e, se o hardware do Tablet PC estiver disponível em um computador, os recursos só funcionarão.

Para versões anteriores de sistemas operacionais Windows que não dão suporte nativo à tinta, você pode redistribuir e usar os controles de tinta do Tablet PC para exibir a tinta desenhada em um Tablet PC.

## <a name="q-what-is-the-difference-between-windows-xp-tablet-pc-edition-and-windows-xp-tablet-pc-edition-2005"></a>Q. Qual é a diferença entre o Windows XP Tablet PC Edition e o Windows XP Tablet PC Edition 2005?

a. O Windows XP Tablet PC Edition 2005 é uma versão atualizada do Windows XP Tablet PC Edition.

## <a name="q-how-do-i-modify-my-application-to-run-on-a-tablet-pc"></a>Q. Como fazer modificar meu aplicativo para ser executado em um Tablet PC?

a. Os aplicativos do Microsoft Windows executados em um computador desktop ou laptop com Windows XP com hardware comparável podem ser executados em um Tablet PC sem modificações.

## <a name="q-i-understand-that-i-dont-need-to-make-any-changes-to-my-application-but-it-is-difficult-to-use-it-with-a-pen-and-speech-what-can-i-do-to-optimize-my-application-for-a-tablet-pc"></a>Q. Entendo que não preciso fazer nenhuma alteração no meu aplicativo, mas é difícil usá-lo com uma caneta e fala. O que posso fazer para otimizar meu aplicativo para um Tablet PC?

a. Os controles de API e de tinta dos componentes da plataforma Tablet PC podem ser usados para criar interfaces de usuário que são mais adequadas para entrada de caneta e manuscrito. Para obter mais informações sobre maneiras específicas de melhorar seu aplicativo, consulte [diretrizes de experiência do usuário do Mobile PC para desenvolvedores](/previous-versions//dd356056(v=vs.85)).

## <a name="q-what-programming-languages-does-the-tablet-support"></a>Q. A quais linguagens de programação o Tablet dá suporte?

a. A tecnologia do Tablet PC no Windows Vista dá suporte a COM (C++) e bibliotecas gerenciadas (o pacote de linguagens do Visual Studio .NET).

A tecnologia Tablet PC também dá suporte a Windows Presentation Foundation (WPF).

## <a name="q-do-i-have-sample-code-that-demonstrates-tablet-platform-capabilities"></a>Q. Tenho um código de exemplo que demonstra os recursos da plataforma Tablet?

a. Sim, o código de exemplo para COM e as linguagens gerenciadas selecionadas estão incluídos nos componentes da plataforma Tablet PC instalados pelo SDK da plataforma Windows.

Para aplicativos de exemplo disponíveis, consulte:

- [Amostras de PC móvel e Tablet PC](mobile-pc-and-tablet-pc-samples.md)
- [Exemplos de tinta digital, Windows Presentation Foundation (WPF)](/previous-versions/dotnet/netframework-3.0/aa972145(v=vs.85))
- <systemdrive>: \\ Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ amostras \\ Tablet

## <a name="q-whats-the-base-level-of-tablet-hardware-that-i-should-develop-for"></a>Q. Qual é o nível básico do hardware do Tablet que devo desenvolver?

a. Em geral, você deve criar um sistema compatível com o Windows Vista, sem herdado.

## <a name="q-what-user-interface-guidelines-can-you-provide-for-tablet-applications"></a>Q. Quais diretrizes de interface do usuário você pode fornecer para aplicativos do Tablet?

a. Problemas da orientação do menu suspenso para da Parallax de tela/digitalizador são descritos na seção [diretrizes de experiência do usuário do PC móvel para desenvolvedores](/previous-versions//dd356056(v=vs.85)) na PC móvel do SDK do Windows.

## <a name="q-do-you-include-system-level-handwriting-gestures-for-commonly-used-keystrokes-can-i-create-my-own-gestures-for-use-when-an-application-is-running-or-has-focus"></a>Q. Você inclui gestos de manuscrito em nível de sistema para pressionamentos de teclas mais usados? Posso criar meus próprios gestos para usar quando um aplicativo estiver em execução ou tiver foco?

a. Sim, incluímos um conjunto de gestos para eventos de mouse. Além disso, você pode criar gestos para uso em seu aplicativo. Para obter mais informações sobre gestos, consulte [usando gestos](using-gestures.md).

## <a name="q-how-can-i-determine-whether-my-application-is-running-on-a-tablet"></a>Q. Como posso determinar se meu aplicativo está sendo executado em um Tablet?

a. Use o GetSystemMetricsAPI do Windows e transmita o Tablet do SM \_ como o valor do índice. O SM \_ Tablet é definido em winuser. h. O valor de Tablet de SM \_ é 86.

Para o desenvolvimento para a Web, você deve ler a variável de ambiente de cadeia de caracteres do agente do usuário \_ \_ . Você pode acessar essa coleção Request. ServerVariables.

Para obter detalhes de como usar o GetSystemMetrics em Tablet PCs que executam o Windows Vista ou o Windows XP Tablet PC Edition, consulte [determinando se um PC é um Tablet PC](determining-whether-a-pc-is-a-tablet-pc.md).

## <a name="q-how-can-i-determine-whether-tablet-platform-components-are-available"></a>Q. Como posso determinar se os componentes da plataforma Tablet estão disponíveis?

a. Algumas partes da plataforma do Tablet PC podem ser instaladas em versões não-Tablet dos sistemas operacionais Windows XP Professional, Windows Server 2003 e Windows 2000.

A maneira apropriada de determinar se um componente da API está instalado é tentar criar uma instância de um objeto ou controle e verificar se ela existe antes de tentar usá-la.

Por exemplo, para determinar se o objeto [**InkCollector**](inkcollector-class.md) está disponível, tente criá-lo usando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

```C++
IInkCollector* pIInkCollector = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkCollector,
 NULL, CLSCTX_INPROC_SERVER, 
 IID_IInkCollector,
 (void **)&pIInkCollector);
if (SUCCEEDED(hr)) 
{ 
  /* InkCollector is usable. */ 
} else 
{
  /* InkCollector unavailable. */
}
```

## <a name="q-how-do-i-run-the-tablet-input-service-on-server-skus"></a>Q. Como fazer executar o serviço de entrada do Tablet nas SKUs do servidor?

a. O TabletInputService foi projetado para não ser executado automaticamente em SKUs de servidor quando o pacote do cliente é instalado. O Client Pack instala todos os componentes na plataforma para que qualquer um dos aplicativos cliente do Tablet possa ser executado também em um servidor. O serviço de entrada do Tablet escuta a notificação PnP em que um digitalizador externo está conectado. Para habilitar o serviço de entrada do Tablet em um servidor, use o utilitário de configuração do sistema.

No menu **Iniciar** , selecione **executar**. Digite "msconfig" e pressione Enter. Selecione a guia **Serviços** , localize os serviços denominados "serviço de entrada HID", marque a caixa de seleção ao lado dele e clique em **aplicar**. Feche o utilitário.

## <a name="q-more-faqs-and-other-resources"></a>Q. Mais perguntas frequentes e outros recursos

- [Centro de Desenvolvimento Microsoft](https://developer.microsoft.com)
- [Referência do Tablet PC principal](./core-reference---tablet-pc-com-library.md)