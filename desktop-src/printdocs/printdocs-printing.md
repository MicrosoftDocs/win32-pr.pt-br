---
description: O Windows fornece aos aplicativos um conjunto completo de funções que permitem a impressão em vários dispositivos, como impressoras a laser, plotadoras vetoriais, impressoras de varredura e máquinas de fax.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impressão (documentos e impressão)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788647"
---
# <a name="printing-documents-and-printing"></a>Impressão (documentos e impressão)

O Windows fornece aos aplicativos um conjunto completo de funções que permitem a impressão em vários dispositivos, como impressoras a laser, plotadoras vetoriais, impressoras de varredura e máquinas de fax.

## <a name="desktop-app-printing"></a>Impressão de aplicativo de desktop

Os programadores do Windows podem selecionar entre várias tecnologias diferentes para imprimir de seu aplicativo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tecnologia</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/tailored-app-printing-api">Imprimir API de pacote de documento</a><br/></td>
<td>Fornece uma interface que permite que um aplicativo acesse e gerencie o pacote de documentos de impressão. Essa API está disponível com o Windows 8 e versões posteriores do Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="print-spooler-api.md">API do spooler de impressão</a><br/></td>
<td>Fornece uma interface para o spooler de impressão para que os aplicativos possam gerenciar impressoras e trabalhos de impressão.<br/> Os aplicativos usam a <a href="print-spooler-api.md">API spooler de impressão</a> para iniciar, parar, controlar e configurar trabalhos de impressão gerenciados pelo spooler de impressão, independentemente de usarem a <a href="/windows/desktop/printdocs/tailored-app-printing-api">API de pacote de documentos de impressão</a> ou a <a href="gdi-printing.md">API de impressão GDI</a> para imprimir o conteúdo.<br/></td>
</tr>
<tr class="odd">
<td><a href="print-ticket-api.md">API de tíquete de impressão</a><br/></td>
<td>Fornece aplicativos com funções para gerenciar e converter tíquetes de impressão.<br/></td>
</tr>
<tr class="even">
<td><a href="gdi-printing.md">API de impressão GDI</a><br/></td>
<td>Fornece aplicativos com uma interface de impressão independente de dispositivo. <br/>
<blockquote>
[!Note]<br />
Os desenvolvedores que estão escrevendo aplicativos para o Windows Vista e versões posteriores do Windows devem considerar o uso da <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de documento XPS</a> em seu aplicativo.
</blockquote>
<br/> A <a href="gdi-printing.md">API de impressão GDI</a> é adequada para aplicativos que devem ser executados no Windows XP e em versões anteriores do Windows.<br/></td>
</tr>
</tbody>
</table>



 

A ilustração a seguir fornece uma exibição de alto nível de como as diferentes APIs de impressão estão relacionadas.

![um diagrama que mostra como um aplicativo nativo do Windows pode usar as APIs de impressão](images/print-apis.png)

 

Os s da [API de pacote de documentos de impressão](./tailored-app-printing-api.md)nesta seção descrevem o pacote de documentos impressos e as interfaces de visualização de impressão que você pode usar com o Windows 8 e versões posteriores do Windows desktop.

Para obter mais informações sobre a impressão de aplicativos da Windows Store que são escritos em JavaScript e HTML, consulte [impressão (aplicativos da Windows Store usando JavaScript e HTML)](/previous-versions/windows/apps/hh465225(v=win.10)). Para obter mais informações sobre a impressão de aplicativos da Windows Store que são escritos em C#, Microsoft Visual Basic ou C++ e XAML, consulte [impressão (aplicativos da Windows Store usando C)](/previous-versions/windows/apps/hh465196(v=win.10)).

> [!Note]  
> Consulte [Win32 e com para aplicativos da Windows Store (impressão e documentos)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) para obter a lista de APIs de impressão do aplicativo de desktop que também podem ser usadas em aplicativos da Windows Store.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[Comunicações bidirecionais de impressora (centro de desenvolvimento de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

