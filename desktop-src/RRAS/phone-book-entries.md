---
title: Phone-Book entrada
description: Telefone de livros contém as informações necessárias para estabelecer uma conexão RAS. Um usuário ou administrador pode usar a Sistema de Rede de Conexão Discada caixa de diálogo para criar, editar e discar entradas de livro telefônica.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea62595504229dd5dd920385a92214156a7d112774cb3fefbaff3f1b5edc7cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789816"
---
# <a name="phone-book-entries"></a>Phone-Book entrada

Telefone de livros contém as informações necessárias para estabelecer uma conexão RAS. Um usuário ou administrador pode usar a **Sistema de Rede de Conexão Discada** caixa de diálogo para criar, editar e discar entradas de livro telefônica.

A partir do Windows NT Server 4.0, o sistema dá suporte às funções descritas para o Windows 95, bem como a várias funções adicionais que um aplicativo pode usar para trabalhar com livros telefônicas e entradas de livros telefônicas.

A [**função RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) exibe uma folha de propriedades que permite que o usuário crie, edite ou copie entradas de phone-book. As [**funções RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) [**e RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) chamam a **função RasEntryDlg.** Você pode usar a [**função RasRenameEntry**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) para renomear uma entrada de phone-book ou [**RasDeleteEntry**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) para excluir uma entrada. O [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) determina se uma cadeia de caracteres especificada tem o formato correto a ser usado como um nome de entrada.

Você pode usar [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para obter e definir informações adicionais sobre uma entrada de livro de telefone. Essas funções usam uma [**estrutura RASENTRY.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))

As [**funções RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) e [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) obterão e definirão as credenciais do usuário associadas a uma entrada de lista telefônica RAS especificada. Essas funções usam uma [**estrutura RASCREDENTIALS.**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85))

A [**função RasGetCountryInfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) recupera informações de discagem específicas do país/região da lista Windows telefonia de países. **RasGetCountryInfo** usa a [**estrutura RASCTRYINFO.**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85))

**Windows 95: ** Dá suporte a um conjunto limitado de funções para trabalhar com entradas de livro de telefone. Você pode usar as [**funções RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) e [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) para criar ou editar uma entrada de livro de telefone. Essas funções exibem uma caixa de diálogo na qual o usuário pode especificar informações sobre a entrada de phone-book. Você pode usar as [**funções RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) e [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) para definir ou recuperar os parâmetros de conexão para uma entrada de livro de telefone. A [**função RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) recupera uma matriz de estruturas [**RASENTRYNAME**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) que contêm os nomes de entrada de phone-book.

 

 