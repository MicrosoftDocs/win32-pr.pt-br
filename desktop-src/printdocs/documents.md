---
description: Esta seção descreve as tecnologias de documento com suporte do Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: Documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119981"
---
# <a name="xps-documents"></a>Documentos XPS

Esta seção descreve as tecnologias de documento com suporte do Microsoft Windows.

-   [Escolhendo uma tecnologia de documento](#choosing-a-document-technology)
-   [Nesta seção](#in-this-section)
-   [Ferramentas de documento XPS](#xps-document-tools)
-   [Tópicos relacionados](#related-topics)


## <a name="choosing-a-document-technology"></a>Escolhendo uma tecnologia de documento

A Microsoft fornece várias tecnologias de documentos diferentes para dar suporte a uma variedade de aplicativos de documentos:

-   **XPS e OpenXPS**

    XPS e OpenXPS têm suporte no Windows 8 e em versões posteriores do Windows. Consulte o diagrama anterior para determinar o cenário de uso correto para XPS e OpenXPS. Para obter mais informações sobre essas tecnologias de documento, consulte [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).

    No caso do uso do OpenXPS com o Windows 8 e o Windows Server 2012, o suporte é fornecido apenas por meio da [API de documento XPS](documents-xps.md)

    Se você precisar converter entre o Microsoft XPS (MSXPS) e o OpenXPS, a Microsoft forneceu uma ferramenta (XPSConverter.exe) que permite converter documentos formatados em MSXPS no formato OpenXPS e vice-versa. A ferramenta faz parte do WDK (Windows Driver Kit). Para baixar o WDK, consulte [como obter o WDK](/windows-hardware/drivers/download-the-wdk).

    Para obter mais informações sobre o OpenXPS e o Windows 8, consulte [suporte do OpenXPS no Windows](/windows-hardware/drivers/print/driver-support-for-openxps).

-   **API de documento XPS**

    A API do documento XPS é uma API nativa do Windows que dá suporte ao OM XPS. A API de documento XPS foi introduzida no Windows 7 e pode ser usada em programas de modo de usuário e drivers de impressora XPSDrv.

    Para obter mais informações, consulte a API de documento XPS e a [API de assinatura digital XPS](xps-digital-signatures.md).

    \*A API de documento XPS também tem suporte no Windows Vista com Service Pack 2 (SP2) com a atualização de plataforma para Windows Vista e Windows Server 2008 com SP2 usando a atualização de plataforma para o Windows Server 2008. Para obter mais informações sobre a atualização de plataforma para Windows Vista ou a atualização de plataforma para o Windows Server 2008, consulte [atualização de plataforma para Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)

-   **.NET Framework**

    .NET Framework fornece suporte a documentos XPS para programas de código gerenciado do modo de usuário.

    O .NET Framework 3,0 tem suporte no Windows XP com Service Pack 2 (SP2) e em versões posteriores de sistemas operacionais cliente Windows e no Windows Server 2003 com Service Pack 2 (SP2) e versões posteriores dos sistemas operacionais Windows Server.

    O .NET Framework 3,5 tem suporte em versões do Windows XP de sistemas operacionais cliente do Windows e no Windows Server 2003 e versões posteriores dos sistemas operacionais Windows Server.

    > [!Note]  
    > Recomendamos o uso de .NET Framework para criar documentos XPS somente em aplicativos cliente, não em aplicativos de servidor, a menos que o aplicativo saia periodicamente, como seria se fosse um aplicativo cliente.

     

    Para obter mais informações sobre o suporte a documentos no .NET Framework, consulte [Windows Presentation Foundation documentos](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

> [!Note]  
> Para trabalhar com documentos XPS em um programa, use a API de documento XPS nativo ou a .NET Framework; Não há suporte para o uso simultâneo de ambos no mesmo programa.

 

## <a name="in-this-section"></a>Nesta seção

Esta seção descreve as tecnologias de documento nativas do Windows com suporte no Microsoft Windows.



| Tecnologia de documentos                                                                   | Descrição                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [API de documento XPS](documents-xps.md)<br/>                   | Fornece um formato confiável para o documento eletrônico.<br/> A API de documento XPS descrita nesta seção fornece aos programas e drivers de impressão XPSDrv acesso ao conteúdo e aos metadados de um documento XPS.<br/> |
| [API de assinatura digital XPS](xps-digital-signatures.md)<br/> | Habilita a assinatura de documentos, a verificação da identidade do signatário e a indicação de se um documento XPS foi alterado desde que foi assinado.<br/>                                                                          |
| [Glossário de documentos XPS](xpsapi-glossary.md)<br/>           | Definições de termos usados pela [API de documento XPS](documents-xps.md) e pela [API de assinatura digital XPS](xps-digital-signatures.md).<br/>                                                                              |



 

## <a name="xps-document-tools"></a>Ferramentas de documento XPS

As ferramentas a seguir estão disponíveis para ajudá-lo a testar e solucionar problemas de arquivos de documento XPS.

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    Testa a conformidade de um arquivo com o XML Paper Specification (XPS) e a especificação do OPC (Open Packaging Conventions).

-   [XpsAnalyzer](/windows-hardware/drivers/devtest/xpsanalyzer)

    Uma ferramenta de prompt de comando que analisa arquivos de documento XPS para compatibilidade com a especificação XPS 1,0.

-   [PTConform](/previous-versions/dd327476(v=msdn.10))

    Uma ferramenta que verifica a validade de documentos PrintTicket e PrintCapabilities.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de impressão XPS](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[Empacotamento](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Impressão](./printdocs-printing.md)
</dt> <dt>
  
[Imprimir programa de exemplo](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))
</dt> </dl>

 

