---
description: Para determinar a página de código de um banco de dados, chame MsiDatabaseExport com hDatabase definido como o identificador do banco de dados e szTableName definido como \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Determinando a página de código de um banco de dados de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89825c99e0652c0ef324c99f8906281f3c87ed58bef099886220faa6a9311583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637845"
---
# <a name="determining-an-installation-databases-code-page"></a>Determinando a página de código de um banco de dados de instalação

Para determinar a página de código de um banco de dados, chame [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) com *hDatabase* definido como o identificador do banco de dados e *szTableName* definido como \_ ForceCodepage. Isso exporta um arquivo de texto com uma extensão. IDT. As duas primeiras linhas desse arquivo estão em branco. A terceira linha é o número da página de código ANSI, seguido por uma guia, seguida pelo nome \_ ForceCodepage. Consulte também [manipulação de página de código de tabelas importadas e exportadas](code-page-handling-of-imported-and-exported-tables.md).

um exemplo de como determinar a página de código usando o [**método Export**](database-export.md) é fornecido no SDK do Windows Installer como parte do WiLangId.vbs do utilitário. Para obter mais informações sobre como usar WiLangId.vbs consulte o tópico: [gerenciar idioma e página de código](manage-language-and-codepage.md).

 

 



