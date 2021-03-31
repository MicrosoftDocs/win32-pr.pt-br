---
title: Certificar seu aplicativo de desktop
description: Siga estas etapas para obter seu aplicativo de desktop certificado para Windows 7, Windows 8, Windows 8.1 e Windows 10. se você quiser converter seu aplicativo de área de trabalho para ser compatível com o Plataforma Universal do Windows e a Windows Store, você usará a ponte de área de trabalho do Windows, caso em que você deve seguir as diretrizes de ponte de desktop para as etapas de certificação. Se você estiver desenvolvendo e certificando um aplicativo UWP desde o início, consulte Diretrizes para certificação de aplicativo do Windows em UWP para obter informações sobre certificação.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642914"
---
# <a name="certify-your-desktop-application"></a>Certificar seu aplicativo de desktop

> [!IMPORTANT]
> A certificação para aplicativos da área de trabalho Win32 foi [preterida](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920). Em vez disso, [envie arquivos aqui](https://www.microsoft.com/wdsi/filesubmission/).

Siga estas etapas para obter seu aplicativo de desktop certificado para Windows 7, Windows 8, Windows 8.1 e Windows 10.

Se você quiser converter seu aplicativo de área de trabalho para ser compatível com o Plataforma Universal do Windows e a Windows Store, você usará a [ponte de área de trabalho do Windows](https://developer.microsoft.com/windows/bridges/desktop), caso em que você deve seguir as diretrizes de ponte de [Desktop](/windows/uwp/porting/desktop-to-uwp-root) para as etapas de certificação.

Se você estiver desenvolvendo e certificando um aplicativo UWP desde o início, consulte [diretrizes para certificação de aplicativo do Windows em UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) para obter informações sobre certificação.

## <a name="step-1-prepare-for-certification"></a>Etapa 1: preparar-se para a certificação



| Tópico                                                                                       | Descrição                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Quais são os benefícios?](what-are-the-benefits-.md)<br/>                             | A certificação de seu aplicativo de desktop fornece vários benefícios para você e seus clientes.              |
| [Leia os requisitos](certification-requirements-for-windows-desktop-apps.md)<br/> | Examine os requisitos técnicos e as qualificações de qualificação que um aplicativo de desktop deve atender. |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a>Etapa 2: testar seu aplicativo com o kit de certificação de aplicativos do Windows



| Tópico                                                          | Descrição                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtenha o kit](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | Para certificar seu aplicativo, você precisa instalar e executar o kit de certificação de aplicativos para Windows (incluído no SDK do Windows).                                                                     |
| [Usando o kit](using-the-windows-app-certification-kit.md)   | Antes de poder enviar seu aplicativo, você deve testá-lo para preparação. Você também pode baixar uma cópia do [White Paper de certificação do aplicativo](https://www.microsoft.com/download/details.aspx?id=27414). |
| [Examinar detalhes do teste](windows-app-certification-kit-tests.md) | Obtenha a lista dos testes que seu aplicativo precisa passar para se qualificar para compatibilidade com o sistema operacional Windows mais recente.                                                               |



 

Observação: os drivers de filtro também devem passar pelo [Kit de certificação de hardware](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe). (Consulte [requisitos de certificação para aplicativos da área de trabalho do Windows, seção 6,2](certification-requirements-for-windows-desktop-apps.md).)

## <a name="step-3-use-the-windows-certification-dashboard"></a>Etapa 3: usar o painel de certificação do Windows

Para enviar seu aplicativo para certificação, você precisará fazer logon ou registrar uma conta da empresa no [painel de certificação do Windows](/previous-versions/hh833792(v=msdn.10)). Depois de fazer isso, não só será possível adquirir seu aplicativo, mas você também obterá acesso a ferramentas para revisar e gerenciar seu aplicativo em todos os estágios do processo.



| Tópico                                                                                                                   | Descrição                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configurar sua conta](/windows-hardware/drivers/dashboard/)                 | Se sua empresa ainda não estiver registrada, você deverá registrá-la por meio do painel de certificação do Windows.                                        |
| [Obter um certificado de assinatura de código](/windows-hardware/drivers/dashboard/)      | Antes de poder estabelecer uma conta do painel de certificação do Windows, você precisa obter um certificado de assinatura de código para proteger suas informações digitais. |
| [Testar localmente e carregar os resultados](/windows-hardware/drivers/dashboard/) | Depois de executar os testes do kit de certificação de aplicativos do Windows, carregue os resultados no painel de certificação do Windows.                                 |
| [Gerenciar seu envio](/windows-hardware/drivers/dashboard/)              | Depois de enviar seu aplicativo para certificação, você pode revisar seu envio por meio do painel de certificação do Windows.                           |



 

## <a name="step-4-promote-your-desktop-app"></a>Etapa 4: promover seu aplicativo de área de trabalho



| Tópico                                                                      | Descrição                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Verificar a compatibilidade do aplicativo](/windows/compatibility/windows-8-1-introduction) | Se você estiver criando um aplicativo para Windows 8.1, investigue as preocupações de compatibilidade.                                           |
| [Use o logotipo com seu aplicativo](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | Exiba o logotipo no empacotamento e em anúncios e outros materiais promocionais de acordo com as diretrizes. Somente para o Windows 7. |



 

## <a name="see-also"></a>Consulte também:

[Fórum de compatibilidade de aplicativos](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): encontre suporte da Comunidade sobre a compatibilidade e a certificação de logotipo.

[Blog de SDK do Windows](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): encontre dicas e notícias relacionadas à certificação de aplicativo.

[Fórum do Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): visite o fórum de certificação para obter respostas.

[Manual de compatibilidade](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Obtenha informações sobre as novidades ou alterações na versão mais recente do Windows.

 

