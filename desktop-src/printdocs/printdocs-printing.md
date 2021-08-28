---
description: Windows aplicativos com um conjunto completo de funções que permitem a impressão em vários dispositivos, como impressoras de raio, plotadores de vetor, impressoras de raster e máquinas de fax.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impressão (documentos e impressão)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6317275e60346428173bf47bdc8e9f84b7a3e523
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465653"
---
# <a name="printing-documents-and-printing"></a>Impressão (documentos e impressão)

Windows aplicativos com um conjunto completo de funções que permitem a impressão em vários dispositivos, como impressoras de raio, plotadores de vetor, impressoras de raster e máquinas de fax.

## <a name="desktop-app-printing"></a>Impressão de aplicativo da área de trabalho

Windows programadores podem selecionar entre várias tecnologias diferentes para imprimir de seu aplicativo.




| Tecnologia | Descrição | 
|------------|-------------|
| <a href="/windows/desktop/printdocs/tailored-app-printing-api">IMPRIMIR API do pacote de documentos</a><br /> | Fornece uma interface que permite que um aplicativo acesse e gerencie o pacote de documentos de impressão. Essa API está disponível com Windows 8 e versões posteriores do Windows.<br /> | 
| <a href="print-spooler-api.md">API do Spooler de Impressão</a><br /> | Fornece uma interface para o spooler de impressão para que os aplicativos possam gerenciar impressoras e trabalhos de impressão.<br /> Os aplicativos usam a API do <a href="print-spooler-api.md">Spooler</a> de Impressão para iniciar, parar, controlar e configurar trabalhos de impressão gerenciados pelo spooler de impressão, independentemente de usarem a <a href="/windows/desktop/printdocs/tailored-app-printing-api">API</a> imprimir pacote de documentos ou a API de Impressão <a href="gdi-printing.md">GDI</a> para imprimir o conteúdo.<br /> | 
| <a href="print-ticket-api.md">API de Tíquete de Impressão</a><br /> | Fornece aplicativos com funções para gerenciar e converter tíquetes de impressão.<br /> | 
| <a href="gdi-printing.md">API de Impressão GDI</a><br /> | Fornece aplicativos com uma interface de impressão independente de dispositivo. <br /><blockquote>[!Note]<br />Os desenvolvedores que estão escrevendo aplicativos para Windows Vista e versões posteriores do Windows devem considerar o uso da <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de Documento XPS</a> em seu aplicativo.</blockquote><br /> A <a href="gdi-printing.md">API de Impressão GDI</a> é adequada para aplicativos que devem ser executados Windows XP e versões anteriores do Windows.<br /> | 




 

A ilustração a seguir fornece uma exibição de alto nível de como as diferentes APIs de impressão estão relacionadas.

![um diagrama que mostra como um aplicativo nativo do Windows pode usar as APIs de impressão](images/print-apis.png)

 

As [API imprimir pacote de](./tailored-app-printing-api.md)documentos nesta seção descrevem o pacote de documentos de impressão e as interfaces de visualização de impressão que você pode usar com Windows 8 e versões posteriores do Windows desktop.

Para obter mais informações sobre impressão de Windows Store que são escritos em JavaScript e HTML, consulte Impressão (aplicativos da Windows Store usando [JavaScript e HTML).](/previous-versions/windows/apps/hh465225(v=win.10)) Para obter mais informações sobre impressão de aplicativos da Windows Store escritos em C#, Microsoft Visual Basic ou C++ e XAML, consulte [Impressão (aplicativos da Windows Store](/previous-versions/windows/apps/hh465196(v=win.10))usando C).

> [!Note]  
> Consulte Win32 e COM para [aplicativos da Windows Store (impressão](/uwp/win32-and-com/win32-and-com-for-uwp-apps) e documentos) para ver a lista das APIs de Impressão de Aplicativo da Área de Trabalho que também podem ser usadas em aplicativos Windows Store.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de Documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[Comunicações de impressora bidirecional (Centro de Desenvolvimento de Hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

