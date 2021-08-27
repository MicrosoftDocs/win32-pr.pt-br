---
description: Estes tópicos descrevem os documentos e os recursos de impressão Windows que permitem que os aplicativos salvem, exibim e imprimam.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Documentos e impressão '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d7af92af0615dcb11d2623be8f2e21ae813aa1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472362"
---
# <a name="documents-and-printing"></a>Documentos e impressão 

Estes tópicos descrevem os documentos e os recursos de impressão Windows que permitem que os aplicativos salvem, exibim e imprimam.

## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Novidades para impressão</a><br /> | Windows 8 dá suporte à impressão <a href="/previous-versions/windows/apps/hh465225(v=win.10)">para aplicativos da Windows Store</a> usando JavaScript e HTML e impressão para aplicativos da Windows Store usando <a href="/previous-versions/windows/apps/hh465196(v=win.10)">C#/VB/C++ e XAML.</a><br /> Windows 8 também inclui uma nova API baseada em COM que fornece suporte completo para Open XPS e acesso a partes dos novos drivers de impressora compatíveis com Windows 8. Para obter mais informações sobre a nova API, consulte <a href="/windows/desktop/printdocs/tailored-app-printing-api">Imprimir API do pacote de documentos</a>.<br /> O Windows de Entrada do Driver de Impressão garante que Windows 8 inclua suporte para um alto percentual das impressoras populares.<br /> | 
| <a href="/windows/desktop/printdocs/jobbindalldocuments">Documentos XPS</a><br /> | Informações sobre a API de Documentos XPS e assinaturas digitais XPS.<br /><ul><li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de Documento XPS</a><br /> A API de Documento XPS é uma API Windows nativa que dá suporte ao OM XPS. A API de Documento XPS foi introduzida no Windows 7 e pode ser usada em programas de modo de usuário e drivers de impressora XPSDrv.<br /></li><li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API de Assinatura Digital XPS</a><br /> As Assinaturas Digitais XPS permitem a assinatura de documentos, a verificação da identidade do signante e a indicação de se um documento XPS foi alterado desde que foi assinado.<br /></li></ul> | 
| <a href="printdocs-printing.md">Impressão</a><br /> | Informações sobre os recursos de impressão com suporte Windows. Esses recursos incluem:<br /><ul><li><a href="/windows/desktop/printdocs/tailored-app-printing-api">IMPRIMIR API do pacote de documentos</a><br /> Fornece aplicativos com uma interface que permite o gerenciamento do <strong>pacote PrintDocument.</strong><br /></li><li><a href="print-spooler-api.md">API do Spooler de Impressão</a><br /> Fornece uma interface para o spooler de impressão para que os aplicativos possam gerenciar impressoras e trabalhos de impressão.<br /></li><li><a href="print-ticket-api.md">API de Tíquete de Impressão</a><br /> Fornece aplicativos com funções para gerenciar e converter tíquetes de impressão.<br /></li><li><a href="gdi-printing.md">API de Impressão GDI</a><br /> Fornece aplicativos com uma interface de impressão independente de dispositivo. <br /></li><li><p><a href="xps-printing.md">API de Impressão XPS</a><br /> Fornece uma interface para o spooler de impressão que os aplicativos podem usar para enviar documentos XPS para uma impressora.</p><blockquote>[!Note]<br />A API de Impressão XPS não tem suporte e pode ser alterada ou não disponível no futuro. Em vez disso, os aplicativos cliente devem <a href="/windows/desktop/printdocs/tailored-app-printing-api">usar a API Imprimir Pacote de</a> Documentos.</blockquote><p><br /><br /></p></li></ul> | 
| <a href="/windows/desktop/printdocs/printschema">Esquema de impressão</a><br /> | O Esquema de Impressão e as tecnologias relacionadas descrevem os recursos de uma impressora e especificam as preferências de impressão de um documento para impressoras e exibição de aplicativos. A <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Especificação de Esquema de</a> Impressão é um documento que pode ser baixado que contém informações sobre o esquema de impressão e como usá-lo em documentos e impressão. As informações online encontradas nesta seção são fornecidas apenas para suas informações e podem não refletir com precisão a versão atual da Especificação <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">de Esquema de Impressão</a>.<br /> Consulte a <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Especificação de Esquema de Impressão</a> para obter as informações de design mais atuais.<br /> | 




 

## <a name="additional-resources"></a>Recursos adicionais

O [aplicativo de exemplo Exemplo de](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) Impressão demonstra como imprimir de um aplicativo Windows Store do Windows 8.

Os recursos descritos nesta seção são para programação Windows nativa. Para usar recursos semelhantes na programação do .NET (gerenciado), [consulte Windows Presentation Foundation Documentos](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

Os documentos XPS são construídos na API [de Empacotamento.](/previous-versions/windows/desktop/opc/packaging) Consulte a API de Empacotamento para acesso de nível inferior ao conteúdo de um documento XPS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comunicações de impressora bidirecional (Centro de Desenvolvimento de Hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
