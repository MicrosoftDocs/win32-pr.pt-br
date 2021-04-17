---
description: Estes tópicos descrevem os documentos e os recursos de impressão do Windows que permitem que os aplicativos salvem, exibam e imprimam.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Documentos e impressão '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b23ae7040586d550c47f3fedc59104d83fe818
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105759581"
---
# <a name="documents-and-printing"></a>Documentos e impressão 

Estes tópicos descrevem os documentos e os recursos de impressão do Windows que permitem que os aplicativos salvem, exibam e imprimam.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">O que há de novo para impressão</a><br/></td>
<td>O Windows 8 oferece suporte à <a href="/previous-versions/windows/apps/hh465225(v=win.10)">impressão para aplicativos da Windows Store usando JavaScript e HTML</a> e <a href="/previous-versions/windows/apps/hh465196(v=win.10)">impressão para aplicativos da Windows Store usando C#/VB/C + + e XAML</a>.<br/> O Windows 8 também inclui uma nova API baseada em COM que fornece suporte completo para Open XPS e acesso a partes dos novos drivers de impressora com suporte do Windows 8. Para obter mais informações sobre a nova API, consulte <a href="/windows/desktop/printdocs/tailored-app-printing-api">Imprimir API do pacote de documentos</a>.<br/> O programa caixa de entrada do driver de impressão do Windows garante que o Windows 8 inclua suporte para uma alta porcentagem das impressoras populares.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/jobbindalldocuments">Documentos XPS</a><br/></td>
<td>Informações sobre a API de documento XPS de uma assinatura digital XPS.<br/>
<ul>
<li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de documento XPS</a><br/> A API do documento XPS é uma API nativa do Windows que dá suporte ao OM XPS. A API de documento XPS foi introduzida no Windows 7 e pode ser usada em programas de modo de usuário e drivers de impressora XPSDrv.<br/></li>
<li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API de assinatura digital XPS</a><br/> As assinaturas digitais XPS permitem a assinatura de documentos, a verificação da identidade do signatário e a indicação de se um documento XPS foi alterado desde que foi assinado.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="printdocs-printing.md">Impressão</a><br/></td>
<td>Informações sobre os recursos de impressão compatíveis com o Windows. Esses recursos incluem:<br/>
<ul>
<li><a href="/windows/desktop/printdocs/tailored-app-printing-api">Imprimir API de pacote de documento</a><br/> Fornece aplicativos com uma interface que permite o gerenciamento do pacote do <strong>documento de documentos</strong> .<br/></li>
<li><a href="print-spooler-api.md">API do spooler de impressão</a><br/> Fornece uma interface para o spooler de impressão para que os aplicativos possam gerenciar impressoras e trabalhos de impressão.<br/></li>
<li><a href="print-ticket-api.md">API de tíquete de impressão</a><br/> Fornece aplicativos com funções para gerenciar e converter tíquetes de impressão.<br/></li>
<li><a href="gdi-printing.md">API de impressão GDI</a><br/> Fornece aplicativos com uma interface de impressão independente de dispositivo. <br/></li>
<li><p><a href="xps-printing.md">API de impressão XPS</a><br/> Fornece uma interface para o spooler de impressão que os aplicativos podem usar para enviar documentos XPS para uma impressora.</p>
<blockquote>
[!Note]<br />
Não há suporte para a API de impressão XPS e elas podem ser alteradas ou não disponíveis no futuro. Em vez disso, os aplicativos cliente devem usar a <a href="/windows/desktop/printdocs/tailored-app-printing-api">API de pacote de documentos de impressão</a> .
</blockquote>
<p><br/> <br/></p></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/printschema">Imprimir esquema</a><br/></td>
<td>O esquema de impressão e as tecnologias relacionadas descrevem os recursos de uma impressora e especificam as preferências de impressão de um documento para impressoras e exibição de aplicativos. A <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">especificação do esquema de impressão</a> é um documento que pode ser baixado que contém informações sobre o esquema de impressão e como usá-lo em documentos e impressão. As informações online encontradas nesta seção são fornecidas apenas para suas informações e podem não refletir com precisão a versão atual da especificação do esquema de <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">impressão</a>.<br/> Consulte a <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">especificação do esquema de impressão</a> para obter as informações de design mais atuais.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="additional-resources"></a>Recursos adicionais

O [aplicativo de exemplo imprimir amostra](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) demonstra como imprimir de um aplicativo da Windows Store começando com o Windows 8.

Os recursos descritos nesta seção são para programação nativa do Windows. Para usar recursos semelhantes na programação do .NET (gerenciado), consulte [Windows Presentation Foundation documentos](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

Os documentos XPS são criados na API de [empacotamento](/previous-versions/windows/desktop/opc/packaging) . Consulte a API de empacotamento para obter acesso de nível inferior ao conteúdo de um documento XPS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comunicações bidirecionais de impressora (centro de desenvolvimento de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
